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
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-jammy`](#rosrolling-ros-base-jammy)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-jammy`](#rosrolling-ros-core-jammy)

## `ros:foxy`

```console
$ docker pull ros@sha256:fc1dca46025189c33434f42fb22e5f6ee0f9e5b7052313f43d479e18a6ce88fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy` - linux; amd64

```console
$ docker pull ros@sha256:18e9dbacc08da9636fe5c515d7303715d0e87d15a53879ccab9d979087ba9a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251846325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c645eb93f5e52feb828db0e9fa5f313ca3c35a01dd8ebff251680537d6ad3403`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV ROS_DISTRO=foxy
# Fri, 22 Apr 2022 03:38:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:38:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:38:06 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:38:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:38:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:39:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e452458b64576978a29ec3371779b11068f93fb9c221ab69945e5c619ac2bd37`  
		Last Modified: Fri, 22 Apr 2022 03:52:44 GMT  
		Size: 120.1 MB (120084788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ab9a02fbc2fb68fd882c39887a0d9650772448527ff6fcaa3d0f5c55274778`  
		Last Modified: Fri, 22 Apr 2022 03:52:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3e6663cc7e7891e966d7dceec6d5a0b5514de61fb1d6a7bf484ef91a686c48`  
		Last Modified: Fri, 22 Apr 2022 03:53:06 GMT  
		Size: 74.5 MB (74539616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11483942dac1171bec761bd7edc1858b665ca4d6eb10be1f55d26f251bdd8e3e`  
		Last Modified: Fri, 22 Apr 2022 03:52:55 GMT  
		Size: 254.2 KB (254168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6a449ba3ea7f9f55f6e49fd90d40fdb8d928abdf760083c6f239ff44274761`  
		Last Modified: Fri, 22 Apr 2022 03:52:55 GMT  
		Size: 2.2 KB (2175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ddd03f832a092dd75d894aaf0dc3031bab4f643254329841d41a0f446918ea`  
		Last Modified: Fri, 22 Apr 2022 03:52:59 GMT  
		Size: 21.7 MB (21669649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d7a58e5756d186f12b068619c563049cf692f41ad01230655a898c34094cb7f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227245810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b043bac584a9e6280aac004d04edc2f7fd3c65f9ebde897d71690ea1bd21216`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:25:55 GMT
ENV ROS_DISTRO=foxy
# Sat, 30 Apr 2022 00:26:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:26:47 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:26:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:26:49 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:27:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:27:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:27:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:27:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e954138377bd97441a0963808a8c70e6c51bf87155d6bdb671530efd4a2af527`  
		Last Modified: Sat, 30 Apr 2022 00:41:20 GMT  
		Size: 104.3 MB (104266243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91245cadd2f0a13ba1496609e0e2f0f4b18302e97d37290d08553b24b77ad13`  
		Last Modified: Sat, 30 Apr 2022 00:41:02 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60afb6ca72387ba9902306d593fa053a9f27a64edd9dac6ed60164bd6606bc70`  
		Last Modified: Sat, 30 Apr 2022 00:41:42 GMT  
		Size: 68.7 MB (68673212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d22cef684130e343bfe87220672bc69f71f542aee8adce35eb893f194b2107b`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 254.9 KB (254867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf97d0af157d8836375c4d09c7145909aa0c3043f4011e862c55162dbb4101a`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 2.2 KB (2160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e657dd15b5ed4ccfe5d24e8cab5e2b032fe73c6e2edd134d2610969e5c8dc2a`  
		Last Modified: Sat, 30 Apr 2022 00:41:35 GMT  
		Size: 20.4 MB (20373496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base`

```console
$ docker pull ros@sha256:fc1dca46025189c33434f42fb22e5f6ee0f9e5b7052313f43d479e18a6ce88fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:18e9dbacc08da9636fe5c515d7303715d0e87d15a53879ccab9d979087ba9a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251846325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c645eb93f5e52feb828db0e9fa5f313ca3c35a01dd8ebff251680537d6ad3403`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV ROS_DISTRO=foxy
# Fri, 22 Apr 2022 03:38:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:38:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:38:06 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:38:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:38:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:39:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e452458b64576978a29ec3371779b11068f93fb9c221ab69945e5c619ac2bd37`  
		Last Modified: Fri, 22 Apr 2022 03:52:44 GMT  
		Size: 120.1 MB (120084788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ab9a02fbc2fb68fd882c39887a0d9650772448527ff6fcaa3d0f5c55274778`  
		Last Modified: Fri, 22 Apr 2022 03:52:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3e6663cc7e7891e966d7dceec6d5a0b5514de61fb1d6a7bf484ef91a686c48`  
		Last Modified: Fri, 22 Apr 2022 03:53:06 GMT  
		Size: 74.5 MB (74539616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11483942dac1171bec761bd7edc1858b665ca4d6eb10be1f55d26f251bdd8e3e`  
		Last Modified: Fri, 22 Apr 2022 03:52:55 GMT  
		Size: 254.2 KB (254168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6a449ba3ea7f9f55f6e49fd90d40fdb8d928abdf760083c6f239ff44274761`  
		Last Modified: Fri, 22 Apr 2022 03:52:55 GMT  
		Size: 2.2 KB (2175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ddd03f832a092dd75d894aaf0dc3031bab4f643254329841d41a0f446918ea`  
		Last Modified: Fri, 22 Apr 2022 03:52:59 GMT  
		Size: 21.7 MB (21669649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d7a58e5756d186f12b068619c563049cf692f41ad01230655a898c34094cb7f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227245810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b043bac584a9e6280aac004d04edc2f7fd3c65f9ebde897d71690ea1bd21216`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:25:55 GMT
ENV ROS_DISTRO=foxy
# Sat, 30 Apr 2022 00:26:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:26:47 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:26:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:26:49 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:27:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:27:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:27:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:27:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e954138377bd97441a0963808a8c70e6c51bf87155d6bdb671530efd4a2af527`  
		Last Modified: Sat, 30 Apr 2022 00:41:20 GMT  
		Size: 104.3 MB (104266243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91245cadd2f0a13ba1496609e0e2f0f4b18302e97d37290d08553b24b77ad13`  
		Last Modified: Sat, 30 Apr 2022 00:41:02 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60afb6ca72387ba9902306d593fa053a9f27a64edd9dac6ed60164bd6606bc70`  
		Last Modified: Sat, 30 Apr 2022 00:41:42 GMT  
		Size: 68.7 MB (68673212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d22cef684130e343bfe87220672bc69f71f542aee8adce35eb893f194b2107b`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 254.9 KB (254867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf97d0af157d8836375c4d09c7145909aa0c3043f4011e862c55162dbb4101a`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 2.2 KB (2160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e657dd15b5ed4ccfe5d24e8cab5e2b032fe73c6e2edd134d2610969e5c8dc2a`  
		Last Modified: Sat, 30 Apr 2022 00:41:35 GMT  
		Size: 20.4 MB (20373496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base-focal`

```console
$ docker pull ros@sha256:fc1dca46025189c33434f42fb22e5f6ee0f9e5b7052313f43d479e18a6ce88fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:18e9dbacc08da9636fe5c515d7303715d0e87d15a53879ccab9d979087ba9a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251846325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c645eb93f5e52feb828db0e9fa5f313ca3c35a01dd8ebff251680537d6ad3403`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV ROS_DISTRO=foxy
# Fri, 22 Apr 2022 03:38:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:38:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:38:06 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:38:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:38:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:39:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e452458b64576978a29ec3371779b11068f93fb9c221ab69945e5c619ac2bd37`  
		Last Modified: Fri, 22 Apr 2022 03:52:44 GMT  
		Size: 120.1 MB (120084788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ab9a02fbc2fb68fd882c39887a0d9650772448527ff6fcaa3d0f5c55274778`  
		Last Modified: Fri, 22 Apr 2022 03:52:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3e6663cc7e7891e966d7dceec6d5a0b5514de61fb1d6a7bf484ef91a686c48`  
		Last Modified: Fri, 22 Apr 2022 03:53:06 GMT  
		Size: 74.5 MB (74539616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11483942dac1171bec761bd7edc1858b665ca4d6eb10be1f55d26f251bdd8e3e`  
		Last Modified: Fri, 22 Apr 2022 03:52:55 GMT  
		Size: 254.2 KB (254168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6a449ba3ea7f9f55f6e49fd90d40fdb8d928abdf760083c6f239ff44274761`  
		Last Modified: Fri, 22 Apr 2022 03:52:55 GMT  
		Size: 2.2 KB (2175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ddd03f832a092dd75d894aaf0dc3031bab4f643254329841d41a0f446918ea`  
		Last Modified: Fri, 22 Apr 2022 03:52:59 GMT  
		Size: 21.7 MB (21669649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d7a58e5756d186f12b068619c563049cf692f41ad01230655a898c34094cb7f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227245810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b043bac584a9e6280aac004d04edc2f7fd3c65f9ebde897d71690ea1bd21216`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:25:55 GMT
ENV ROS_DISTRO=foxy
# Sat, 30 Apr 2022 00:26:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:26:47 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:26:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:26:49 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:27:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:27:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:27:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:27:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e954138377bd97441a0963808a8c70e6c51bf87155d6bdb671530efd4a2af527`  
		Last Modified: Sat, 30 Apr 2022 00:41:20 GMT  
		Size: 104.3 MB (104266243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91245cadd2f0a13ba1496609e0e2f0f4b18302e97d37290d08553b24b77ad13`  
		Last Modified: Sat, 30 Apr 2022 00:41:02 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60afb6ca72387ba9902306d593fa053a9f27a64edd9dac6ed60164bd6606bc70`  
		Last Modified: Sat, 30 Apr 2022 00:41:42 GMT  
		Size: 68.7 MB (68673212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d22cef684130e343bfe87220672bc69f71f542aee8adce35eb893f194b2107b`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 254.9 KB (254867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf97d0af157d8836375c4d09c7145909aa0c3043f4011e862c55162dbb4101a`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 2.2 KB (2160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e657dd15b5ed4ccfe5d24e8cab5e2b032fe73c6e2edd134d2610969e5c8dc2a`  
		Last Modified: Sat, 30 Apr 2022 00:41:35 GMT  
		Size: 20.4 MB (20373496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:6d9187be762a45d1f0a06a29a73fef9dbcf73e7d07e15bfd3743d953558dfb04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:1323f3efb34e39faf1164fc87cfe0465a3e8b2099bef1d297ed3d66afe7e1d81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155380717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ad8dd08c800843587e3d2836c25d19c199bc3a90245ff114b31365247ddf3b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV ROS_DISTRO=foxy
# Fri, 22 Apr 2022 03:38:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:38:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:38:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e452458b64576978a29ec3371779b11068f93fb9c221ab69945e5c619ac2bd37`  
		Last Modified: Fri, 22 Apr 2022 03:52:44 GMT  
		Size: 120.1 MB (120084788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ab9a02fbc2fb68fd882c39887a0d9650772448527ff6fcaa3d0f5c55274778`  
		Last Modified: Fri, 22 Apr 2022 03:52:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:74092d169aa613a7ecd87a3c9d2870fcc8f396a86f139c69d48b117b7594ca87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137942075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ba4581cfae71825fabbf137b7566979f5b578df240df7ea566972e0152fdc1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:25:55 GMT
ENV ROS_DISTRO=foxy
# Sat, 30 Apr 2022 00:26:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:26:47 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:26:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:26:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e954138377bd97441a0963808a8c70e6c51bf87155d6bdb671530efd4a2af527`  
		Last Modified: Sat, 30 Apr 2022 00:41:20 GMT  
		Size: 104.3 MB (104266243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91245cadd2f0a13ba1496609e0e2f0f4b18302e97d37290d08553b24b77ad13`  
		Last Modified: Sat, 30 Apr 2022 00:41:02 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core-focal`

```console
$ docker pull ros@sha256:6d9187be762a45d1f0a06a29a73fef9dbcf73e7d07e15bfd3743d953558dfb04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:1323f3efb34e39faf1164fc87cfe0465a3e8b2099bef1d297ed3d66afe7e1d81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155380717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ad8dd08c800843587e3d2836c25d19c199bc3a90245ff114b31365247ddf3b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV ROS_DISTRO=foxy
# Fri, 22 Apr 2022 03:38:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:38:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:38:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e452458b64576978a29ec3371779b11068f93fb9c221ab69945e5c619ac2bd37`  
		Last Modified: Fri, 22 Apr 2022 03:52:44 GMT  
		Size: 120.1 MB (120084788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ab9a02fbc2fb68fd882c39887a0d9650772448527ff6fcaa3d0f5c55274778`  
		Last Modified: Fri, 22 Apr 2022 03:52:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:74092d169aa613a7ecd87a3c9d2870fcc8f396a86f139c69d48b117b7594ca87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137942075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ba4581cfae71825fabbf137b7566979f5b578df240df7ea566972e0152fdc1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:25:55 GMT
ENV ROS_DISTRO=foxy
# Sat, 30 Apr 2022 00:26:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:26:47 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:26:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:26:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e954138377bd97441a0963808a8c70e6c51bf87155d6bdb671530efd4a2af527`  
		Last Modified: Sat, 30 Apr 2022 00:41:20 GMT  
		Size: 104.3 MB (104266243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91245cadd2f0a13ba1496609e0e2f0f4b18302e97d37290d08553b24b77ad13`  
		Last Modified: Sat, 30 Apr 2022 00:41:02 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:49052a99e3302a2128e3b99e1a57aa6fde09b277b7e17d871ea5323c3d137373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:f6f5c0a0e4853ebcb1d0c793d490da59bd2d64e6a5f872210082b42730db3f96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.7 MB (349716175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0977093e1753c1bf7fb7338dbbbce5e7fe7a1baee3a2b24ab01af46d236e91f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV ROS_DISTRO=foxy
# Fri, 22 Apr 2022 03:38:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:38:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:38:06 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:38:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:38:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:39:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:39:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:39:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:39:14 GMT
ENV ROS1_DISTRO=noetic
# Fri, 22 Apr 2022 03:39:14 GMT
ENV ROS2_DISTRO=foxy
# Fri, 22 Apr 2022 03:39:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:39:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:39:53 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e452458b64576978a29ec3371779b11068f93fb9c221ab69945e5c619ac2bd37`  
		Last Modified: Fri, 22 Apr 2022 03:52:44 GMT  
		Size: 120.1 MB (120084788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ab9a02fbc2fb68fd882c39887a0d9650772448527ff6fcaa3d0f5c55274778`  
		Last Modified: Fri, 22 Apr 2022 03:52:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3e6663cc7e7891e966d7dceec6d5a0b5514de61fb1d6a7bf484ef91a686c48`  
		Last Modified: Fri, 22 Apr 2022 03:53:06 GMT  
		Size: 74.5 MB (74539616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11483942dac1171bec761bd7edc1858b665ca4d6eb10be1f55d26f251bdd8e3e`  
		Last Modified: Fri, 22 Apr 2022 03:52:55 GMT  
		Size: 254.2 KB (254168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6a449ba3ea7f9f55f6e49fd90d40fdb8d928abdf760083c6f239ff44274761`  
		Last Modified: Fri, 22 Apr 2022 03:52:55 GMT  
		Size: 2.2 KB (2175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ddd03f832a092dd75d894aaf0dc3031bab4f643254329841d41a0f446918ea`  
		Last Modified: Fri, 22 Apr 2022 03:52:59 GMT  
		Size: 21.7 MB (21669649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b5f330b17bff3b79078ad4a779b74b71742d53f1bd9cb4bf256ab89fe6d3e`  
		Last Modified: Fri, 22 Apr 2022 03:53:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308cbc359a788776e176402454db5b48e363e38d8fbbcb052472da3aac8d9206`  
		Last Modified: Fri, 22 Apr 2022 03:53:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08aea5382ebe2ec51b07e3e93c6d68facc813a488754b27f195e36931889ddf7`  
		Last Modified: Fri, 22 Apr 2022 03:53:36 GMT  
		Size: 76.3 MB (76324782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c672e567bbdbc2ec09e3bf6b2f3e362e0a23eb023827223ce11a4463938b298`  
		Last Modified: Fri, 22 Apr 2022 03:53:26 GMT  
		Size: 21.5 MB (21544441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1febcc87ce4e65c78a1ec45e36df3fa2099f9b70f8e76560cb9db11e7c769834`  
		Last Modified: Fri, 22 Apr 2022 03:53:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8f2bdfbbd35f27434eacb61e1cc753f6a3dc69edecd9aee5dc13f245a51ff50c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.4 MB (317367145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c948ad83552ce31ced72bd4815e0565b48911d21c957a24f2099e6549becc79f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:25:55 GMT
ENV ROS_DISTRO=foxy
# Sat, 30 Apr 2022 00:26:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:26:47 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:26:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:26:49 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:27:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:27:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:27:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:27:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:05 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:09 GMT
ENV ROS1_DISTRO=noetic
# Sat, 30 Apr 2022 00:28:10 GMT
ENV ROS2_DISTRO=foxy
# Sat, 30 Apr 2022 00:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:54 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e954138377bd97441a0963808a8c70e6c51bf87155d6bdb671530efd4a2af527`  
		Last Modified: Sat, 30 Apr 2022 00:41:20 GMT  
		Size: 104.3 MB (104266243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91245cadd2f0a13ba1496609e0e2f0f4b18302e97d37290d08553b24b77ad13`  
		Last Modified: Sat, 30 Apr 2022 00:41:02 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60afb6ca72387ba9902306d593fa053a9f27a64edd9dac6ed60164bd6606bc70`  
		Last Modified: Sat, 30 Apr 2022 00:41:42 GMT  
		Size: 68.7 MB (68673212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d22cef684130e343bfe87220672bc69f71f542aee8adce35eb893f194b2107b`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 254.9 KB (254867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf97d0af157d8836375c4d09c7145909aa0c3043f4011e862c55162dbb4101a`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 2.2 KB (2160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e657dd15b5ed4ccfe5d24e8cab5e2b032fe73c6e2edd134d2610969e5c8dc2a`  
		Last Modified: Sat, 30 Apr 2022 00:41:35 GMT  
		Size: 20.4 MB (20373496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa861354fd70fd36143a3e94a568ce9e81bdbc1c5e222a6143efac91778d8fa`  
		Last Modified: Sat, 30 Apr 2022 00:42:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf14151782a20560e27aca7e73441befbb3c36d7dd202484e5b17bc7c5ce4050`  
		Last Modified: Sat, 30 Apr 2022 00:42:20 GMT  
		Size: 76.2 MB (76156204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a1b46f28edc250d9ba807da3c6f52c46ce707d4b58ff24ea6463fae42c70c`  
		Last Modified: Sat, 30 Apr 2022 00:42:08 GMT  
		Size: 14.0 MB (13964661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a723bcdccecac05d4dd6103b787a4f069f613618a753c6cbe7fdfe2bdf6143`  
		Last Modified: Sat, 30 Apr 2022 00:42:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:49052a99e3302a2128e3b99e1a57aa6fde09b277b7e17d871ea5323c3d137373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:f6f5c0a0e4853ebcb1d0c793d490da59bd2d64e6a5f872210082b42730db3f96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.7 MB (349716175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0977093e1753c1bf7fb7338dbbbce5e7fe7a1baee3a2b24ab01af46d236e91f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV ROS_DISTRO=foxy
# Fri, 22 Apr 2022 03:38:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:38:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:38:06 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:38:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:38:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:39:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:39:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:39:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:39:14 GMT
ENV ROS1_DISTRO=noetic
# Fri, 22 Apr 2022 03:39:14 GMT
ENV ROS2_DISTRO=foxy
# Fri, 22 Apr 2022 03:39:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:39:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:39:53 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e452458b64576978a29ec3371779b11068f93fb9c221ab69945e5c619ac2bd37`  
		Last Modified: Fri, 22 Apr 2022 03:52:44 GMT  
		Size: 120.1 MB (120084788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ab9a02fbc2fb68fd882c39887a0d9650772448527ff6fcaa3d0f5c55274778`  
		Last Modified: Fri, 22 Apr 2022 03:52:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3e6663cc7e7891e966d7dceec6d5a0b5514de61fb1d6a7bf484ef91a686c48`  
		Last Modified: Fri, 22 Apr 2022 03:53:06 GMT  
		Size: 74.5 MB (74539616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11483942dac1171bec761bd7edc1858b665ca4d6eb10be1f55d26f251bdd8e3e`  
		Last Modified: Fri, 22 Apr 2022 03:52:55 GMT  
		Size: 254.2 KB (254168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6a449ba3ea7f9f55f6e49fd90d40fdb8d928abdf760083c6f239ff44274761`  
		Last Modified: Fri, 22 Apr 2022 03:52:55 GMT  
		Size: 2.2 KB (2175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ddd03f832a092dd75d894aaf0dc3031bab4f643254329841d41a0f446918ea`  
		Last Modified: Fri, 22 Apr 2022 03:52:59 GMT  
		Size: 21.7 MB (21669649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b5f330b17bff3b79078ad4a779b74b71742d53f1bd9cb4bf256ab89fe6d3e`  
		Last Modified: Fri, 22 Apr 2022 03:53:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308cbc359a788776e176402454db5b48e363e38d8fbbcb052472da3aac8d9206`  
		Last Modified: Fri, 22 Apr 2022 03:53:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08aea5382ebe2ec51b07e3e93c6d68facc813a488754b27f195e36931889ddf7`  
		Last Modified: Fri, 22 Apr 2022 03:53:36 GMT  
		Size: 76.3 MB (76324782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c672e567bbdbc2ec09e3bf6b2f3e362e0a23eb023827223ce11a4463938b298`  
		Last Modified: Fri, 22 Apr 2022 03:53:26 GMT  
		Size: 21.5 MB (21544441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1febcc87ce4e65c78a1ec45e36df3fa2099f9b70f8e76560cb9db11e7c769834`  
		Last Modified: Fri, 22 Apr 2022 03:53:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8f2bdfbbd35f27434eacb61e1cc753f6a3dc69edecd9aee5dc13f245a51ff50c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.4 MB (317367145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c948ad83552ce31ced72bd4815e0565b48911d21c957a24f2099e6549becc79f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:25:55 GMT
ENV ROS_DISTRO=foxy
# Sat, 30 Apr 2022 00:26:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:26:47 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:26:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:26:49 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:27:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:27:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:27:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:27:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:05 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:09 GMT
ENV ROS1_DISTRO=noetic
# Sat, 30 Apr 2022 00:28:10 GMT
ENV ROS2_DISTRO=foxy
# Sat, 30 Apr 2022 00:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:54 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e954138377bd97441a0963808a8c70e6c51bf87155d6bdb671530efd4a2af527`  
		Last Modified: Sat, 30 Apr 2022 00:41:20 GMT  
		Size: 104.3 MB (104266243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91245cadd2f0a13ba1496609e0e2f0f4b18302e97d37290d08553b24b77ad13`  
		Last Modified: Sat, 30 Apr 2022 00:41:02 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60afb6ca72387ba9902306d593fa053a9f27a64edd9dac6ed60164bd6606bc70`  
		Last Modified: Sat, 30 Apr 2022 00:41:42 GMT  
		Size: 68.7 MB (68673212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d22cef684130e343bfe87220672bc69f71f542aee8adce35eb893f194b2107b`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 254.9 KB (254867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf97d0af157d8836375c4d09c7145909aa0c3043f4011e862c55162dbb4101a`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 2.2 KB (2160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e657dd15b5ed4ccfe5d24e8cab5e2b032fe73c6e2edd134d2610969e5c8dc2a`  
		Last Modified: Sat, 30 Apr 2022 00:41:35 GMT  
		Size: 20.4 MB (20373496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa861354fd70fd36143a3e94a568ce9e81bdbc1c5e222a6143efac91778d8fa`  
		Last Modified: Sat, 30 Apr 2022 00:42:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf14151782a20560e27aca7e73441befbb3c36d7dd202484e5b17bc7c5ce4050`  
		Last Modified: Sat, 30 Apr 2022 00:42:20 GMT  
		Size: 76.2 MB (76156204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a1b46f28edc250d9ba807da3c6f52c46ce707d4b58ff24ea6463fae42c70c`  
		Last Modified: Sat, 30 Apr 2022 00:42:08 GMT  
		Size: 14.0 MB (13964661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a723bcdccecac05d4dd6103b787a4f069f613618a753c6cbe7fdfe2bdf6143`  
		Last Modified: Sat, 30 Apr 2022 00:42:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic`

```console
$ docker pull ros@sha256:36b2fd60f78a92c1f8fb4eca95df77d3fdde60637fc142317537e54d96bcb3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic` - linux; amd64

```console
$ docker pull ros@sha256:57982240c0b1d9639b5d4017bd39fd04ffb6e1947f059b9bb2c46320879db806
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235830367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf1eab5ff47ea02c884e6f99e01b82106247185704ba244505d93fa6ec51b75`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:40:00 GMT
ENV ROS_DISTRO=galactic
# Fri, 22 Apr 2022 03:40:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:40:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:40:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:40:43 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:41:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:41:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:41:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:41:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a86987c94783b7f050791cd972e66bdcf20ee12dcccd1a0162756a9bbea3ff5`  
		Last Modified: Fri, 22 Apr 2022 03:54:05 GMT  
		Size: 103.7 MB (103662159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca3e7c02467d0b63472d97b71a8664755cfe96d8fe8c6842a7b4861910bc761`  
		Last Modified: Fri, 22 Apr 2022 03:53:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d81b4f14257aafe9c36754217f7b33e5594f7991bdc5fed442f3e351818ca6`  
		Last Modified: Fri, 22 Apr 2022 03:54:26 GMT  
		Size: 74.5 MB (74494199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86ee117572ea9ab37045a8143bd74f2c6fc866407f2c1b855fef3c348bec9f6`  
		Last Modified: Fri, 22 Apr 2022 03:54:15 GMT  
		Size: 262.2 KB (262250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc056e4b5fb80b3e3a36e14d46061812f16e11166015dfbf5c8e9f911b4bc5e0`  
		Last Modified: Fri, 22 Apr 2022 03:54:15 GMT  
		Size: 2.2 KB (2194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a725f33deb8c6696fb2fe8f21c3fe0f20e6598f23354c10b3d1953701fe651`  
		Last Modified: Fri, 22 Apr 2022 03:54:18 GMT  
		Size: 22.1 MB (22113636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dab7abec5a85308189ba03074b631e678a40e648f315dd42f0fa44542d7d8427
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (224034577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0d1d7744b8a9a5962675b09c96c177acfefc5c3db57cc4b5e9eebb9457e676`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:29:05 GMT
ENV ROS_DISTRO=galactic
# Sat, 30 Apr 2022 00:29:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:29:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:29:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:29:57 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:30:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:30:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:30:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:30:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc429bf8652d7c199bc2696f50eb5d6d96995a020de7042fcefc0c861e53b494`  
		Last Modified: Sat, 30 Apr 2022 00:42:49 GMT  
		Size: 100.0 MB (100040496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24d376e5e7a9471996a0ba2517b9f4860601c4b261f5b4568a13a3138e91451`  
		Last Modified: Sat, 30 Apr 2022 00:42:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c48e7d9d49e9d72193ee8a2410040fc2dbb905e90a5e87a2963ec1efc64dc2`  
		Last Modified: Sat, 30 Apr 2022 00:43:11 GMT  
		Size: 68.6 MB (68617962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d3c508c87335df6c90cdb63cfc533f43c7e76223a40d60d51d5a56d650b11`  
		Last Modified: Sat, 30 Apr 2022 00:43:01 GMT  
		Size: 262.9 KB (262931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174ce5304359afaff45591ca5d498cc4399f317742522047929ffc39f06c6af2`  
		Last Modified: Sat, 30 Apr 2022 00:43:01 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb658821f56c3fbaa2fa5ca66ecb34a323faf00bb9654441fcc020fd19e8570f`  
		Last Modified: Sat, 30 Apr 2022 00:43:04 GMT  
		Size: 21.4 MB (21435249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base`

```console
$ docker pull ros@sha256:36b2fd60f78a92c1f8fb4eca95df77d3fdde60637fc142317537e54d96bcb3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:57982240c0b1d9639b5d4017bd39fd04ffb6e1947f059b9bb2c46320879db806
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235830367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf1eab5ff47ea02c884e6f99e01b82106247185704ba244505d93fa6ec51b75`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:40:00 GMT
ENV ROS_DISTRO=galactic
# Fri, 22 Apr 2022 03:40:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:40:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:40:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:40:43 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:41:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:41:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:41:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:41:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a86987c94783b7f050791cd972e66bdcf20ee12dcccd1a0162756a9bbea3ff5`  
		Last Modified: Fri, 22 Apr 2022 03:54:05 GMT  
		Size: 103.7 MB (103662159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca3e7c02467d0b63472d97b71a8664755cfe96d8fe8c6842a7b4861910bc761`  
		Last Modified: Fri, 22 Apr 2022 03:53:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d81b4f14257aafe9c36754217f7b33e5594f7991bdc5fed442f3e351818ca6`  
		Last Modified: Fri, 22 Apr 2022 03:54:26 GMT  
		Size: 74.5 MB (74494199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86ee117572ea9ab37045a8143bd74f2c6fc866407f2c1b855fef3c348bec9f6`  
		Last Modified: Fri, 22 Apr 2022 03:54:15 GMT  
		Size: 262.2 KB (262250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc056e4b5fb80b3e3a36e14d46061812f16e11166015dfbf5c8e9f911b4bc5e0`  
		Last Modified: Fri, 22 Apr 2022 03:54:15 GMT  
		Size: 2.2 KB (2194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a725f33deb8c6696fb2fe8f21c3fe0f20e6598f23354c10b3d1953701fe651`  
		Last Modified: Fri, 22 Apr 2022 03:54:18 GMT  
		Size: 22.1 MB (22113636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dab7abec5a85308189ba03074b631e678a40e648f315dd42f0fa44542d7d8427
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (224034577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0d1d7744b8a9a5962675b09c96c177acfefc5c3db57cc4b5e9eebb9457e676`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:29:05 GMT
ENV ROS_DISTRO=galactic
# Sat, 30 Apr 2022 00:29:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:29:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:29:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:29:57 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:30:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:30:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:30:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:30:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc429bf8652d7c199bc2696f50eb5d6d96995a020de7042fcefc0c861e53b494`  
		Last Modified: Sat, 30 Apr 2022 00:42:49 GMT  
		Size: 100.0 MB (100040496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24d376e5e7a9471996a0ba2517b9f4860601c4b261f5b4568a13a3138e91451`  
		Last Modified: Sat, 30 Apr 2022 00:42:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c48e7d9d49e9d72193ee8a2410040fc2dbb905e90a5e87a2963ec1efc64dc2`  
		Last Modified: Sat, 30 Apr 2022 00:43:11 GMT  
		Size: 68.6 MB (68617962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d3c508c87335df6c90cdb63cfc533f43c7e76223a40d60d51d5a56d650b11`  
		Last Modified: Sat, 30 Apr 2022 00:43:01 GMT  
		Size: 262.9 KB (262931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174ce5304359afaff45591ca5d498cc4399f317742522047929ffc39f06c6af2`  
		Last Modified: Sat, 30 Apr 2022 00:43:01 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb658821f56c3fbaa2fa5ca66ecb34a323faf00bb9654441fcc020fd19e8570f`  
		Last Modified: Sat, 30 Apr 2022 00:43:04 GMT  
		Size: 21.4 MB (21435249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base-focal`

```console
$ docker pull ros@sha256:36b2fd60f78a92c1f8fb4eca95df77d3fdde60637fc142317537e54d96bcb3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:57982240c0b1d9639b5d4017bd39fd04ffb6e1947f059b9bb2c46320879db806
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235830367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf1eab5ff47ea02c884e6f99e01b82106247185704ba244505d93fa6ec51b75`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:40:00 GMT
ENV ROS_DISTRO=galactic
# Fri, 22 Apr 2022 03:40:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:40:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:40:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:40:43 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:41:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:41:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:41:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:41:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a86987c94783b7f050791cd972e66bdcf20ee12dcccd1a0162756a9bbea3ff5`  
		Last Modified: Fri, 22 Apr 2022 03:54:05 GMT  
		Size: 103.7 MB (103662159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca3e7c02467d0b63472d97b71a8664755cfe96d8fe8c6842a7b4861910bc761`  
		Last Modified: Fri, 22 Apr 2022 03:53:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d81b4f14257aafe9c36754217f7b33e5594f7991bdc5fed442f3e351818ca6`  
		Last Modified: Fri, 22 Apr 2022 03:54:26 GMT  
		Size: 74.5 MB (74494199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86ee117572ea9ab37045a8143bd74f2c6fc866407f2c1b855fef3c348bec9f6`  
		Last Modified: Fri, 22 Apr 2022 03:54:15 GMT  
		Size: 262.2 KB (262250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc056e4b5fb80b3e3a36e14d46061812f16e11166015dfbf5c8e9f911b4bc5e0`  
		Last Modified: Fri, 22 Apr 2022 03:54:15 GMT  
		Size: 2.2 KB (2194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a725f33deb8c6696fb2fe8f21c3fe0f20e6598f23354c10b3d1953701fe651`  
		Last Modified: Fri, 22 Apr 2022 03:54:18 GMT  
		Size: 22.1 MB (22113636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dab7abec5a85308189ba03074b631e678a40e648f315dd42f0fa44542d7d8427
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (224034577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0d1d7744b8a9a5962675b09c96c177acfefc5c3db57cc4b5e9eebb9457e676`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:29:05 GMT
ENV ROS_DISTRO=galactic
# Sat, 30 Apr 2022 00:29:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:29:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:29:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:29:57 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:30:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:30:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:30:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:30:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc429bf8652d7c199bc2696f50eb5d6d96995a020de7042fcefc0c861e53b494`  
		Last Modified: Sat, 30 Apr 2022 00:42:49 GMT  
		Size: 100.0 MB (100040496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24d376e5e7a9471996a0ba2517b9f4860601c4b261f5b4568a13a3138e91451`  
		Last Modified: Sat, 30 Apr 2022 00:42:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c48e7d9d49e9d72193ee8a2410040fc2dbb905e90a5e87a2963ec1efc64dc2`  
		Last Modified: Sat, 30 Apr 2022 00:43:11 GMT  
		Size: 68.6 MB (68617962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d3c508c87335df6c90cdb63cfc533f43c7e76223a40d60d51d5a56d650b11`  
		Last Modified: Sat, 30 Apr 2022 00:43:01 GMT  
		Size: 262.9 KB (262931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174ce5304359afaff45591ca5d498cc4399f317742522047929ffc39f06c6af2`  
		Last Modified: Sat, 30 Apr 2022 00:43:01 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb658821f56c3fbaa2fa5ca66ecb34a323faf00bb9654441fcc020fd19e8570f`  
		Last Modified: Sat, 30 Apr 2022 00:43:04 GMT  
		Size: 21.4 MB (21435249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core`

```console
$ docker pull ros@sha256:ec99a1f4552a6e073e072406131b25f6b3fd6b793626a909e4b6c1dadf5b54b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c644630aa2cadfb39da6be16c872c066e583724bb601c338cd9f9bba235c12bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138958088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce7931771f1d143f583c2a02af3a0452f1f4abd91a6da08f4bdab2b99b69347`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:40:00 GMT
ENV ROS_DISTRO=galactic
# Fri, 22 Apr 2022 03:40:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:40:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:40:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:40:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a86987c94783b7f050791cd972e66bdcf20ee12dcccd1a0162756a9bbea3ff5`  
		Last Modified: Fri, 22 Apr 2022 03:54:05 GMT  
		Size: 103.7 MB (103662159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca3e7c02467d0b63472d97b71a8664755cfe96d8fe8c6842a7b4861910bc761`  
		Last Modified: Fri, 22 Apr 2022 03:53:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3ed6a9e83e2aa8bc98fc3a7fd76344b5bbe2185f77d65a86c46a9e8ce47e57e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133716329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8861d548374a54940b31d30055fa3ce4692be4ea9418ac6afd0e5bb342237f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:29:05 GMT
ENV ROS_DISTRO=galactic
# Sat, 30 Apr 2022 00:29:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:29:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:29:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:29:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc429bf8652d7c199bc2696f50eb5d6d96995a020de7042fcefc0c861e53b494`  
		Last Modified: Sat, 30 Apr 2022 00:42:49 GMT  
		Size: 100.0 MB (100040496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24d376e5e7a9471996a0ba2517b9f4860601c4b261f5b4568a13a3138e91451`  
		Last Modified: Sat, 30 Apr 2022 00:42:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core-focal`

```console
$ docker pull ros@sha256:ec99a1f4552a6e073e072406131b25f6b3fd6b793626a909e4b6c1dadf5b54b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:c644630aa2cadfb39da6be16c872c066e583724bb601c338cd9f9bba235c12bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138958088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce7931771f1d143f583c2a02af3a0452f1f4abd91a6da08f4bdab2b99b69347`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:40:00 GMT
ENV ROS_DISTRO=galactic
# Fri, 22 Apr 2022 03:40:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:40:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:40:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:40:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a86987c94783b7f050791cd972e66bdcf20ee12dcccd1a0162756a9bbea3ff5`  
		Last Modified: Fri, 22 Apr 2022 03:54:05 GMT  
		Size: 103.7 MB (103662159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca3e7c02467d0b63472d97b71a8664755cfe96d8fe8c6842a7b4861910bc761`  
		Last Modified: Fri, 22 Apr 2022 03:53:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3ed6a9e83e2aa8bc98fc3a7fd76344b5bbe2185f77d65a86c46a9e8ce47e57e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133716329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8861d548374a54940b31d30055fa3ce4692be4ea9418ac6afd0e5bb342237f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:29:05 GMT
ENV ROS_DISTRO=galactic
# Sat, 30 Apr 2022 00:29:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:29:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:29:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:29:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc429bf8652d7c199bc2696f50eb5d6d96995a020de7042fcefc0c861e53b494`  
		Last Modified: Sat, 30 Apr 2022 00:42:49 GMT  
		Size: 100.0 MB (100040496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24d376e5e7a9471996a0ba2517b9f4860601c4b261f5b4568a13a3138e91451`  
		Last Modified: Sat, 30 Apr 2022 00:42:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge`

```console
$ docker pull ros@sha256:02e03dd4d4c7765cf7a5650358ab63f9da018473929537a76af21c19b684fe0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:1ee3ad3ffb633974159613107bbadc7f6dd7ad5807c60e139922774fe90e780b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330799106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f77c5f173ec4f3c66c94951fabd1f99f7111e3cb9bfc7aea69a7563c30d0c15`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:40:00 GMT
ENV ROS_DISTRO=galactic
# Fri, 22 Apr 2022 03:40:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:40:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:40:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:40:43 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:41:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:41:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:41:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:41:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:41:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:41:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:41:38 GMT
ENV ROS1_DISTRO=noetic
# Fri, 22 Apr 2022 03:41:38 GMT
ENV ROS2_DISTRO=galactic
# Fri, 22 Apr 2022 03:42:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:14 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a86987c94783b7f050791cd972e66bdcf20ee12dcccd1a0162756a9bbea3ff5`  
		Last Modified: Fri, 22 Apr 2022 03:54:05 GMT  
		Size: 103.7 MB (103662159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca3e7c02467d0b63472d97b71a8664755cfe96d8fe8c6842a7b4861910bc761`  
		Last Modified: Fri, 22 Apr 2022 03:53:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d81b4f14257aafe9c36754217f7b33e5594f7991bdc5fed442f3e351818ca6`  
		Last Modified: Fri, 22 Apr 2022 03:54:26 GMT  
		Size: 74.5 MB (74494199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86ee117572ea9ab37045a8143bd74f2c6fc866407f2c1b855fef3c348bec9f6`  
		Last Modified: Fri, 22 Apr 2022 03:54:15 GMT  
		Size: 262.2 KB (262250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc056e4b5fb80b3e3a36e14d46061812f16e11166015dfbf5c8e9f911b4bc5e0`  
		Last Modified: Fri, 22 Apr 2022 03:54:15 GMT  
		Size: 2.2 KB (2194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a725f33deb8c6696fb2fe8f21c3fe0f20e6598f23354c10b3d1953701fe651`  
		Last Modified: Fri, 22 Apr 2022 03:54:18 GMT  
		Size: 22.1 MB (22113636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35397945785dd434ec219e89250b0f82e33f7e60fa1ecaece9dc3c9e24bc0898`  
		Last Modified: Fri, 22 Apr 2022 03:54:40 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec5c0b2de935b90b5d54f02de899a12d4160855583ae6d65db5c6584a36dbe9`  
		Last Modified: Fri, 22 Apr 2022 03:54:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679fbb730a3136b74b5877ac3a03ee66cece62f0068afe23aae6173aad122c88`  
		Last Modified: Fri, 22 Apr 2022 03:54:54 GMT  
		Size: 78.6 MB (78597460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e57be180fb5ee836d1688d5d00f7ccf15ab87060b5d7f177b04ad4ca3c4ae4e`  
		Last Modified: Fri, 22 Apr 2022 03:54:43 GMT  
		Size: 16.4 MB (16370653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a40b523eed521aa1ac1f804bef4890d0051443a53b28d5d17dcf210e8e3098`  
		Last Modified: Fri, 22 Apr 2022 03:54:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:48962fe4314d31cfbe0c476bc5fc5aa5c6e3a86b036d2529e4181ccf4f3f6d02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (318030674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce0a6ba85ea8984ccfe00e891f3fa1fc5714370e4d0d173729d06d89ead5597`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:29:05 GMT
ENV ROS_DISTRO=galactic
# Sat, 30 Apr 2022 00:29:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:29:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:29:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:29:57 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:30:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:30:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:30:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:30:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:31:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:31:13 GMT
ENV ROS1_DISTRO=noetic
# Sat, 30 Apr 2022 00:31:14 GMT
ENV ROS2_DISTRO=galactic
# Sat, 30 Apr 2022 00:31:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:01 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc429bf8652d7c199bc2696f50eb5d6d96995a020de7042fcefc0c861e53b494`  
		Last Modified: Sat, 30 Apr 2022 00:42:49 GMT  
		Size: 100.0 MB (100040496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24d376e5e7a9471996a0ba2517b9f4860601c4b261f5b4568a13a3138e91451`  
		Last Modified: Sat, 30 Apr 2022 00:42:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c48e7d9d49e9d72193ee8a2410040fc2dbb905e90a5e87a2963ec1efc64dc2`  
		Last Modified: Sat, 30 Apr 2022 00:43:11 GMT  
		Size: 68.6 MB (68617962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d3c508c87335df6c90cdb63cfc533f43c7e76223a40d60d51d5a56d650b11`  
		Last Modified: Sat, 30 Apr 2022 00:43:01 GMT  
		Size: 262.9 KB (262931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174ce5304359afaff45591ca5d498cc4399f317742522047929ffc39f06c6af2`  
		Last Modified: Sat, 30 Apr 2022 00:43:01 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb658821f56c3fbaa2fa5ca66ecb34a323faf00bb9654441fcc020fd19e8570f`  
		Last Modified: Sat, 30 Apr 2022 00:43:04 GMT  
		Size: 21.4 MB (21435249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02c9a7a06776ddd2eac23260813a366f1d3f3e7dc80e9a4d2f2f6b4dbf53e63`  
		Last Modified: Sat, 30 Apr 2022 00:43:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cb6af35ed1d38b83eeb5f73eb9a821e0d2bb870d66062baff249aee9ecddb2`  
		Last Modified: Sat, 30 Apr 2022 00:43:43 GMT  
		Size: 78.3 MB (78325638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cd3ad1141d2aec27411320026308bd67afff55754028e3c0c53d04a45846d8`  
		Last Modified: Sat, 30 Apr 2022 00:43:30 GMT  
		Size: 15.7 MB (15669988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a8c3f4e5657b2b41897151effdbe5aa3f29312c704a85e9612296bc5996335`  
		Last Modified: Sat, 30 Apr 2022 00:43:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge-focal`

```console
$ docker pull ros@sha256:02e03dd4d4c7765cf7a5650358ab63f9da018473929537a76af21c19b684fe0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:1ee3ad3ffb633974159613107bbadc7f6dd7ad5807c60e139922774fe90e780b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330799106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f77c5f173ec4f3c66c94951fabd1f99f7111e3cb9bfc7aea69a7563c30d0c15`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:40:00 GMT
ENV ROS_DISTRO=galactic
# Fri, 22 Apr 2022 03:40:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:40:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:40:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:40:43 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:41:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:41:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:41:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:41:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:41:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:41:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:41:38 GMT
ENV ROS1_DISTRO=noetic
# Fri, 22 Apr 2022 03:41:38 GMT
ENV ROS2_DISTRO=galactic
# Fri, 22 Apr 2022 03:42:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:14 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a86987c94783b7f050791cd972e66bdcf20ee12dcccd1a0162756a9bbea3ff5`  
		Last Modified: Fri, 22 Apr 2022 03:54:05 GMT  
		Size: 103.7 MB (103662159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca3e7c02467d0b63472d97b71a8664755cfe96d8fe8c6842a7b4861910bc761`  
		Last Modified: Fri, 22 Apr 2022 03:53:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d81b4f14257aafe9c36754217f7b33e5594f7991bdc5fed442f3e351818ca6`  
		Last Modified: Fri, 22 Apr 2022 03:54:26 GMT  
		Size: 74.5 MB (74494199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86ee117572ea9ab37045a8143bd74f2c6fc866407f2c1b855fef3c348bec9f6`  
		Last Modified: Fri, 22 Apr 2022 03:54:15 GMT  
		Size: 262.2 KB (262250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc056e4b5fb80b3e3a36e14d46061812f16e11166015dfbf5c8e9f911b4bc5e0`  
		Last Modified: Fri, 22 Apr 2022 03:54:15 GMT  
		Size: 2.2 KB (2194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a725f33deb8c6696fb2fe8f21c3fe0f20e6598f23354c10b3d1953701fe651`  
		Last Modified: Fri, 22 Apr 2022 03:54:18 GMT  
		Size: 22.1 MB (22113636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35397945785dd434ec219e89250b0f82e33f7e60fa1ecaece9dc3c9e24bc0898`  
		Last Modified: Fri, 22 Apr 2022 03:54:40 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec5c0b2de935b90b5d54f02de899a12d4160855583ae6d65db5c6584a36dbe9`  
		Last Modified: Fri, 22 Apr 2022 03:54:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679fbb730a3136b74b5877ac3a03ee66cece62f0068afe23aae6173aad122c88`  
		Last Modified: Fri, 22 Apr 2022 03:54:54 GMT  
		Size: 78.6 MB (78597460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e57be180fb5ee836d1688d5d00f7ccf15ab87060b5d7f177b04ad4ca3c4ae4e`  
		Last Modified: Fri, 22 Apr 2022 03:54:43 GMT  
		Size: 16.4 MB (16370653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a40b523eed521aa1ac1f804bef4890d0051443a53b28d5d17dcf210e8e3098`  
		Last Modified: Fri, 22 Apr 2022 03:54:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:48962fe4314d31cfbe0c476bc5fc5aa5c6e3a86b036d2529e4181ccf4f3f6d02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (318030674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce0a6ba85ea8984ccfe00e891f3fa1fc5714370e4d0d173729d06d89ead5597`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:29:05 GMT
ENV ROS_DISTRO=galactic
# Sat, 30 Apr 2022 00:29:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:29:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:29:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:29:57 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:30:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:30:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:30:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:30:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:31:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:31:13 GMT
ENV ROS1_DISTRO=noetic
# Sat, 30 Apr 2022 00:31:14 GMT
ENV ROS2_DISTRO=galactic
# Sat, 30 Apr 2022 00:31:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:01 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc429bf8652d7c199bc2696f50eb5d6d96995a020de7042fcefc0c861e53b494`  
		Last Modified: Sat, 30 Apr 2022 00:42:49 GMT  
		Size: 100.0 MB (100040496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24d376e5e7a9471996a0ba2517b9f4860601c4b261f5b4568a13a3138e91451`  
		Last Modified: Sat, 30 Apr 2022 00:42:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c48e7d9d49e9d72193ee8a2410040fc2dbb905e90a5e87a2963ec1efc64dc2`  
		Last Modified: Sat, 30 Apr 2022 00:43:11 GMT  
		Size: 68.6 MB (68617962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d3c508c87335df6c90cdb63cfc533f43c7e76223a40d60d51d5a56d650b11`  
		Last Modified: Sat, 30 Apr 2022 00:43:01 GMT  
		Size: 262.9 KB (262931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174ce5304359afaff45591ca5d498cc4399f317742522047929ffc39f06c6af2`  
		Last Modified: Sat, 30 Apr 2022 00:43:01 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb658821f56c3fbaa2fa5ca66ecb34a323faf00bb9654441fcc020fd19e8570f`  
		Last Modified: Sat, 30 Apr 2022 00:43:04 GMT  
		Size: 21.4 MB (21435249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02c9a7a06776ddd2eac23260813a366f1d3f3e7dc80e9a4d2f2f6b4dbf53e63`  
		Last Modified: Sat, 30 Apr 2022 00:43:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cb6af35ed1d38b83eeb5f73eb9a821e0d2bb870d66062baff249aee9ecddb2`  
		Last Modified: Sat, 30 Apr 2022 00:43:43 GMT  
		Size: 78.3 MB (78325638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cd3ad1141d2aec27411320026308bd67afff55754028e3c0c53d04a45846d8`  
		Last Modified: Sat, 30 Apr 2022 00:43:30 GMT  
		Size: 15.7 MB (15669988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a8c3f4e5657b2b41897151effdbe5aa3f29312c704a85e9612296bc5996335`  
		Last Modified: Sat, 30 Apr 2022 00:43:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:fc1dca46025189c33434f42fb22e5f6ee0f9e5b7052313f43d479e18a6ce88fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:18e9dbacc08da9636fe5c515d7303715d0e87d15a53879ccab9d979087ba9a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251846325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c645eb93f5e52feb828db0e9fa5f313ca3c35a01dd8ebff251680537d6ad3403`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV ROS_DISTRO=foxy
# Fri, 22 Apr 2022 03:38:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:38:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:38:06 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:38:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:38:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:38:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:39:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e452458b64576978a29ec3371779b11068f93fb9c221ab69945e5c619ac2bd37`  
		Last Modified: Fri, 22 Apr 2022 03:52:44 GMT  
		Size: 120.1 MB (120084788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ab9a02fbc2fb68fd882c39887a0d9650772448527ff6fcaa3d0f5c55274778`  
		Last Modified: Fri, 22 Apr 2022 03:52:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3e6663cc7e7891e966d7dceec6d5a0b5514de61fb1d6a7bf484ef91a686c48`  
		Last Modified: Fri, 22 Apr 2022 03:53:06 GMT  
		Size: 74.5 MB (74539616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11483942dac1171bec761bd7edc1858b665ca4d6eb10be1f55d26f251bdd8e3e`  
		Last Modified: Fri, 22 Apr 2022 03:52:55 GMT  
		Size: 254.2 KB (254168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6a449ba3ea7f9f55f6e49fd90d40fdb8d928abdf760083c6f239ff44274761`  
		Last Modified: Fri, 22 Apr 2022 03:52:55 GMT  
		Size: 2.2 KB (2175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ddd03f832a092dd75d894aaf0dc3031bab4f643254329841d41a0f446918ea`  
		Last Modified: Fri, 22 Apr 2022 03:52:59 GMT  
		Size: 21.7 MB (21669649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d7a58e5756d186f12b068619c563049cf692f41ad01230655a898c34094cb7f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227245810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b043bac584a9e6280aac004d04edc2f7fd3c65f9ebde897d71690ea1bd21216`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:25:55 GMT
ENV ROS_DISTRO=foxy
# Sat, 30 Apr 2022 00:26:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:26:47 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:26:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:26:49 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:27:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:27:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:27:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:27:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e954138377bd97441a0963808a8c70e6c51bf87155d6bdb671530efd4a2af527`  
		Last Modified: Sat, 30 Apr 2022 00:41:20 GMT  
		Size: 104.3 MB (104266243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91245cadd2f0a13ba1496609e0e2f0f4b18302e97d37290d08553b24b77ad13`  
		Last Modified: Sat, 30 Apr 2022 00:41:02 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60afb6ca72387ba9902306d593fa053a9f27a64edd9dac6ed60164bd6606bc70`  
		Last Modified: Sat, 30 Apr 2022 00:41:42 GMT  
		Size: 68.7 MB (68673212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d22cef684130e343bfe87220672bc69f71f542aee8adce35eb893f194b2107b`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 254.9 KB (254867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf97d0af157d8836375c4d09c7145909aa0c3043f4011e862c55162dbb4101a`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 2.2 KB (2160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e657dd15b5ed4ccfe5d24e8cab5e2b032fe73c6e2edd134d2610969e5c8dc2a`  
		Last Modified: Sat, 30 Apr 2022 00:41:35 GMT  
		Size: 20.4 MB (20373496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic`

```console
$ docker pull ros@sha256:1d906c5b1ed01e5f591674e4b18546348c54514b65abb70158b7e5ef337d45db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic` - linux; amd64

```console
$ docker pull ros@sha256:b35e906f707bf988db588f95ca6370e62514d104a193a57b4632649a0d97b48c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.4 MB (437394244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5023ff407aa1e7f107544b46c999a8edce6403d120be868f5edb7d852da0eb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:12:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:16:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV ROS_DISTRO=melodic
# Fri, 22 Apr 2022 03:18:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:18:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:18:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:18:54 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:19:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:19:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:20:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d08ae4a50ec7a4071fcd259c6dc2b8f3219e66e5206c2f15ee781c4691a7699`  
		Last Modified: Fri, 22 Apr 2022 02:30:38 GMT  
		Size: 839.0 KB (838982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca35b07994f608387e199fa484cf0d3a586144538b7ea207fea47c25e64441b`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 4.9 MB (4872320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e99e7d92f7a9c84f55e914a1ad549e14ba4885ce72e1422955549eb8a42412`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda5797f8b0a501462dae5d9c7c7baa2ab56476067c48007d7f7d5f28e027821`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdb800ef4ebf782b8706d3ca51c5602217bfdaccffd3c87e146da0fd5b913a`  
		Last Modified: Fri, 22 Apr 2022 03:47:53 GMT  
		Size: 259.5 MB (259455669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1a8004d93ae4d2dcb4e49fb62c1ad152510f72453bd6d548075d99ffce4a72`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2772d37526d353480c40bc6613660a726bae949372e0b95ff5a4e9aef62d22cc`  
		Last Modified: Fri, 22 Apr 2022 03:48:13 GMT  
		Size: 70.2 MB (70241270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b2bccc87971a9fadd6a92eb4daea27c47e122f6de0c129f9cb64e2aa64019c`  
		Last Modified: Fri, 22 Apr 2022 03:48:03 GMT  
		Size: 279.1 KB (279107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f4d6dcfc3bd2fa9202d04bbd1d4f684046c0a525682228e9024af7ee3fee6`  
		Last Modified: Fri, 22 Apr 2022 03:48:15 GMT  
		Size: 75.0 MB (74994599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm variant v7

```console
$ docker pull ros@sha256:1d881fbd22871cd711f2824e52ca0e22ea1759aa60e9b703b778f96d6d13928c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385903779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f99306b40951ca6357fdb1ee9046768a03bed48d10a058806e68a8476874069`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:25 GMT
ADD file:9604e3641a386ec134596dd717862c2386c1b90009c0646b1773930f98949d9c in / 
# Fri, 29 Apr 2022 22:58:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:28:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:41 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:31:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:31:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:31:55 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:03ca5b55b2bdc3c68d23c18a88c099e2015c6bdcef6e3c43ca0bfb6aea0b032a`  
		Last Modified: Fri, 29 Apr 2022 23:02:31 GMT  
		Size: 22.3 MB (22300451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ab3231e4fbaccf7df6d1d44ef88608a6c1b716de9810c8e2ad6b7dcc9f5fc`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 840.2 KB (840158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f529e0e8ed7433413f39308a48052c609e82179d4d22b76f62189c616e5fe14`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 4.1 MB (4086200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59f023c86c2016dd149f7a89f71dc59cb35eeaf64c75eadba638336b28f6abd`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdf654803a8e788e4166c4bf287b5137ec541b313ce50e4d9401f0bd63fc8d`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa17f883dcf2090ca188521c82e8ecd78e6182c5c0af353b2dee9a1b0e0c44e`  
		Last Modified: Sat, 30 Apr 2022 00:53:38 GMT  
		Size: 238.9 MB (238937435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27e0b0ee020522ab3317cb8094bd430e3fb49425c99d1cfafe5284f0562f68`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c89127f2ab55d40e6d39537412903ef429801ea54d6baf3a6439a6bb01692f0`  
		Last Modified: Sat, 30 Apr 2022 00:54:21 GMT  
		Size: 54.7 MB (54710630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108adfc0916db7aeda7a39615caa2cee9b6fbe75cd66aa27a2ac82eaf1e6e9b9`  
		Last Modified: Sat, 30 Apr 2022 00:53:50 GMT  
		Size: 280.0 KB (279967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab1dc1feb0f323edf28a08fb0fcfc3796eb524ac698714b37837180467e312`  
		Last Modified: Sat, 30 Apr 2022 00:54:36 GMT  
		Size: 64.7 MB (64746523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:86b3f38d9bc9cc4ee2d33234df5041dc6f3d66f36083940df940dbd204ce3207
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.6 MB (411582882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83530c05ad8de8ce3636161e25b23921e4b94ab77b64d3eaffeff2253a6625d1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:15:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:15:31 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:15:32 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:15:33 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:16:57 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:16:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:17:00 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:17:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:17:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:18:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9119a950b820c04a3c9309fd9cd748b4a1c924ef00ac90dcd01791d857977923`  
		Last Modified: Sat, 30 Apr 2022 00:35:56 GMT  
		Size: 839.8 KB (839766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54865980d811f13a848975797615c6b0c5f21fed029eb255b5a1b3a0566900ec`  
		Last Modified: Sat, 30 Apr 2022 00:35:55 GMT  
		Size: 4.3 MB (4264191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d745fee38250cce36d1723e6eb3964a525bb738eb2c82b501244732a881913`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbae97ea1f2eea13534851ba6f58745635c465f6dd61681051632a7cac4bc8c`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccf8a195bad2001e20b085a797b257c60b2e4020d738441e352b661525e5029`  
		Last Modified: Sat, 30 Apr 2022 00:36:30 GMT  
		Size: 252.4 MB (252383482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c7449338629d393daa386d56eda7c00568a57dd328cd7df0410b5e398458d`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9440733505277e8f3f7d4bc2ad385b06e37093582b77feeef90fbf8570dddf3c`  
		Last Modified: Sat, 30 Apr 2022 00:36:51 GMT  
		Size: 63.1 MB (63076164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8b76e35d4800cba2ffd96b6e5766991c5f6f8df302a89558162e2756996fac`  
		Last Modified: Sat, 30 Apr 2022 00:36:42 GMT  
		Size: 279.9 KB (279913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240a0f2f7118df62260d84e096be2a18536d017cef9a31f1ecdb65a6c2608eed`  
		Last Modified: Sat, 30 Apr 2022 00:36:53 GMT  
		Size: 67.0 MB (67001910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception`

```console
$ docker pull ros@sha256:8839d389f0b2797002339956a750d664cef04b20da4cf7c4fd6f29b95488344e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception` - linux; amd64

```console
$ docker pull ros@sha256:b3404f2853827d7efc1e557ee67ecec5abad6c4be9b4ef8ecf5fb030e9a4f454
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.7 MB (742710927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f2b2bc1d75b72a2da3c58631a301ce9812d3a552f21af6f8137544a5d409b9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:12:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:16:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV ROS_DISTRO=melodic
# Fri, 22 Apr 2022 03:18:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:18:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:18:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:18:54 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:19:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:19:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:20:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d08ae4a50ec7a4071fcd259c6dc2b8f3219e66e5206c2f15ee781c4691a7699`  
		Last Modified: Fri, 22 Apr 2022 02:30:38 GMT  
		Size: 839.0 KB (838982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca35b07994f608387e199fa484cf0d3a586144538b7ea207fea47c25e64441b`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 4.9 MB (4872320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e99e7d92f7a9c84f55e914a1ad549e14ba4885ce72e1422955549eb8a42412`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda5797f8b0a501462dae5d9c7c7baa2ab56476067c48007d7f7d5f28e027821`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdb800ef4ebf782b8706d3ca51c5602217bfdaccffd3c87e146da0fd5b913a`  
		Last Modified: Fri, 22 Apr 2022 03:47:53 GMT  
		Size: 259.5 MB (259455669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1a8004d93ae4d2dcb4e49fb62c1ad152510f72453bd6d548075d99ffce4a72`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2772d37526d353480c40bc6613660a726bae949372e0b95ff5a4e9aef62d22cc`  
		Last Modified: Fri, 22 Apr 2022 03:48:13 GMT  
		Size: 70.2 MB (70241270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b2bccc87971a9fadd6a92eb4daea27c47e122f6de0c129f9cb64e2aa64019c`  
		Last Modified: Fri, 22 Apr 2022 03:48:03 GMT  
		Size: 279.1 KB (279107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f4d6dcfc3bd2fa9202d04bbd1d4f684046c0a525682228e9024af7ee3fee6`  
		Last Modified: Fri, 22 Apr 2022 03:48:15 GMT  
		Size: 75.0 MB (74994599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493c771b079d789db9df9583325355027638af6b25d95d4a937ce930de755c04`  
		Last Modified: Fri, 22 Apr 2022 03:49:28 GMT  
		Size: 305.3 MB (305316683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:cd396be2ca46cd7dfcde32f48d42a211db6e312784912e3628744900d6b0c2b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.9 MB (645946166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859f432cda36e5a6f96e8a2d4597ec613a7e4cb99907a711467d08e775f9e5a5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:25 GMT
ADD file:9604e3641a386ec134596dd717862c2386c1b90009c0646b1773930f98949d9c in / 
# Fri, 29 Apr 2022 22:58:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:28:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:41 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:31:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:31:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:31:55 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:38:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:03ca5b55b2bdc3c68d23c18a88c099e2015c6bdcef6e3c43ca0bfb6aea0b032a`  
		Last Modified: Fri, 29 Apr 2022 23:02:31 GMT  
		Size: 22.3 MB (22300451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ab3231e4fbaccf7df6d1d44ef88608a6c1b716de9810c8e2ad6b7dcc9f5fc`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 840.2 KB (840158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f529e0e8ed7433413f39308a48052c609e82179d4d22b76f62189c616e5fe14`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 4.1 MB (4086200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59f023c86c2016dd149f7a89f71dc59cb35eeaf64c75eadba638336b28f6abd`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdf654803a8e788e4166c4bf287b5137ec541b313ce50e4d9401f0bd63fc8d`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa17f883dcf2090ca188521c82e8ecd78e6182c5c0af353b2dee9a1b0e0c44e`  
		Last Modified: Sat, 30 Apr 2022 00:53:38 GMT  
		Size: 238.9 MB (238937435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27e0b0ee020522ab3317cb8094bd430e3fb49425c99d1cfafe5284f0562f68`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c89127f2ab55d40e6d39537412903ef429801ea54d6baf3a6439a6bb01692f0`  
		Last Modified: Sat, 30 Apr 2022 00:54:21 GMT  
		Size: 54.7 MB (54710630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108adfc0916db7aeda7a39615caa2cee9b6fbe75cd66aa27a2ac82eaf1e6e9b9`  
		Last Modified: Sat, 30 Apr 2022 00:53:50 GMT  
		Size: 280.0 KB (279967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab1dc1feb0f323edf28a08fb0fcfc3796eb524ac698714b37837180467e312`  
		Last Modified: Sat, 30 Apr 2022 00:54:36 GMT  
		Size: 64.7 MB (64746523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d75072f0ae1c4ebd364e5b399abd459ffbe79508b5305949c7e203edd68958e`  
		Last Modified: Sat, 30 Apr 2022 00:57:57 GMT  
		Size: 260.0 MB (260042387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ca807f065cfad860bd04db915ee044c80c79ad8c20e9cae96a25a022007580ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.0 MB (702991669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca9aa4207c71c21c1033211abdbac9667291fac2ddc21690b6bcc11f58379cf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:15:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:15:31 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:15:32 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:15:33 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:16:57 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:16:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:17:00 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:17:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:17:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:18:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9119a950b820c04a3c9309fd9cd748b4a1c924ef00ac90dcd01791d857977923`  
		Last Modified: Sat, 30 Apr 2022 00:35:56 GMT  
		Size: 839.8 KB (839766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54865980d811f13a848975797615c6b0c5f21fed029eb255b5a1b3a0566900ec`  
		Last Modified: Sat, 30 Apr 2022 00:35:55 GMT  
		Size: 4.3 MB (4264191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d745fee38250cce36d1723e6eb3964a525bb738eb2c82b501244732a881913`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbae97ea1f2eea13534851ba6f58745635c465f6dd61681051632a7cac4bc8c`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccf8a195bad2001e20b085a797b257c60b2e4020d738441e352b661525e5029`  
		Last Modified: Sat, 30 Apr 2022 00:36:30 GMT  
		Size: 252.4 MB (252383482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c7449338629d393daa386d56eda7c00568a57dd328cd7df0410b5e398458d`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9440733505277e8f3f7d4bc2ad385b06e37093582b77feeef90fbf8570dddf3c`  
		Last Modified: Sat, 30 Apr 2022 00:36:51 GMT  
		Size: 63.1 MB (63076164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8b76e35d4800cba2ffd96b6e5766991c5f6f8df302a89558162e2756996fac`  
		Last Modified: Sat, 30 Apr 2022 00:36:42 GMT  
		Size: 279.9 KB (279913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240a0f2f7118df62260d84e096be2a18536d017cef9a31f1ecdb65a6c2608eed`  
		Last Modified: Sat, 30 Apr 2022 00:36:53 GMT  
		Size: 67.0 MB (67001910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dea0e3098d641876fd5b669fc706eb09153bbfc9a9965819f7887cd6e57416`  
		Last Modified: Sat, 30 Apr 2022 00:38:05 GMT  
		Size: 291.4 MB (291408787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception-bionic`

```console
$ docker pull ros@sha256:8839d389f0b2797002339956a750d664cef04b20da4cf7c4fd6f29b95488344e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception-bionic` - linux; amd64

```console
$ docker pull ros@sha256:b3404f2853827d7efc1e557ee67ecec5abad6c4be9b4ef8ecf5fb030e9a4f454
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.7 MB (742710927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f2b2bc1d75b72a2da3c58631a301ce9812d3a552f21af6f8137544a5d409b9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:12:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:16:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV ROS_DISTRO=melodic
# Fri, 22 Apr 2022 03:18:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:18:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:18:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:18:54 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:19:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:19:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:20:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d08ae4a50ec7a4071fcd259c6dc2b8f3219e66e5206c2f15ee781c4691a7699`  
		Last Modified: Fri, 22 Apr 2022 02:30:38 GMT  
		Size: 839.0 KB (838982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca35b07994f608387e199fa484cf0d3a586144538b7ea207fea47c25e64441b`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 4.9 MB (4872320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e99e7d92f7a9c84f55e914a1ad549e14ba4885ce72e1422955549eb8a42412`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda5797f8b0a501462dae5d9c7c7baa2ab56476067c48007d7f7d5f28e027821`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdb800ef4ebf782b8706d3ca51c5602217bfdaccffd3c87e146da0fd5b913a`  
		Last Modified: Fri, 22 Apr 2022 03:47:53 GMT  
		Size: 259.5 MB (259455669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1a8004d93ae4d2dcb4e49fb62c1ad152510f72453bd6d548075d99ffce4a72`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2772d37526d353480c40bc6613660a726bae949372e0b95ff5a4e9aef62d22cc`  
		Last Modified: Fri, 22 Apr 2022 03:48:13 GMT  
		Size: 70.2 MB (70241270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b2bccc87971a9fadd6a92eb4daea27c47e122f6de0c129f9cb64e2aa64019c`  
		Last Modified: Fri, 22 Apr 2022 03:48:03 GMT  
		Size: 279.1 KB (279107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f4d6dcfc3bd2fa9202d04bbd1d4f684046c0a525682228e9024af7ee3fee6`  
		Last Modified: Fri, 22 Apr 2022 03:48:15 GMT  
		Size: 75.0 MB (74994599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493c771b079d789db9df9583325355027638af6b25d95d4a937ce930de755c04`  
		Last Modified: Fri, 22 Apr 2022 03:49:28 GMT  
		Size: 305.3 MB (305316683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:cd396be2ca46cd7dfcde32f48d42a211db6e312784912e3628744900d6b0c2b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.9 MB (645946166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859f432cda36e5a6f96e8a2d4597ec613a7e4cb99907a711467d08e775f9e5a5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:25 GMT
ADD file:9604e3641a386ec134596dd717862c2386c1b90009c0646b1773930f98949d9c in / 
# Fri, 29 Apr 2022 22:58:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:28:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:41 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:31:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:31:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:31:55 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:38:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:03ca5b55b2bdc3c68d23c18a88c099e2015c6bdcef6e3c43ca0bfb6aea0b032a`  
		Last Modified: Fri, 29 Apr 2022 23:02:31 GMT  
		Size: 22.3 MB (22300451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ab3231e4fbaccf7df6d1d44ef88608a6c1b716de9810c8e2ad6b7dcc9f5fc`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 840.2 KB (840158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f529e0e8ed7433413f39308a48052c609e82179d4d22b76f62189c616e5fe14`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 4.1 MB (4086200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59f023c86c2016dd149f7a89f71dc59cb35eeaf64c75eadba638336b28f6abd`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdf654803a8e788e4166c4bf287b5137ec541b313ce50e4d9401f0bd63fc8d`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa17f883dcf2090ca188521c82e8ecd78e6182c5c0af353b2dee9a1b0e0c44e`  
		Last Modified: Sat, 30 Apr 2022 00:53:38 GMT  
		Size: 238.9 MB (238937435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27e0b0ee020522ab3317cb8094bd430e3fb49425c99d1cfafe5284f0562f68`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c89127f2ab55d40e6d39537412903ef429801ea54d6baf3a6439a6bb01692f0`  
		Last Modified: Sat, 30 Apr 2022 00:54:21 GMT  
		Size: 54.7 MB (54710630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108adfc0916db7aeda7a39615caa2cee9b6fbe75cd66aa27a2ac82eaf1e6e9b9`  
		Last Modified: Sat, 30 Apr 2022 00:53:50 GMT  
		Size: 280.0 KB (279967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab1dc1feb0f323edf28a08fb0fcfc3796eb524ac698714b37837180467e312`  
		Last Modified: Sat, 30 Apr 2022 00:54:36 GMT  
		Size: 64.7 MB (64746523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d75072f0ae1c4ebd364e5b399abd459ffbe79508b5305949c7e203edd68958e`  
		Last Modified: Sat, 30 Apr 2022 00:57:57 GMT  
		Size: 260.0 MB (260042387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ca807f065cfad860bd04db915ee044c80c79ad8c20e9cae96a25a022007580ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.0 MB (702991669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca9aa4207c71c21c1033211abdbac9667291fac2ddc21690b6bcc11f58379cf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:15:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:15:31 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:15:32 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:15:33 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:16:57 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:16:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:17:00 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:17:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:17:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:18:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9119a950b820c04a3c9309fd9cd748b4a1c924ef00ac90dcd01791d857977923`  
		Last Modified: Sat, 30 Apr 2022 00:35:56 GMT  
		Size: 839.8 KB (839766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54865980d811f13a848975797615c6b0c5f21fed029eb255b5a1b3a0566900ec`  
		Last Modified: Sat, 30 Apr 2022 00:35:55 GMT  
		Size: 4.3 MB (4264191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d745fee38250cce36d1723e6eb3964a525bb738eb2c82b501244732a881913`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbae97ea1f2eea13534851ba6f58745635c465f6dd61681051632a7cac4bc8c`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccf8a195bad2001e20b085a797b257c60b2e4020d738441e352b661525e5029`  
		Last Modified: Sat, 30 Apr 2022 00:36:30 GMT  
		Size: 252.4 MB (252383482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c7449338629d393daa386d56eda7c00568a57dd328cd7df0410b5e398458d`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9440733505277e8f3f7d4bc2ad385b06e37093582b77feeef90fbf8570dddf3c`  
		Last Modified: Sat, 30 Apr 2022 00:36:51 GMT  
		Size: 63.1 MB (63076164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8b76e35d4800cba2ffd96b6e5766991c5f6f8df302a89558162e2756996fac`  
		Last Modified: Sat, 30 Apr 2022 00:36:42 GMT  
		Size: 279.9 KB (279913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240a0f2f7118df62260d84e096be2a18536d017cef9a31f1ecdb65a6c2608eed`  
		Last Modified: Sat, 30 Apr 2022 00:36:53 GMT  
		Size: 67.0 MB (67001910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dea0e3098d641876fd5b669fc706eb09153bbfc9a9965819f7887cd6e57416`  
		Last Modified: Sat, 30 Apr 2022 00:38:05 GMT  
		Size: 291.4 MB (291408787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot`

```console
$ docker pull ros@sha256:7ea13828785d507116d34792afc9dd2c805226ef4b3600671c1ec5c596d5146c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:a28bc3f892f1dfeecae7a00ba6304b00add7a4f48d9ecc1357d7bd5a3f87a2d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448477280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec5677d8005df5c0680c12d81e6e284c12cbdf56cd93577cbf4d460cf52bd33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:12:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:16:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV ROS_DISTRO=melodic
# Fri, 22 Apr 2022 03:18:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:18:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:18:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:18:54 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:19:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:19:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:20:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:21:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d08ae4a50ec7a4071fcd259c6dc2b8f3219e66e5206c2f15ee781c4691a7699`  
		Last Modified: Fri, 22 Apr 2022 02:30:38 GMT  
		Size: 839.0 KB (838982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca35b07994f608387e199fa484cf0d3a586144538b7ea207fea47c25e64441b`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 4.9 MB (4872320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e99e7d92f7a9c84f55e914a1ad549e14ba4885ce72e1422955549eb8a42412`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda5797f8b0a501462dae5d9c7c7baa2ab56476067c48007d7f7d5f28e027821`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdb800ef4ebf782b8706d3ca51c5602217bfdaccffd3c87e146da0fd5b913a`  
		Last Modified: Fri, 22 Apr 2022 03:47:53 GMT  
		Size: 259.5 MB (259455669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1a8004d93ae4d2dcb4e49fb62c1ad152510f72453bd6d548075d99ffce4a72`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2772d37526d353480c40bc6613660a726bae949372e0b95ff5a4e9aef62d22cc`  
		Last Modified: Fri, 22 Apr 2022 03:48:13 GMT  
		Size: 70.2 MB (70241270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b2bccc87971a9fadd6a92eb4daea27c47e122f6de0c129f9cb64e2aa64019c`  
		Last Modified: Fri, 22 Apr 2022 03:48:03 GMT  
		Size: 279.1 KB (279107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f4d6dcfc3bd2fa9202d04bbd1d4f684046c0a525682228e9024af7ee3fee6`  
		Last Modified: Fri, 22 Apr 2022 03:48:15 GMT  
		Size: 75.0 MB (74994599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453ce09845a35fb485ffe49a62e58ecd3d528a9aeb7429bdf7fd6941e6eb3ffa`  
		Last Modified: Fri, 22 Apr 2022 03:48:30 GMT  
		Size: 11.1 MB (11083036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:1d14bd9194543ed4a9d9f0dd81dbc60b9e4ceb6ddf151a2e4a2a09cda63e5b6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 MB (396027305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063acd2980c8c66d21cb505f4234c799e9f46aa28de7caa2849f8448d946245a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:25 GMT
ADD file:9604e3641a386ec134596dd717862c2386c1b90009c0646b1773930f98949d9c in / 
# Fri, 29 Apr 2022 22:58:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:28:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:41 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:31:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:31:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:31:55 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:35:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:03ca5b55b2bdc3c68d23c18a88c099e2015c6bdcef6e3c43ca0bfb6aea0b032a`  
		Last Modified: Fri, 29 Apr 2022 23:02:31 GMT  
		Size: 22.3 MB (22300451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ab3231e4fbaccf7df6d1d44ef88608a6c1b716de9810c8e2ad6b7dcc9f5fc`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 840.2 KB (840158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f529e0e8ed7433413f39308a48052c609e82179d4d22b76f62189c616e5fe14`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 4.1 MB (4086200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59f023c86c2016dd149f7a89f71dc59cb35eeaf64c75eadba638336b28f6abd`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdf654803a8e788e4166c4bf287b5137ec541b313ce50e4d9401f0bd63fc8d`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa17f883dcf2090ca188521c82e8ecd78e6182c5c0af353b2dee9a1b0e0c44e`  
		Last Modified: Sat, 30 Apr 2022 00:53:38 GMT  
		Size: 238.9 MB (238937435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27e0b0ee020522ab3317cb8094bd430e3fb49425c99d1cfafe5284f0562f68`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c89127f2ab55d40e6d39537412903ef429801ea54d6baf3a6439a6bb01692f0`  
		Last Modified: Sat, 30 Apr 2022 00:54:21 GMT  
		Size: 54.7 MB (54710630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108adfc0916db7aeda7a39615caa2cee9b6fbe75cd66aa27a2ac82eaf1e6e9b9`  
		Last Modified: Sat, 30 Apr 2022 00:53:50 GMT  
		Size: 280.0 KB (279967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab1dc1feb0f323edf28a08fb0fcfc3796eb524ac698714b37837180467e312`  
		Last Modified: Sat, 30 Apr 2022 00:54:36 GMT  
		Size: 64.7 MB (64746523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b852a9e6f9b9db1a873f5d26b96fa8e2ec994256c7153e1ef272a96d26c60c`  
		Last Modified: Sat, 30 Apr 2022 00:54:59 GMT  
		Size: 10.1 MB (10123526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dc415320b59ed3eceb471c9a86f2fc6febaf558f3bcc16cc737987b61c97d90f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.3 MB (422317875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7546d28bc1ce4883d78a9030d968b5c8fc659fcd88fbf850437db6e51fdd5a57`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:15:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:15:31 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:15:32 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:15:33 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:16:57 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:16:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:17:00 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:17:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:17:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:18:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:18:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9119a950b820c04a3c9309fd9cd748b4a1c924ef00ac90dcd01791d857977923`  
		Last Modified: Sat, 30 Apr 2022 00:35:56 GMT  
		Size: 839.8 KB (839766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54865980d811f13a848975797615c6b0c5f21fed029eb255b5a1b3a0566900ec`  
		Last Modified: Sat, 30 Apr 2022 00:35:55 GMT  
		Size: 4.3 MB (4264191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d745fee38250cce36d1723e6eb3964a525bb738eb2c82b501244732a881913`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbae97ea1f2eea13534851ba6f58745635c465f6dd61681051632a7cac4bc8c`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccf8a195bad2001e20b085a797b257c60b2e4020d738441e352b661525e5029`  
		Last Modified: Sat, 30 Apr 2022 00:36:30 GMT  
		Size: 252.4 MB (252383482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c7449338629d393daa386d56eda7c00568a57dd328cd7df0410b5e398458d`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9440733505277e8f3f7d4bc2ad385b06e37093582b77feeef90fbf8570dddf3c`  
		Last Modified: Sat, 30 Apr 2022 00:36:51 GMT  
		Size: 63.1 MB (63076164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8b76e35d4800cba2ffd96b6e5766991c5f6f8df302a89558162e2756996fac`  
		Last Modified: Sat, 30 Apr 2022 00:36:42 GMT  
		Size: 279.9 KB (279913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240a0f2f7118df62260d84e096be2a18536d017cef9a31f1ecdb65a6c2608eed`  
		Last Modified: Sat, 30 Apr 2022 00:36:53 GMT  
		Size: 67.0 MB (67001910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7faa7e77a0405102c184b835be4302b1e544dcf264e0d19ea9f3626032a270`  
		Last Modified: Sat, 30 Apr 2022 00:37:10 GMT  
		Size: 10.7 MB (10734993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot-bionic`

```console
$ docker pull ros@sha256:7ea13828785d507116d34792afc9dd2c805226ef4b3600671c1ec5c596d5146c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot-bionic` - linux; amd64

```console
$ docker pull ros@sha256:a28bc3f892f1dfeecae7a00ba6304b00add7a4f48d9ecc1357d7bd5a3f87a2d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448477280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec5677d8005df5c0680c12d81e6e284c12cbdf56cd93577cbf4d460cf52bd33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:12:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:16:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV ROS_DISTRO=melodic
# Fri, 22 Apr 2022 03:18:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:18:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:18:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:18:54 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:19:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:19:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:20:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:21:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d08ae4a50ec7a4071fcd259c6dc2b8f3219e66e5206c2f15ee781c4691a7699`  
		Last Modified: Fri, 22 Apr 2022 02:30:38 GMT  
		Size: 839.0 KB (838982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca35b07994f608387e199fa484cf0d3a586144538b7ea207fea47c25e64441b`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 4.9 MB (4872320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e99e7d92f7a9c84f55e914a1ad549e14ba4885ce72e1422955549eb8a42412`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda5797f8b0a501462dae5d9c7c7baa2ab56476067c48007d7f7d5f28e027821`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdb800ef4ebf782b8706d3ca51c5602217bfdaccffd3c87e146da0fd5b913a`  
		Last Modified: Fri, 22 Apr 2022 03:47:53 GMT  
		Size: 259.5 MB (259455669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1a8004d93ae4d2dcb4e49fb62c1ad152510f72453bd6d548075d99ffce4a72`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2772d37526d353480c40bc6613660a726bae949372e0b95ff5a4e9aef62d22cc`  
		Last Modified: Fri, 22 Apr 2022 03:48:13 GMT  
		Size: 70.2 MB (70241270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b2bccc87971a9fadd6a92eb4daea27c47e122f6de0c129f9cb64e2aa64019c`  
		Last Modified: Fri, 22 Apr 2022 03:48:03 GMT  
		Size: 279.1 KB (279107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f4d6dcfc3bd2fa9202d04bbd1d4f684046c0a525682228e9024af7ee3fee6`  
		Last Modified: Fri, 22 Apr 2022 03:48:15 GMT  
		Size: 75.0 MB (74994599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453ce09845a35fb485ffe49a62e58ecd3d528a9aeb7429bdf7fd6941e6eb3ffa`  
		Last Modified: Fri, 22 Apr 2022 03:48:30 GMT  
		Size: 11.1 MB (11083036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:1d14bd9194543ed4a9d9f0dd81dbc60b9e4ceb6ddf151a2e4a2a09cda63e5b6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 MB (396027305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063acd2980c8c66d21cb505f4234c799e9f46aa28de7caa2849f8448d946245a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:25 GMT
ADD file:9604e3641a386ec134596dd717862c2386c1b90009c0646b1773930f98949d9c in / 
# Fri, 29 Apr 2022 22:58:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:28:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:41 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:31:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:31:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:31:55 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:35:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:03ca5b55b2bdc3c68d23c18a88c099e2015c6bdcef6e3c43ca0bfb6aea0b032a`  
		Last Modified: Fri, 29 Apr 2022 23:02:31 GMT  
		Size: 22.3 MB (22300451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ab3231e4fbaccf7df6d1d44ef88608a6c1b716de9810c8e2ad6b7dcc9f5fc`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 840.2 KB (840158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f529e0e8ed7433413f39308a48052c609e82179d4d22b76f62189c616e5fe14`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 4.1 MB (4086200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59f023c86c2016dd149f7a89f71dc59cb35eeaf64c75eadba638336b28f6abd`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdf654803a8e788e4166c4bf287b5137ec541b313ce50e4d9401f0bd63fc8d`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa17f883dcf2090ca188521c82e8ecd78e6182c5c0af353b2dee9a1b0e0c44e`  
		Last Modified: Sat, 30 Apr 2022 00:53:38 GMT  
		Size: 238.9 MB (238937435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27e0b0ee020522ab3317cb8094bd430e3fb49425c99d1cfafe5284f0562f68`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c89127f2ab55d40e6d39537412903ef429801ea54d6baf3a6439a6bb01692f0`  
		Last Modified: Sat, 30 Apr 2022 00:54:21 GMT  
		Size: 54.7 MB (54710630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108adfc0916db7aeda7a39615caa2cee9b6fbe75cd66aa27a2ac82eaf1e6e9b9`  
		Last Modified: Sat, 30 Apr 2022 00:53:50 GMT  
		Size: 280.0 KB (279967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab1dc1feb0f323edf28a08fb0fcfc3796eb524ac698714b37837180467e312`  
		Last Modified: Sat, 30 Apr 2022 00:54:36 GMT  
		Size: 64.7 MB (64746523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b852a9e6f9b9db1a873f5d26b96fa8e2ec994256c7153e1ef272a96d26c60c`  
		Last Modified: Sat, 30 Apr 2022 00:54:59 GMT  
		Size: 10.1 MB (10123526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dc415320b59ed3eceb471c9a86f2fc6febaf558f3bcc16cc737987b61c97d90f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.3 MB (422317875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7546d28bc1ce4883d78a9030d968b5c8fc659fcd88fbf850437db6e51fdd5a57`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:15:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:15:31 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:15:32 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:15:33 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:16:57 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:16:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:17:00 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:17:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:17:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:18:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:18:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9119a950b820c04a3c9309fd9cd748b4a1c924ef00ac90dcd01791d857977923`  
		Last Modified: Sat, 30 Apr 2022 00:35:56 GMT  
		Size: 839.8 KB (839766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54865980d811f13a848975797615c6b0c5f21fed029eb255b5a1b3a0566900ec`  
		Last Modified: Sat, 30 Apr 2022 00:35:55 GMT  
		Size: 4.3 MB (4264191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d745fee38250cce36d1723e6eb3964a525bb738eb2c82b501244732a881913`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbae97ea1f2eea13534851ba6f58745635c465f6dd61681051632a7cac4bc8c`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccf8a195bad2001e20b085a797b257c60b2e4020d738441e352b661525e5029`  
		Last Modified: Sat, 30 Apr 2022 00:36:30 GMT  
		Size: 252.4 MB (252383482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c7449338629d393daa386d56eda7c00568a57dd328cd7df0410b5e398458d`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9440733505277e8f3f7d4bc2ad385b06e37093582b77feeef90fbf8570dddf3c`  
		Last Modified: Sat, 30 Apr 2022 00:36:51 GMT  
		Size: 63.1 MB (63076164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8b76e35d4800cba2ffd96b6e5766991c5f6f8df302a89558162e2756996fac`  
		Last Modified: Sat, 30 Apr 2022 00:36:42 GMT  
		Size: 279.9 KB (279913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240a0f2f7118df62260d84e096be2a18536d017cef9a31f1ecdb65a6c2608eed`  
		Last Modified: Sat, 30 Apr 2022 00:36:53 GMT  
		Size: 67.0 MB (67001910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7faa7e77a0405102c184b835be4302b1e544dcf264e0d19ea9f3626032a270`  
		Last Modified: Sat, 30 Apr 2022 00:37:10 GMT  
		Size: 10.7 MB (10734993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base`

```console
$ docker pull ros@sha256:1d906c5b1ed01e5f591674e4b18546348c54514b65abb70158b7e5ef337d45db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:b35e906f707bf988db588f95ca6370e62514d104a193a57b4632649a0d97b48c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.4 MB (437394244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5023ff407aa1e7f107544b46c999a8edce6403d120be868f5edb7d852da0eb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:12:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:16:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV ROS_DISTRO=melodic
# Fri, 22 Apr 2022 03:18:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:18:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:18:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:18:54 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:19:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:19:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:20:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d08ae4a50ec7a4071fcd259c6dc2b8f3219e66e5206c2f15ee781c4691a7699`  
		Last Modified: Fri, 22 Apr 2022 02:30:38 GMT  
		Size: 839.0 KB (838982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca35b07994f608387e199fa484cf0d3a586144538b7ea207fea47c25e64441b`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 4.9 MB (4872320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e99e7d92f7a9c84f55e914a1ad549e14ba4885ce72e1422955549eb8a42412`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda5797f8b0a501462dae5d9c7c7baa2ab56476067c48007d7f7d5f28e027821`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdb800ef4ebf782b8706d3ca51c5602217bfdaccffd3c87e146da0fd5b913a`  
		Last Modified: Fri, 22 Apr 2022 03:47:53 GMT  
		Size: 259.5 MB (259455669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1a8004d93ae4d2dcb4e49fb62c1ad152510f72453bd6d548075d99ffce4a72`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2772d37526d353480c40bc6613660a726bae949372e0b95ff5a4e9aef62d22cc`  
		Last Modified: Fri, 22 Apr 2022 03:48:13 GMT  
		Size: 70.2 MB (70241270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b2bccc87971a9fadd6a92eb4daea27c47e122f6de0c129f9cb64e2aa64019c`  
		Last Modified: Fri, 22 Apr 2022 03:48:03 GMT  
		Size: 279.1 KB (279107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f4d6dcfc3bd2fa9202d04bbd1d4f684046c0a525682228e9024af7ee3fee6`  
		Last Modified: Fri, 22 Apr 2022 03:48:15 GMT  
		Size: 75.0 MB (74994599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:1d881fbd22871cd711f2824e52ca0e22ea1759aa60e9b703b778f96d6d13928c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385903779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f99306b40951ca6357fdb1ee9046768a03bed48d10a058806e68a8476874069`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:25 GMT
ADD file:9604e3641a386ec134596dd717862c2386c1b90009c0646b1773930f98949d9c in / 
# Fri, 29 Apr 2022 22:58:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:28:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:41 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:31:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:31:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:31:55 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:03ca5b55b2bdc3c68d23c18a88c099e2015c6bdcef6e3c43ca0bfb6aea0b032a`  
		Last Modified: Fri, 29 Apr 2022 23:02:31 GMT  
		Size: 22.3 MB (22300451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ab3231e4fbaccf7df6d1d44ef88608a6c1b716de9810c8e2ad6b7dcc9f5fc`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 840.2 KB (840158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f529e0e8ed7433413f39308a48052c609e82179d4d22b76f62189c616e5fe14`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 4.1 MB (4086200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59f023c86c2016dd149f7a89f71dc59cb35eeaf64c75eadba638336b28f6abd`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdf654803a8e788e4166c4bf287b5137ec541b313ce50e4d9401f0bd63fc8d`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa17f883dcf2090ca188521c82e8ecd78e6182c5c0af353b2dee9a1b0e0c44e`  
		Last Modified: Sat, 30 Apr 2022 00:53:38 GMT  
		Size: 238.9 MB (238937435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27e0b0ee020522ab3317cb8094bd430e3fb49425c99d1cfafe5284f0562f68`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c89127f2ab55d40e6d39537412903ef429801ea54d6baf3a6439a6bb01692f0`  
		Last Modified: Sat, 30 Apr 2022 00:54:21 GMT  
		Size: 54.7 MB (54710630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108adfc0916db7aeda7a39615caa2cee9b6fbe75cd66aa27a2ac82eaf1e6e9b9`  
		Last Modified: Sat, 30 Apr 2022 00:53:50 GMT  
		Size: 280.0 KB (279967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab1dc1feb0f323edf28a08fb0fcfc3796eb524ac698714b37837180467e312`  
		Last Modified: Sat, 30 Apr 2022 00:54:36 GMT  
		Size: 64.7 MB (64746523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:86b3f38d9bc9cc4ee2d33234df5041dc6f3d66f36083940df940dbd204ce3207
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.6 MB (411582882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83530c05ad8de8ce3636161e25b23921e4b94ab77b64d3eaffeff2253a6625d1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:15:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:15:31 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:15:32 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:15:33 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:16:57 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:16:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:17:00 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:17:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:17:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:18:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9119a950b820c04a3c9309fd9cd748b4a1c924ef00ac90dcd01791d857977923`  
		Last Modified: Sat, 30 Apr 2022 00:35:56 GMT  
		Size: 839.8 KB (839766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54865980d811f13a848975797615c6b0c5f21fed029eb255b5a1b3a0566900ec`  
		Last Modified: Sat, 30 Apr 2022 00:35:55 GMT  
		Size: 4.3 MB (4264191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d745fee38250cce36d1723e6eb3964a525bb738eb2c82b501244732a881913`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbae97ea1f2eea13534851ba6f58745635c465f6dd61681051632a7cac4bc8c`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccf8a195bad2001e20b085a797b257c60b2e4020d738441e352b661525e5029`  
		Last Modified: Sat, 30 Apr 2022 00:36:30 GMT  
		Size: 252.4 MB (252383482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c7449338629d393daa386d56eda7c00568a57dd328cd7df0410b5e398458d`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9440733505277e8f3f7d4bc2ad385b06e37093582b77feeef90fbf8570dddf3c`  
		Last Modified: Sat, 30 Apr 2022 00:36:51 GMT  
		Size: 63.1 MB (63076164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8b76e35d4800cba2ffd96b6e5766991c5f6f8df302a89558162e2756996fac`  
		Last Modified: Sat, 30 Apr 2022 00:36:42 GMT  
		Size: 279.9 KB (279913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240a0f2f7118df62260d84e096be2a18536d017cef9a31f1ecdb65a6c2608eed`  
		Last Modified: Sat, 30 Apr 2022 00:36:53 GMT  
		Size: 67.0 MB (67001910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base-bionic`

```console
$ docker pull ros@sha256:1d906c5b1ed01e5f591674e4b18546348c54514b65abb70158b7e5ef337d45db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:b35e906f707bf988db588f95ca6370e62514d104a193a57b4632649a0d97b48c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.4 MB (437394244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5023ff407aa1e7f107544b46c999a8edce6403d120be868f5edb7d852da0eb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:12:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:16:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV ROS_DISTRO=melodic
# Fri, 22 Apr 2022 03:18:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:18:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:18:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:18:54 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:19:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:19:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:20:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d08ae4a50ec7a4071fcd259c6dc2b8f3219e66e5206c2f15ee781c4691a7699`  
		Last Modified: Fri, 22 Apr 2022 02:30:38 GMT  
		Size: 839.0 KB (838982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca35b07994f608387e199fa484cf0d3a586144538b7ea207fea47c25e64441b`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 4.9 MB (4872320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e99e7d92f7a9c84f55e914a1ad549e14ba4885ce72e1422955549eb8a42412`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda5797f8b0a501462dae5d9c7c7baa2ab56476067c48007d7f7d5f28e027821`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdb800ef4ebf782b8706d3ca51c5602217bfdaccffd3c87e146da0fd5b913a`  
		Last Modified: Fri, 22 Apr 2022 03:47:53 GMT  
		Size: 259.5 MB (259455669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1a8004d93ae4d2dcb4e49fb62c1ad152510f72453bd6d548075d99ffce4a72`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2772d37526d353480c40bc6613660a726bae949372e0b95ff5a4e9aef62d22cc`  
		Last Modified: Fri, 22 Apr 2022 03:48:13 GMT  
		Size: 70.2 MB (70241270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b2bccc87971a9fadd6a92eb4daea27c47e122f6de0c129f9cb64e2aa64019c`  
		Last Modified: Fri, 22 Apr 2022 03:48:03 GMT  
		Size: 279.1 KB (279107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f4d6dcfc3bd2fa9202d04bbd1d4f684046c0a525682228e9024af7ee3fee6`  
		Last Modified: Fri, 22 Apr 2022 03:48:15 GMT  
		Size: 75.0 MB (74994599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:1d881fbd22871cd711f2824e52ca0e22ea1759aa60e9b703b778f96d6d13928c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385903779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f99306b40951ca6357fdb1ee9046768a03bed48d10a058806e68a8476874069`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:25 GMT
ADD file:9604e3641a386ec134596dd717862c2386c1b90009c0646b1773930f98949d9c in / 
# Fri, 29 Apr 2022 22:58:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:28:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:41 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:31:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:31:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:31:55 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:03ca5b55b2bdc3c68d23c18a88c099e2015c6bdcef6e3c43ca0bfb6aea0b032a`  
		Last Modified: Fri, 29 Apr 2022 23:02:31 GMT  
		Size: 22.3 MB (22300451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ab3231e4fbaccf7df6d1d44ef88608a6c1b716de9810c8e2ad6b7dcc9f5fc`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 840.2 KB (840158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f529e0e8ed7433413f39308a48052c609e82179d4d22b76f62189c616e5fe14`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 4.1 MB (4086200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59f023c86c2016dd149f7a89f71dc59cb35eeaf64c75eadba638336b28f6abd`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdf654803a8e788e4166c4bf287b5137ec541b313ce50e4d9401f0bd63fc8d`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa17f883dcf2090ca188521c82e8ecd78e6182c5c0af353b2dee9a1b0e0c44e`  
		Last Modified: Sat, 30 Apr 2022 00:53:38 GMT  
		Size: 238.9 MB (238937435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27e0b0ee020522ab3317cb8094bd430e3fb49425c99d1cfafe5284f0562f68`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c89127f2ab55d40e6d39537412903ef429801ea54d6baf3a6439a6bb01692f0`  
		Last Modified: Sat, 30 Apr 2022 00:54:21 GMT  
		Size: 54.7 MB (54710630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108adfc0916db7aeda7a39615caa2cee9b6fbe75cd66aa27a2ac82eaf1e6e9b9`  
		Last Modified: Sat, 30 Apr 2022 00:53:50 GMT  
		Size: 280.0 KB (279967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab1dc1feb0f323edf28a08fb0fcfc3796eb524ac698714b37837180467e312`  
		Last Modified: Sat, 30 Apr 2022 00:54:36 GMT  
		Size: 64.7 MB (64746523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:86b3f38d9bc9cc4ee2d33234df5041dc6f3d66f36083940df940dbd204ce3207
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.6 MB (411582882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83530c05ad8de8ce3636161e25b23921e4b94ab77b64d3eaffeff2253a6625d1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:15:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:15:31 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:15:32 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:15:33 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:16:57 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:16:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:17:00 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:17:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:17:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:18:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9119a950b820c04a3c9309fd9cd748b4a1c924ef00ac90dcd01791d857977923`  
		Last Modified: Sat, 30 Apr 2022 00:35:56 GMT  
		Size: 839.8 KB (839766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54865980d811f13a848975797615c6b0c5f21fed029eb255b5a1b3a0566900ec`  
		Last Modified: Sat, 30 Apr 2022 00:35:55 GMT  
		Size: 4.3 MB (4264191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d745fee38250cce36d1723e6eb3964a525bb738eb2c82b501244732a881913`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbae97ea1f2eea13534851ba6f58745635c465f6dd61681051632a7cac4bc8c`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccf8a195bad2001e20b085a797b257c60b2e4020d738441e352b661525e5029`  
		Last Modified: Sat, 30 Apr 2022 00:36:30 GMT  
		Size: 252.4 MB (252383482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c7449338629d393daa386d56eda7c00568a57dd328cd7df0410b5e398458d`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9440733505277e8f3f7d4bc2ad385b06e37093582b77feeef90fbf8570dddf3c`  
		Last Modified: Sat, 30 Apr 2022 00:36:51 GMT  
		Size: 63.1 MB (63076164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8b76e35d4800cba2ffd96b6e5766991c5f6f8df302a89558162e2756996fac`  
		Last Modified: Sat, 30 Apr 2022 00:36:42 GMT  
		Size: 279.9 KB (279913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240a0f2f7118df62260d84e096be2a18536d017cef9a31f1ecdb65a6c2608eed`  
		Last Modified: Sat, 30 Apr 2022 00:36:53 GMT  
		Size: 67.0 MB (67001910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:b05febfdd20e29d9ab4c8c84d24bc620d87fd2be146a65e7e5d718c78f6a764c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:df25ed094291a1fb6871268725546bdaec1755a6adcc3e01006291f069ed4c77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291879268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5a74700fa30db918ce7f3f12af76aa76fd9a048ff3df2d2598696f78ffe3f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:12:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:16:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV ROS_DISTRO=melodic
# Fri, 22 Apr 2022 03:18:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:18:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:18:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:18:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d08ae4a50ec7a4071fcd259c6dc2b8f3219e66e5206c2f15ee781c4691a7699`  
		Last Modified: Fri, 22 Apr 2022 02:30:38 GMT  
		Size: 839.0 KB (838982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca35b07994f608387e199fa484cf0d3a586144538b7ea207fea47c25e64441b`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 4.9 MB (4872320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e99e7d92f7a9c84f55e914a1ad549e14ba4885ce72e1422955549eb8a42412`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda5797f8b0a501462dae5d9c7c7baa2ab56476067c48007d7f7d5f28e027821`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdb800ef4ebf782b8706d3ca51c5602217bfdaccffd3c87e146da0fd5b913a`  
		Last Modified: Fri, 22 Apr 2022 03:47:53 GMT  
		Size: 259.5 MB (259455669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1a8004d93ae4d2dcb4e49fb62c1ad152510f72453bd6d548075d99ffce4a72`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:acf689ff37ed4dca35a9ec4f405a80509c2ad86a4a8ed564049ca49476567f19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266166659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd942724ced67c41e9e3a662aad99a1ecc5b0d8b27170dce8a888bb6fc63e01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:25 GMT
ADD file:9604e3641a386ec134596dd717862c2386c1b90009c0646b1773930f98949d9c in / 
# Fri, 29 Apr 2022 22:58:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:28:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:41 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:31:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:31:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:31:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:03ca5b55b2bdc3c68d23c18a88c099e2015c6bdcef6e3c43ca0bfb6aea0b032a`  
		Last Modified: Fri, 29 Apr 2022 23:02:31 GMT  
		Size: 22.3 MB (22300451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ab3231e4fbaccf7df6d1d44ef88608a6c1b716de9810c8e2ad6b7dcc9f5fc`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 840.2 KB (840158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f529e0e8ed7433413f39308a48052c609e82179d4d22b76f62189c616e5fe14`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 4.1 MB (4086200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59f023c86c2016dd149f7a89f71dc59cb35eeaf64c75eadba638336b28f6abd`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdf654803a8e788e4166c4bf287b5137ec541b313ce50e4d9401f0bd63fc8d`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa17f883dcf2090ca188521c82e8ecd78e6182c5c0af353b2dee9a1b0e0c44e`  
		Last Modified: Sat, 30 Apr 2022 00:53:38 GMT  
		Size: 238.9 MB (238937435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27e0b0ee020522ab3317cb8094bd430e3fb49425c99d1cfafe5284f0562f68`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f80bd2021f4064e73fa6c8288e28e79addf215f802688837c08c207a8391edae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281224895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f5d03985df014cb9760c418e73f445759afa99fac7fa0c6bb83780b33d83ae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:15:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:15:31 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:15:32 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:15:33 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:16:57 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:16:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:17:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9119a950b820c04a3c9309fd9cd748b4a1c924ef00ac90dcd01791d857977923`  
		Last Modified: Sat, 30 Apr 2022 00:35:56 GMT  
		Size: 839.8 KB (839766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54865980d811f13a848975797615c6b0c5f21fed029eb255b5a1b3a0566900ec`  
		Last Modified: Sat, 30 Apr 2022 00:35:55 GMT  
		Size: 4.3 MB (4264191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d745fee38250cce36d1723e6eb3964a525bb738eb2c82b501244732a881913`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbae97ea1f2eea13534851ba6f58745635c465f6dd61681051632a7cac4bc8c`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccf8a195bad2001e20b085a797b257c60b2e4020d738441e352b661525e5029`  
		Last Modified: Sat, 30 Apr 2022 00:36:30 GMT  
		Size: 252.4 MB (252383482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c7449338629d393daa386d56eda7c00568a57dd328cd7df0410b5e398458d`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core-bionic`

```console
$ docker pull ros@sha256:b05febfdd20e29d9ab4c8c84d24bc620d87fd2be146a65e7e5d718c78f6a764c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:df25ed094291a1fb6871268725546bdaec1755a6adcc3e01006291f069ed4c77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291879268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5a74700fa30db918ce7f3f12af76aa76fd9a048ff3df2d2598696f78ffe3f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:12:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:16:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV ROS_DISTRO=melodic
# Fri, 22 Apr 2022 03:18:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:18:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:18:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:18:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d08ae4a50ec7a4071fcd259c6dc2b8f3219e66e5206c2f15ee781c4691a7699`  
		Last Modified: Fri, 22 Apr 2022 02:30:38 GMT  
		Size: 839.0 KB (838982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca35b07994f608387e199fa484cf0d3a586144538b7ea207fea47c25e64441b`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 4.9 MB (4872320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e99e7d92f7a9c84f55e914a1ad549e14ba4885ce72e1422955549eb8a42412`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda5797f8b0a501462dae5d9c7c7baa2ab56476067c48007d7f7d5f28e027821`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdb800ef4ebf782b8706d3ca51c5602217bfdaccffd3c87e146da0fd5b913a`  
		Last Modified: Fri, 22 Apr 2022 03:47:53 GMT  
		Size: 259.5 MB (259455669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1a8004d93ae4d2dcb4e49fb62c1ad152510f72453bd6d548075d99ffce4a72`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:acf689ff37ed4dca35a9ec4f405a80509c2ad86a4a8ed564049ca49476567f19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266166659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd942724ced67c41e9e3a662aad99a1ecc5b0d8b27170dce8a888bb6fc63e01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:25 GMT
ADD file:9604e3641a386ec134596dd717862c2386c1b90009c0646b1773930f98949d9c in / 
# Fri, 29 Apr 2022 22:58:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:28:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:41 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:31:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:31:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:31:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:03ca5b55b2bdc3c68d23c18a88c099e2015c6bdcef6e3c43ca0bfb6aea0b032a`  
		Last Modified: Fri, 29 Apr 2022 23:02:31 GMT  
		Size: 22.3 MB (22300451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ab3231e4fbaccf7df6d1d44ef88608a6c1b716de9810c8e2ad6b7dcc9f5fc`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 840.2 KB (840158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f529e0e8ed7433413f39308a48052c609e82179d4d22b76f62189c616e5fe14`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 4.1 MB (4086200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59f023c86c2016dd149f7a89f71dc59cb35eeaf64c75eadba638336b28f6abd`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdf654803a8e788e4166c4bf287b5137ec541b313ce50e4d9401f0bd63fc8d`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa17f883dcf2090ca188521c82e8ecd78e6182c5c0af353b2dee9a1b0e0c44e`  
		Last Modified: Sat, 30 Apr 2022 00:53:38 GMT  
		Size: 238.9 MB (238937435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27e0b0ee020522ab3317cb8094bd430e3fb49425c99d1cfafe5284f0562f68`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f80bd2021f4064e73fa6c8288e28e79addf215f802688837c08c207a8391edae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281224895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f5d03985df014cb9760c418e73f445759afa99fac7fa0c6bb83780b33d83ae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:15:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:15:31 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:15:32 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:15:33 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:16:57 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:16:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:17:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9119a950b820c04a3c9309fd9cd748b4a1c924ef00ac90dcd01791d857977923`  
		Last Modified: Sat, 30 Apr 2022 00:35:56 GMT  
		Size: 839.8 KB (839766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54865980d811f13a848975797615c6b0c5f21fed029eb255b5a1b3a0566900ec`  
		Last Modified: Sat, 30 Apr 2022 00:35:55 GMT  
		Size: 4.3 MB (4264191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d745fee38250cce36d1723e6eb3964a525bb738eb2c82b501244732a881913`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbae97ea1f2eea13534851ba6f58745635c465f6dd61681051632a7cac4bc8c`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccf8a195bad2001e20b085a797b257c60b2e4020d738441e352b661525e5029`  
		Last Modified: Sat, 30 Apr 2022 00:36:30 GMT  
		Size: 252.4 MB (252383482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c7449338629d393daa386d56eda7c00568a57dd328cd7df0410b5e398458d`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:8076aa2a1acb8782dafa600b60ac18d61240a4214a5780482938a7f82fadf1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:62e0f0bf5659f14e229c216fa8b63e1ee9d2ca697ad8a5471bfe157b9957efad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.0 MB (343021947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fd733d2da3cc8a934cace2a21423ed6c30c11016a16c493a06b9b3f312039b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:26:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:26:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 22 Apr 2022 03:28:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:28 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:28:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:28:28 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:28:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:29:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a113e5bfc6a41a0f6d9401ad372ec451407fd55bff2862a2023976889322604`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c65e0abed62803e4b89b3aa305b9b4f0262f25940675f4b8fa7ad7bb9f01a9`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90362b1253ae0b3ad24a095a66a71c2437d714ea43529f9af6cf1f9ee26e7d6`  
		Last Modified: Fri, 22 Apr 2022 03:50:08 GMT  
		Size: 176.9 MB (176875279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424da76ce8b30c3127dada4dbec6e2374d087e7e2b0951038c14545d05b87cc7`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fb42a12f184b9b6ad2c9b99a06bdfba4eb6b8c9d97cb8eb224a20386496a4a`  
		Last Modified: Fri, 22 Apr 2022 03:50:26 GMT  
		Size: 50.9 MB (50933515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9199749d47db40394c6f583da9bf1786de2f23b56c00534df5ab66d5e7ff7`  
		Last Modified: Fri, 22 Apr 2022 03:50:18 GMT  
		Size: 314.8 KB (314824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647f59c451e50b55164b1df4f395c7658e7583fbee1cb10ac1d0c4231a7abf39`  
		Last Modified: Fri, 22 Apr 2022 03:50:30 GMT  
		Size: 79.6 MB (79602400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:4fde0076ff1a895147ac2024675ff31ba8d303480a76aefe0c0fe4f4da840e9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288657790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5ed39b32a22763a4e60b12651dc742897d6eb060f5ca112244773945a49537`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:39:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:39:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:39:27 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:41:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:41:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:41:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:41:54 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:42:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:42:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:43:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788bc5672cc0168109c03624bd9c0486dc436058f2ef6bd58aa20183c16330dc`  
		Last Modified: Sat, 30 Apr 2022 00:58:13 GMT  
		Size: 1.2 MB (1182235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f050457c70471d51e645d9056bf76421874818d4dcb3c2d9167cc4c7c59f1`  
		Last Modified: Sat, 30 Apr 2022 00:58:12 GMT  
		Size: 4.7 MB (4676780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf102ed76521e041cbd91514e5b37b5e35694a768c899009f51ba52983b3d4d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b493804b771bd37872f55298ac60b41ddb64199e41c6cbd02a5bd78b13f2e17`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf0953c9382836b5d5e61b0e28e2f23c2431ef644d2ddc2d4a5bffbadff9b15`  
		Last Modified: Sat, 30 Apr 2022 01:00:16 GMT  
		Size: 157.4 MB (157423830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5012cfe0e5842d29eb696b50431a424ba513d5c1554715f456713b05532596d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faae41d6b1935d771645ed3646ee3838471dd083a2f92d29b121834b2a712fab`  
		Last Modified: Sat, 30 Apr 2022 01:00:51 GMT  
		Size: 40.5 MB (40501299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dea40ff78bf9cdbb2384fb35a4bb7127dac17db236f078dcc3d9de59148a06`  
		Last Modified: Sat, 30 Apr 2022 01:00:28 GMT  
		Size: 315.7 KB (315673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d375b84b753999e87a8ed0b405d15fd34c522a1f831031dad0599a36d2f84491`  
		Last Modified: Sat, 30 Apr 2022 01:01:07 GMT  
		Size: 60.5 MB (60481908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0947defb184c2b20e8ecc6e46de7f5cea05f9153f501b7de2631711c44034219
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322027098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901688928341e7b725a0f474197821ddabbb0e5966213c9a6ac648fe518fb26d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:20:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:20:44 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:20:45 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:20:46 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:21:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:21:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:21:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:22:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:22:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:22:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1a842c5f450bf757d4efae2d77d0b3637b2f76a02794282656ef03f45e1f1`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e026a627567dcb9c599ab69248d8c084364d4df165bc5257f923c2709f493ab`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527d513e9f97294799a5126bcf25e7f7b73ff93ceb27622f1b3838d580fcde9`  
		Last Modified: Sat, 30 Apr 2022 00:38:47 GMT  
		Size: 171.3 MB (171293442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc48433487f9d4e46329a07c1247899a65bab17103180e95e2da17c25f686d5`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9776aee7c7d20a2a679ec671b31130800b8048248586171aa655e89df4b91f4a`  
		Last Modified: Sat, 30 Apr 2022 00:39:05 GMT  
		Size: 45.0 MB (44988594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890ccdeaa4aedd37f00917bbddd6365cd5dc7f1746a97c5520462003cccd6b3a`  
		Last Modified: Sat, 30 Apr 2022 00:38:58 GMT  
		Size: 315.6 KB (315611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8b7144add68575402586085ccee53c0002fd54ef7e2813f589098a7cce933e`  
		Last Modified: Sat, 30 Apr 2022 00:39:09 GMT  
		Size: 71.8 MB (71753617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:6a30b32a6148b4c46af17660b155547744a7314665c84562020fb315b2381fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:ab69286a981b4c72f6cfc5c3b5b915d7976c67edf8350649071ecc6a1855f920
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.0 MB (834986866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4e4bba5021550a163834d0d889b8f07daafecdaf9de04b4e27ca6f13665025`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:26:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:26:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 22 Apr 2022 03:28:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:28 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:28:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:28:28 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:28:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:29:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a113e5bfc6a41a0f6d9401ad372ec451407fd55bff2862a2023976889322604`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c65e0abed62803e4b89b3aa305b9b4f0262f25940675f4b8fa7ad7bb9f01a9`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90362b1253ae0b3ad24a095a66a71c2437d714ea43529f9af6cf1f9ee26e7d6`  
		Last Modified: Fri, 22 Apr 2022 03:50:08 GMT  
		Size: 176.9 MB (176875279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424da76ce8b30c3127dada4dbec6e2374d087e7e2b0951038c14545d05b87cc7`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fb42a12f184b9b6ad2c9b99a06bdfba4eb6b8c9d97cb8eb224a20386496a4a`  
		Last Modified: Fri, 22 Apr 2022 03:50:26 GMT  
		Size: 50.9 MB (50933515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9199749d47db40394c6f583da9bf1786de2f23b56c00534df5ab66d5e7ff7`  
		Last Modified: Fri, 22 Apr 2022 03:50:18 GMT  
		Size: 314.8 KB (314824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647f59c451e50b55164b1df4f395c7658e7583fbee1cb10ac1d0c4231a7abf39`  
		Last Modified: Fri, 22 Apr 2022 03:50:30 GMT  
		Size: 79.6 MB (79602400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92599f66529a813a6e3e49ab12cf914bb5e22f6f03eff38e96f0b8cb317b249`  
		Last Modified: Fri, 22 Apr 2022 03:52:11 GMT  
		Size: 492.0 MB (491964919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:732a9ce14f825cacefc32886651b9a23180a0f46ef47874a17d32205450628b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.6 MB (725587279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce21f86b3137fa28a954f09289263b797c9a14a186dc78e041997dbdbfbc4e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:39:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:39:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:39:27 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:41:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:41:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:41:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:41:54 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:42:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:42:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:43:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:49:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788bc5672cc0168109c03624bd9c0486dc436058f2ef6bd58aa20183c16330dc`  
		Last Modified: Sat, 30 Apr 2022 00:58:13 GMT  
		Size: 1.2 MB (1182235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f050457c70471d51e645d9056bf76421874818d4dcb3c2d9167cc4c7c59f1`  
		Last Modified: Sat, 30 Apr 2022 00:58:12 GMT  
		Size: 4.7 MB (4676780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf102ed76521e041cbd91514e5b37b5e35694a768c899009f51ba52983b3d4d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b493804b771bd37872f55298ac60b41ddb64199e41c6cbd02a5bd78b13f2e17`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf0953c9382836b5d5e61b0e28e2f23c2431ef644d2ddc2d4a5bffbadff9b15`  
		Last Modified: Sat, 30 Apr 2022 01:00:16 GMT  
		Size: 157.4 MB (157423830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5012cfe0e5842d29eb696b50431a424ba513d5c1554715f456713b05532596d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faae41d6b1935d771645ed3646ee3838471dd083a2f92d29b121834b2a712fab`  
		Last Modified: Sat, 30 Apr 2022 01:00:51 GMT  
		Size: 40.5 MB (40501299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dea40ff78bf9cdbb2384fb35a4bb7127dac17db236f078dcc3d9de59148a06`  
		Last Modified: Sat, 30 Apr 2022 01:00:28 GMT  
		Size: 315.7 KB (315673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d375b84b753999e87a8ed0b405d15fd34c522a1f831031dad0599a36d2f84491`  
		Last Modified: Sat, 30 Apr 2022 01:01:07 GMT  
		Size: 60.5 MB (60481908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9dc52f71902d762b0a95cfa3c0abfc4606212d101bdb1102c56046907805949`  
		Last Modified: Sat, 30 Apr 2022 01:06:14 GMT  
		Size: 436.9 MB (436929489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:37cba6b7529f06b540518f6797f71750191abcc4d1839510c6b82cf8d9d314b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.5 MB (784517811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081f48272fe65c5d6151746f56f2f4d30a39cbbb9177a73868d875d2ca4e4533`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:20:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:20:44 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:20:45 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:20:46 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:21:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:21:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:21:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:22:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:22:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:22:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1a842c5f450bf757d4efae2d77d0b3637b2f76a02794282656ef03f45e1f1`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e026a627567dcb9c599ab69248d8c084364d4df165bc5257f923c2709f493ab`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527d513e9f97294799a5126bcf25e7f7b73ff93ceb27622f1b3838d580fcde9`  
		Last Modified: Sat, 30 Apr 2022 00:38:47 GMT  
		Size: 171.3 MB (171293442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc48433487f9d4e46329a07c1247899a65bab17103180e95e2da17c25f686d5`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9776aee7c7d20a2a679ec671b31130800b8048248586171aa655e89df4b91f4a`  
		Last Modified: Sat, 30 Apr 2022 00:39:05 GMT  
		Size: 45.0 MB (44988594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890ccdeaa4aedd37f00917bbddd6365cd5dc7f1746a97c5520462003cccd6b3a`  
		Last Modified: Sat, 30 Apr 2022 00:38:58 GMT  
		Size: 315.6 KB (315611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8b7144add68575402586085ccee53c0002fd54ef7e2813f589098a7cce933e`  
		Last Modified: Sat, 30 Apr 2022 00:39:09 GMT  
		Size: 71.8 MB (71753617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f15a8b59ed9e76d31ca016fba28201e39c0b6f21f48212025ce82ac5a9162a0`  
		Last Modified: Sat, 30 Apr 2022 00:40:47 GMT  
		Size: 462.5 MB (462490713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:8ad82eff31eaa1d0bf1d9e9e564bcf1d6f001124a6c768ff17ad74f35b91e0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:25bc6ce5fdfefee48e015f60e641910a0142999ad6e4332ae4bf3818dc8bf497
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **951.5 MB (951517214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9764e88e4b84531e3e1aa2b08bb398c9693f5be42ee0743dfe1a553040854f3d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:37:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:37:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 20 Apr 2022 17:37:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 20 Apr 2022 17:37:26 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 17:37:26 GMT
ENV LC_ALL=C.UTF-8
# Wed, 20 Apr 2022 17:37:26 GMT
ENV ROS_DISTRO=noetic
# Wed, 20 Apr 2022 17:38:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:38:27 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 20 Apr 2022 17:38:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 20 Apr 2022 17:38:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:38:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:39:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 20 Apr 2022 17:39:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:41:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20546aaa06f50802eafdb39e7339d4cb6230c7a1aff32a53c46d1fcfed8f2dd5`  
		Last Modified: Wed, 20 Apr 2022 17:43:00 GMT  
		Size: 10.9 MB (10892097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abde7f24de9cf0bbb2249385441601015b239338b7901eae3402cb42a98c589`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afac4f8c5429cab550330c262feb633f708f9eda06ab0962fa784c88a9c3459a`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8609835955c8073fb8ee41d1c9ebb686c08c5a154f81dc42e1ee92614d6e430`  
		Last Modified: Wed, 20 Apr 2022 17:43:31 GMT  
		Size: 239.2 MB (239162184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb06026309bf4ee95de3a56281f392cddaad08a74c5056617cee6a3cbad0840`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757a381d58433d12adbc8267c4306c48e05ceab27e9b7180e6ab5153115398a9`  
		Last Modified: Wed, 20 Apr 2022 17:43:51 GMT  
		Size: 86.6 MB (86566693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2d2e540aad82640f395c83b534034224c4743c463281a9308bcd39e755a9a5`  
		Last Modified: Wed, 20 Apr 2022 17:43:39 GMT  
		Size: 309.3 KB (309290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc64f783db31ecba0dea771f5c67d54898bd9e111176ecd00620deaa53fef6e`  
		Last Modified: Wed, 20 Apr 2022 17:43:49 GMT  
		Size: 76.0 MB (75976251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a6c84da7010552c141b5d0c478700dd9362ce1ff0a16729b967a26cfe6b941`  
		Last Modified: Wed, 20 Apr 2022 17:45:22 GMT  
		Size: 488.2 MB (488171305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:25b6fe2a0e3dfdddf6d36c32b27206b68b4ae4cb544a4fda27922baa7ef31bbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 MB (867713663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcf21208468124b3285b34c0276748127e9ae21c28c8082af342ed7ce0e62b0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:10:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:10:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 20 Apr 2022 12:10:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 20 Apr 2022 12:10:22 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:10:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 20 Apr 2022 12:10:24 GMT
ENV ROS_DISTRO=noetic
# Wed, 20 Apr 2022 12:11:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:11:39 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 20 Apr 2022 12:11:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 20 Apr 2022 12:11:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:12:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:12:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 20 Apr 2022 12:13:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:16:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3957d218911547e664ee734939dc71ad089b29ed94b50f538786d667373e1ce5`  
		Last Modified: Wed, 20 Apr 2022 12:18:50 GMT  
		Size: 10.7 MB (10688204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2c217f5a5971a62fad5aac5564915eaf89c57b2110a7751a364f5a0de02dd7`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4a549feaf8502a671617c04bc2c2a084e6374b096bd615bebf4d2b3278be0a`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a05822887f56bc9d0b9364d7c755b5baee6c94b00f61dd5c41b4c2392919797`  
		Last Modified: Wed, 20 Apr 2022 12:19:19 GMT  
		Size: 184.4 MB (184369896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8501994f2ad5e8e01905fad8c5f1491a035971eab743a788c7208cf18255c4e`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd36c64b99b0defab15ab0ce0f85dbf6fbab02bd969287c79becce5d9293059c`  
		Last Modified: Wed, 20 Apr 2022 12:19:38 GMT  
		Size: 84.4 MB (84352350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0359920e3958bfbe6523bec5a0c24d8479e58e68ab41c3c437aa9806e83e776e`  
		Last Modified: Wed, 20 Apr 2022 12:19:27 GMT  
		Size: 309.2 KB (309235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e22341ca497d2ab03ede7e0d29948509d06168bfff83be501fc2c9fb1499be`  
		Last Modified: Wed, 20 Apr 2022 12:19:37 GMT  
		Size: 73.9 MB (73865013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4fe6b32b74a770b835d7ef94154e208ca4d9d3c236f06b6e38fe5a5a75ce`  
		Last Modified: Wed, 20 Apr 2022 12:21:03 GMT  
		Size: 464.9 MB (464898859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:6a30b32a6148b4c46af17660b155547744a7314665c84562020fb315b2381fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:ab69286a981b4c72f6cfc5c3b5b915d7976c67edf8350649071ecc6a1855f920
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.0 MB (834986866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4e4bba5021550a163834d0d889b8f07daafecdaf9de04b4e27ca6f13665025`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:26:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:26:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 22 Apr 2022 03:28:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:28 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:28:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:28:28 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:28:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:29:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a113e5bfc6a41a0f6d9401ad372ec451407fd55bff2862a2023976889322604`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c65e0abed62803e4b89b3aa305b9b4f0262f25940675f4b8fa7ad7bb9f01a9`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90362b1253ae0b3ad24a095a66a71c2437d714ea43529f9af6cf1f9ee26e7d6`  
		Last Modified: Fri, 22 Apr 2022 03:50:08 GMT  
		Size: 176.9 MB (176875279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424da76ce8b30c3127dada4dbec6e2374d087e7e2b0951038c14545d05b87cc7`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fb42a12f184b9b6ad2c9b99a06bdfba4eb6b8c9d97cb8eb224a20386496a4a`  
		Last Modified: Fri, 22 Apr 2022 03:50:26 GMT  
		Size: 50.9 MB (50933515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9199749d47db40394c6f583da9bf1786de2f23b56c00534df5ab66d5e7ff7`  
		Last Modified: Fri, 22 Apr 2022 03:50:18 GMT  
		Size: 314.8 KB (314824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647f59c451e50b55164b1df4f395c7658e7583fbee1cb10ac1d0c4231a7abf39`  
		Last Modified: Fri, 22 Apr 2022 03:50:30 GMT  
		Size: 79.6 MB (79602400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92599f66529a813a6e3e49ab12cf914bb5e22f6f03eff38e96f0b8cb317b249`  
		Last Modified: Fri, 22 Apr 2022 03:52:11 GMT  
		Size: 492.0 MB (491964919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:732a9ce14f825cacefc32886651b9a23180a0f46ef47874a17d32205450628b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.6 MB (725587279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce21f86b3137fa28a954f09289263b797c9a14a186dc78e041997dbdbfbc4e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:39:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:39:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:39:27 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:41:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:41:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:41:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:41:54 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:42:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:42:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:43:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:49:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788bc5672cc0168109c03624bd9c0486dc436058f2ef6bd58aa20183c16330dc`  
		Last Modified: Sat, 30 Apr 2022 00:58:13 GMT  
		Size: 1.2 MB (1182235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f050457c70471d51e645d9056bf76421874818d4dcb3c2d9167cc4c7c59f1`  
		Last Modified: Sat, 30 Apr 2022 00:58:12 GMT  
		Size: 4.7 MB (4676780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf102ed76521e041cbd91514e5b37b5e35694a768c899009f51ba52983b3d4d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b493804b771bd37872f55298ac60b41ddb64199e41c6cbd02a5bd78b13f2e17`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf0953c9382836b5d5e61b0e28e2f23c2431ef644d2ddc2d4a5bffbadff9b15`  
		Last Modified: Sat, 30 Apr 2022 01:00:16 GMT  
		Size: 157.4 MB (157423830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5012cfe0e5842d29eb696b50431a424ba513d5c1554715f456713b05532596d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faae41d6b1935d771645ed3646ee3838471dd083a2f92d29b121834b2a712fab`  
		Last Modified: Sat, 30 Apr 2022 01:00:51 GMT  
		Size: 40.5 MB (40501299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dea40ff78bf9cdbb2384fb35a4bb7127dac17db236f078dcc3d9de59148a06`  
		Last Modified: Sat, 30 Apr 2022 01:00:28 GMT  
		Size: 315.7 KB (315673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d375b84b753999e87a8ed0b405d15fd34c522a1f831031dad0599a36d2f84491`  
		Last Modified: Sat, 30 Apr 2022 01:01:07 GMT  
		Size: 60.5 MB (60481908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9dc52f71902d762b0a95cfa3c0abfc4606212d101bdb1102c56046907805949`  
		Last Modified: Sat, 30 Apr 2022 01:06:14 GMT  
		Size: 436.9 MB (436929489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:37cba6b7529f06b540518f6797f71750191abcc4d1839510c6b82cf8d9d314b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.5 MB (784517811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081f48272fe65c5d6151746f56f2f4d30a39cbbb9177a73868d875d2ca4e4533`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:20:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:20:44 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:20:45 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:20:46 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:21:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:21:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:21:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:22:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:22:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:22:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1a842c5f450bf757d4efae2d77d0b3637b2f76a02794282656ef03f45e1f1`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e026a627567dcb9c599ab69248d8c084364d4df165bc5257f923c2709f493ab`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527d513e9f97294799a5126bcf25e7f7b73ff93ceb27622f1b3838d580fcde9`  
		Last Modified: Sat, 30 Apr 2022 00:38:47 GMT  
		Size: 171.3 MB (171293442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc48433487f9d4e46329a07c1247899a65bab17103180e95e2da17c25f686d5`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9776aee7c7d20a2a679ec671b31130800b8048248586171aa655e89df4b91f4a`  
		Last Modified: Sat, 30 Apr 2022 00:39:05 GMT  
		Size: 45.0 MB (44988594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890ccdeaa4aedd37f00917bbddd6365cd5dc7f1746a97c5520462003cccd6b3a`  
		Last Modified: Sat, 30 Apr 2022 00:38:58 GMT  
		Size: 315.6 KB (315611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8b7144add68575402586085ccee53c0002fd54ef7e2813f589098a7cce933e`  
		Last Modified: Sat, 30 Apr 2022 00:39:09 GMT  
		Size: 71.8 MB (71753617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f15a8b59ed9e76d31ca016fba28201e39c0b6f21f48212025ce82ac5a9162a0`  
		Last Modified: Sat, 30 Apr 2022 00:40:47 GMT  
		Size: 462.5 MB (462490713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:baa43b9b599444bff925df05e70a49cdb0a17aeaf7f9cfd8e86796ef545f38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:82adffa092e98d53cac94a9ecb55ba7569efc8f0f5d22fa619f93ce70eb50a80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358880748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e0ca8e38ae15069727b4c1507435dfe3fb53c865c6ab323f807fd32afdec7f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:26:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:26:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 22 Apr 2022 03:28:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:28 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:28:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:28:28 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:28:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:29:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a113e5bfc6a41a0f6d9401ad372ec451407fd55bff2862a2023976889322604`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c65e0abed62803e4b89b3aa305b9b4f0262f25940675f4b8fa7ad7bb9f01a9`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90362b1253ae0b3ad24a095a66a71c2437d714ea43529f9af6cf1f9ee26e7d6`  
		Last Modified: Fri, 22 Apr 2022 03:50:08 GMT  
		Size: 176.9 MB (176875279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424da76ce8b30c3127dada4dbec6e2374d087e7e2b0951038c14545d05b87cc7`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fb42a12f184b9b6ad2c9b99a06bdfba4eb6b8c9d97cb8eb224a20386496a4a`  
		Last Modified: Fri, 22 Apr 2022 03:50:26 GMT  
		Size: 50.9 MB (50933515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9199749d47db40394c6f583da9bf1786de2f23b56c00534df5ab66d5e7ff7`  
		Last Modified: Fri, 22 Apr 2022 03:50:18 GMT  
		Size: 314.8 KB (314824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647f59c451e50b55164b1df4f395c7658e7583fbee1cb10ac1d0c4231a7abf39`  
		Last Modified: Fri, 22 Apr 2022 03:50:30 GMT  
		Size: 79.6 MB (79602400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f093d22dbe5877606fa8a0bb7ab4ff9f764a797720db05f3891f492ba89135`  
		Last Modified: Fri, 22 Apr 2022 03:50:46 GMT  
		Size: 15.9 MB (15858801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:925e6735d0b0a8bd360ae8b6f9bb3430e72444f8460bc6bd09c456b484b52f57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302722275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd50d304cce6369dd44fe927243dae8e7814cc4f7542f0689e49734ffc263139`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:39:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:39:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:39:27 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:41:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:41:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:41:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:41:54 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:42:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:42:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:43:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:44:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788bc5672cc0168109c03624bd9c0486dc436058f2ef6bd58aa20183c16330dc`  
		Last Modified: Sat, 30 Apr 2022 00:58:13 GMT  
		Size: 1.2 MB (1182235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f050457c70471d51e645d9056bf76421874818d4dcb3c2d9167cc4c7c59f1`  
		Last Modified: Sat, 30 Apr 2022 00:58:12 GMT  
		Size: 4.7 MB (4676780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf102ed76521e041cbd91514e5b37b5e35694a768c899009f51ba52983b3d4d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b493804b771bd37872f55298ac60b41ddb64199e41c6cbd02a5bd78b13f2e17`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf0953c9382836b5d5e61b0e28e2f23c2431ef644d2ddc2d4a5bffbadff9b15`  
		Last Modified: Sat, 30 Apr 2022 01:00:16 GMT  
		Size: 157.4 MB (157423830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5012cfe0e5842d29eb696b50431a424ba513d5c1554715f456713b05532596d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faae41d6b1935d771645ed3646ee3838471dd083a2f92d29b121834b2a712fab`  
		Last Modified: Sat, 30 Apr 2022 01:00:51 GMT  
		Size: 40.5 MB (40501299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dea40ff78bf9cdbb2384fb35a4bb7127dac17db236f078dcc3d9de59148a06`  
		Last Modified: Sat, 30 Apr 2022 01:00:28 GMT  
		Size: 315.7 KB (315673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d375b84b753999e87a8ed0b405d15fd34c522a1f831031dad0599a36d2f84491`  
		Last Modified: Sat, 30 Apr 2022 01:01:07 GMT  
		Size: 60.5 MB (60481908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b5b7095191acb5cd8a7361427292819dc1bc964f10e4ebb99aea3a00e113c1`  
		Last Modified: Sat, 30 Apr 2022 01:01:32 GMT  
		Size: 14.1 MB (14064485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7b254652b1ff037527cc04a7dfc60d2ff4f28dfb3fea29a192499a2b48019a17
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337474799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452f9a01749cd1dd57fda1c22ab16becc392c6f85837a65638348968970665f0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:20:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:20:44 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:20:45 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:20:46 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:21:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:21:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:21:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:22:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:22:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:22:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:23:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1a842c5f450bf757d4efae2d77d0b3637b2f76a02794282656ef03f45e1f1`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e026a627567dcb9c599ab69248d8c084364d4df165bc5257f923c2709f493ab`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527d513e9f97294799a5126bcf25e7f7b73ff93ceb27622f1b3838d580fcde9`  
		Last Modified: Sat, 30 Apr 2022 00:38:47 GMT  
		Size: 171.3 MB (171293442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc48433487f9d4e46329a07c1247899a65bab17103180e95e2da17c25f686d5`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9776aee7c7d20a2a679ec671b31130800b8048248586171aa655e89df4b91f4a`  
		Last Modified: Sat, 30 Apr 2022 00:39:05 GMT  
		Size: 45.0 MB (44988594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890ccdeaa4aedd37f00917bbddd6365cd5dc7f1746a97c5520462003cccd6b3a`  
		Last Modified: Sat, 30 Apr 2022 00:38:58 GMT  
		Size: 315.6 KB (315611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8b7144add68575402586085ccee53c0002fd54ef7e2813f589098a7cce933e`  
		Last Modified: Sat, 30 Apr 2022 00:39:09 GMT  
		Size: 71.8 MB (71753617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877ece7883f291d281f7de9072fa07427d7bf0ac57e8394bcd57db019004f91e`  
		Last Modified: Sat, 30 Apr 2022 00:39:27 GMT  
		Size: 15.4 MB (15447701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:639cbd7dd6e31741d5501387d4b4d3ea14184abe76b63a3b54d0da46bca4ae9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:06f11bae1fe6d88435a4f3fd50f68714f82ac481556a5fe64d7728626afe6395
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484792573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df3ed63c705dfd05177d123ca4d5a37b56dbeede4cfc71c9ddfd54b46e0c72c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:37:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:37:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 20 Apr 2022 17:37:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 20 Apr 2022 17:37:26 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 17:37:26 GMT
ENV LC_ALL=C.UTF-8
# Wed, 20 Apr 2022 17:37:26 GMT
ENV ROS_DISTRO=noetic
# Wed, 20 Apr 2022 17:38:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:38:27 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 20 Apr 2022 17:38:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 20 Apr 2022 17:38:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:38:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:39:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 20 Apr 2022 17:39:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:39:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20546aaa06f50802eafdb39e7339d4cb6230c7a1aff32a53c46d1fcfed8f2dd5`  
		Last Modified: Wed, 20 Apr 2022 17:43:00 GMT  
		Size: 10.9 MB (10892097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abde7f24de9cf0bbb2249385441601015b239338b7901eae3402cb42a98c589`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afac4f8c5429cab550330c262feb633f708f9eda06ab0962fa784c88a9c3459a`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8609835955c8073fb8ee41d1c9ebb686c08c5a154f81dc42e1ee92614d6e430`  
		Last Modified: Wed, 20 Apr 2022 17:43:31 GMT  
		Size: 239.2 MB (239162184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb06026309bf4ee95de3a56281f392cddaad08a74c5056617cee6a3cbad0840`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757a381d58433d12adbc8267c4306c48e05ceab27e9b7180e6ab5153115398a9`  
		Last Modified: Wed, 20 Apr 2022 17:43:51 GMT  
		Size: 86.6 MB (86566693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2d2e540aad82640f395c83b534034224c4743c463281a9308bcd39e755a9a5`  
		Last Modified: Wed, 20 Apr 2022 17:43:39 GMT  
		Size: 309.3 KB (309290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc64f783db31ecba0dea771f5c67d54898bd9e111176ecd00620deaa53fef6e`  
		Last Modified: Wed, 20 Apr 2022 17:43:49 GMT  
		Size: 76.0 MB (75976251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1c560921f8011622c11605269becc4a75f29225fe293f61872f0046836466a`  
		Last Modified: Wed, 20 Apr 2022 17:44:01 GMT  
		Size: 21.4 MB (21446664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f6d9402dd9ab9325e630216c0891b72ea6f7be615d81b3d353d2d87dcb0a3528
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.9 MB (423920584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86513fad1e0a77e9431d687d44981867b263681a71c599265f41c15ffa14429`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:10:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:10:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 20 Apr 2022 12:10:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 20 Apr 2022 12:10:22 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:10:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 20 Apr 2022 12:10:24 GMT
ENV ROS_DISTRO=noetic
# Wed, 20 Apr 2022 12:11:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:11:39 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 20 Apr 2022 12:11:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 20 Apr 2022 12:11:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:12:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:12:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 20 Apr 2022 12:13:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:13:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3957d218911547e664ee734939dc71ad089b29ed94b50f538786d667373e1ce5`  
		Last Modified: Wed, 20 Apr 2022 12:18:50 GMT  
		Size: 10.7 MB (10688204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2c217f5a5971a62fad5aac5564915eaf89c57b2110a7751a364f5a0de02dd7`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4a549feaf8502a671617c04bc2c2a084e6374b096bd615bebf4d2b3278be0a`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a05822887f56bc9d0b9364d7c755b5baee6c94b00f61dd5c41b4c2392919797`  
		Last Modified: Wed, 20 Apr 2022 12:19:19 GMT  
		Size: 184.4 MB (184369896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8501994f2ad5e8e01905fad8c5f1491a035971eab743a788c7208cf18255c4e`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd36c64b99b0defab15ab0ce0f85dbf6fbab02bd969287c79becce5d9293059c`  
		Last Modified: Wed, 20 Apr 2022 12:19:38 GMT  
		Size: 84.4 MB (84352350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0359920e3958bfbe6523bec5a0c24d8479e58e68ab41c3c437aa9806e83e776e`  
		Last Modified: Wed, 20 Apr 2022 12:19:27 GMT  
		Size: 309.2 KB (309235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e22341ca497d2ab03ede7e0d29948509d06168bfff83be501fc2c9fb1499be`  
		Last Modified: Wed, 20 Apr 2022 12:19:37 GMT  
		Size: 73.9 MB (73865013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd96d96d99154147eebbce9635acab9f6a43ffeac0ccf758ad22469b3c6fc15`  
		Last Modified: Wed, 20 Apr 2022 12:19:49 GMT  
		Size: 21.1 MB (21105780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:baa43b9b599444bff925df05e70a49cdb0a17aeaf7f9cfd8e86796ef545f38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:82adffa092e98d53cac94a9ecb55ba7569efc8f0f5d22fa619f93ce70eb50a80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358880748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e0ca8e38ae15069727b4c1507435dfe3fb53c865c6ab323f807fd32afdec7f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:26:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:26:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 22 Apr 2022 03:28:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:28 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:28:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:28:28 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:28:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:29:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a113e5bfc6a41a0f6d9401ad372ec451407fd55bff2862a2023976889322604`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c65e0abed62803e4b89b3aa305b9b4f0262f25940675f4b8fa7ad7bb9f01a9`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90362b1253ae0b3ad24a095a66a71c2437d714ea43529f9af6cf1f9ee26e7d6`  
		Last Modified: Fri, 22 Apr 2022 03:50:08 GMT  
		Size: 176.9 MB (176875279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424da76ce8b30c3127dada4dbec6e2374d087e7e2b0951038c14545d05b87cc7`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fb42a12f184b9b6ad2c9b99a06bdfba4eb6b8c9d97cb8eb224a20386496a4a`  
		Last Modified: Fri, 22 Apr 2022 03:50:26 GMT  
		Size: 50.9 MB (50933515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9199749d47db40394c6f583da9bf1786de2f23b56c00534df5ab66d5e7ff7`  
		Last Modified: Fri, 22 Apr 2022 03:50:18 GMT  
		Size: 314.8 KB (314824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647f59c451e50b55164b1df4f395c7658e7583fbee1cb10ac1d0c4231a7abf39`  
		Last Modified: Fri, 22 Apr 2022 03:50:30 GMT  
		Size: 79.6 MB (79602400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f093d22dbe5877606fa8a0bb7ab4ff9f764a797720db05f3891f492ba89135`  
		Last Modified: Fri, 22 Apr 2022 03:50:46 GMT  
		Size: 15.9 MB (15858801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:925e6735d0b0a8bd360ae8b6f9bb3430e72444f8460bc6bd09c456b484b52f57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302722275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd50d304cce6369dd44fe927243dae8e7814cc4f7542f0689e49734ffc263139`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:39:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:39:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:39:27 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:41:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:41:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:41:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:41:54 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:42:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:42:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:43:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:44:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788bc5672cc0168109c03624bd9c0486dc436058f2ef6bd58aa20183c16330dc`  
		Last Modified: Sat, 30 Apr 2022 00:58:13 GMT  
		Size: 1.2 MB (1182235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f050457c70471d51e645d9056bf76421874818d4dcb3c2d9167cc4c7c59f1`  
		Last Modified: Sat, 30 Apr 2022 00:58:12 GMT  
		Size: 4.7 MB (4676780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf102ed76521e041cbd91514e5b37b5e35694a768c899009f51ba52983b3d4d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b493804b771bd37872f55298ac60b41ddb64199e41c6cbd02a5bd78b13f2e17`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf0953c9382836b5d5e61b0e28e2f23c2431ef644d2ddc2d4a5bffbadff9b15`  
		Last Modified: Sat, 30 Apr 2022 01:00:16 GMT  
		Size: 157.4 MB (157423830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5012cfe0e5842d29eb696b50431a424ba513d5c1554715f456713b05532596d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faae41d6b1935d771645ed3646ee3838471dd083a2f92d29b121834b2a712fab`  
		Last Modified: Sat, 30 Apr 2022 01:00:51 GMT  
		Size: 40.5 MB (40501299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dea40ff78bf9cdbb2384fb35a4bb7127dac17db236f078dcc3d9de59148a06`  
		Last Modified: Sat, 30 Apr 2022 01:00:28 GMT  
		Size: 315.7 KB (315673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d375b84b753999e87a8ed0b405d15fd34c522a1f831031dad0599a36d2f84491`  
		Last Modified: Sat, 30 Apr 2022 01:01:07 GMT  
		Size: 60.5 MB (60481908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b5b7095191acb5cd8a7361427292819dc1bc964f10e4ebb99aea3a00e113c1`  
		Last Modified: Sat, 30 Apr 2022 01:01:32 GMT  
		Size: 14.1 MB (14064485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7b254652b1ff037527cc04a7dfc60d2ff4f28dfb3fea29a192499a2b48019a17
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337474799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452f9a01749cd1dd57fda1c22ab16becc392c6f85837a65638348968970665f0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:20:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:20:44 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:20:45 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:20:46 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:21:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:21:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:21:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:22:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:22:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:22:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:23:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1a842c5f450bf757d4efae2d77d0b3637b2f76a02794282656ef03f45e1f1`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e026a627567dcb9c599ab69248d8c084364d4df165bc5257f923c2709f493ab`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527d513e9f97294799a5126bcf25e7f7b73ff93ceb27622f1b3838d580fcde9`  
		Last Modified: Sat, 30 Apr 2022 00:38:47 GMT  
		Size: 171.3 MB (171293442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc48433487f9d4e46329a07c1247899a65bab17103180e95e2da17c25f686d5`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9776aee7c7d20a2a679ec671b31130800b8048248586171aa655e89df4b91f4a`  
		Last Modified: Sat, 30 Apr 2022 00:39:05 GMT  
		Size: 45.0 MB (44988594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890ccdeaa4aedd37f00917bbddd6365cd5dc7f1746a97c5520462003cccd6b3a`  
		Last Modified: Sat, 30 Apr 2022 00:38:58 GMT  
		Size: 315.6 KB (315611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8b7144add68575402586085ccee53c0002fd54ef7e2813f589098a7cce933e`  
		Last Modified: Sat, 30 Apr 2022 00:39:09 GMT  
		Size: 71.8 MB (71753617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877ece7883f291d281f7de9072fa07427d7bf0ac57e8394bcd57db019004f91e`  
		Last Modified: Sat, 30 Apr 2022 00:39:27 GMT  
		Size: 15.4 MB (15447701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:8076aa2a1acb8782dafa600b60ac18d61240a4214a5780482938a7f82fadf1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:62e0f0bf5659f14e229c216fa8b63e1ee9d2ca697ad8a5471bfe157b9957efad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.0 MB (343021947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fd733d2da3cc8a934cace2a21423ed6c30c11016a16c493a06b9b3f312039b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:26:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:26:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 22 Apr 2022 03:28:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:28 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:28:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:28:28 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:28:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:29:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a113e5bfc6a41a0f6d9401ad372ec451407fd55bff2862a2023976889322604`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c65e0abed62803e4b89b3aa305b9b4f0262f25940675f4b8fa7ad7bb9f01a9`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90362b1253ae0b3ad24a095a66a71c2437d714ea43529f9af6cf1f9ee26e7d6`  
		Last Modified: Fri, 22 Apr 2022 03:50:08 GMT  
		Size: 176.9 MB (176875279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424da76ce8b30c3127dada4dbec6e2374d087e7e2b0951038c14545d05b87cc7`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fb42a12f184b9b6ad2c9b99a06bdfba4eb6b8c9d97cb8eb224a20386496a4a`  
		Last Modified: Fri, 22 Apr 2022 03:50:26 GMT  
		Size: 50.9 MB (50933515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9199749d47db40394c6f583da9bf1786de2f23b56c00534df5ab66d5e7ff7`  
		Last Modified: Fri, 22 Apr 2022 03:50:18 GMT  
		Size: 314.8 KB (314824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647f59c451e50b55164b1df4f395c7658e7583fbee1cb10ac1d0c4231a7abf39`  
		Last Modified: Fri, 22 Apr 2022 03:50:30 GMT  
		Size: 79.6 MB (79602400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:4fde0076ff1a895147ac2024675ff31ba8d303480a76aefe0c0fe4f4da840e9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288657790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5ed39b32a22763a4e60b12651dc742897d6eb060f5ca112244773945a49537`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:39:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:39:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:39:27 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:41:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:41:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:41:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:41:54 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:42:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:42:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:43:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788bc5672cc0168109c03624bd9c0486dc436058f2ef6bd58aa20183c16330dc`  
		Last Modified: Sat, 30 Apr 2022 00:58:13 GMT  
		Size: 1.2 MB (1182235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f050457c70471d51e645d9056bf76421874818d4dcb3c2d9167cc4c7c59f1`  
		Last Modified: Sat, 30 Apr 2022 00:58:12 GMT  
		Size: 4.7 MB (4676780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf102ed76521e041cbd91514e5b37b5e35694a768c899009f51ba52983b3d4d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b493804b771bd37872f55298ac60b41ddb64199e41c6cbd02a5bd78b13f2e17`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf0953c9382836b5d5e61b0e28e2f23c2431ef644d2ddc2d4a5bffbadff9b15`  
		Last Modified: Sat, 30 Apr 2022 01:00:16 GMT  
		Size: 157.4 MB (157423830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5012cfe0e5842d29eb696b50431a424ba513d5c1554715f456713b05532596d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faae41d6b1935d771645ed3646ee3838471dd083a2f92d29b121834b2a712fab`  
		Last Modified: Sat, 30 Apr 2022 01:00:51 GMT  
		Size: 40.5 MB (40501299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dea40ff78bf9cdbb2384fb35a4bb7127dac17db236f078dcc3d9de59148a06`  
		Last Modified: Sat, 30 Apr 2022 01:00:28 GMT  
		Size: 315.7 KB (315673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d375b84b753999e87a8ed0b405d15fd34c522a1f831031dad0599a36d2f84491`  
		Last Modified: Sat, 30 Apr 2022 01:01:07 GMT  
		Size: 60.5 MB (60481908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0947defb184c2b20e8ecc6e46de7f5cea05f9153f501b7de2631711c44034219
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322027098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901688928341e7b725a0f474197821ddabbb0e5966213c9a6ac648fe518fb26d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:20:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:20:44 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:20:45 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:20:46 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:21:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:21:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:21:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:22:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:22:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:22:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1a842c5f450bf757d4efae2d77d0b3637b2f76a02794282656ef03f45e1f1`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e026a627567dcb9c599ab69248d8c084364d4df165bc5257f923c2709f493ab`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527d513e9f97294799a5126bcf25e7f7b73ff93ceb27622f1b3838d580fcde9`  
		Last Modified: Sat, 30 Apr 2022 00:38:47 GMT  
		Size: 171.3 MB (171293442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc48433487f9d4e46329a07c1247899a65bab17103180e95e2da17c25f686d5`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9776aee7c7d20a2a679ec671b31130800b8048248586171aa655e89df4b91f4a`  
		Last Modified: Sat, 30 Apr 2022 00:39:05 GMT  
		Size: 45.0 MB (44988594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890ccdeaa4aedd37f00917bbddd6365cd5dc7f1746a97c5520462003cccd6b3a`  
		Last Modified: Sat, 30 Apr 2022 00:38:58 GMT  
		Size: 315.6 KB (315611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8b7144add68575402586085ccee53c0002fd54ef7e2813f589098a7cce933e`  
		Last Modified: Sat, 30 Apr 2022 00:39:09 GMT  
		Size: 71.8 MB (71753617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:e8d3f1b71626a3c53aeb5a67fdf9363f35dc897f7d36bff8133c8b29bad08e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:6b4406b04c3846197e0bd36ebd863516ccf681c16a0bee86361a33ef668549c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.3 MB (463345909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920dd0639d765b1780c742f8ab16fc2f50932373bfde99d3bb475d7b813f7067`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:37:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:37:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 20 Apr 2022 17:37:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 20 Apr 2022 17:37:26 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 17:37:26 GMT
ENV LC_ALL=C.UTF-8
# Wed, 20 Apr 2022 17:37:26 GMT
ENV ROS_DISTRO=noetic
# Wed, 20 Apr 2022 17:38:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:38:27 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 20 Apr 2022 17:38:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 20 Apr 2022 17:38:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:38:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:39:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 20 Apr 2022 17:39:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20546aaa06f50802eafdb39e7339d4cb6230c7a1aff32a53c46d1fcfed8f2dd5`  
		Last Modified: Wed, 20 Apr 2022 17:43:00 GMT  
		Size: 10.9 MB (10892097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abde7f24de9cf0bbb2249385441601015b239338b7901eae3402cb42a98c589`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afac4f8c5429cab550330c262feb633f708f9eda06ab0962fa784c88a9c3459a`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8609835955c8073fb8ee41d1c9ebb686c08c5a154f81dc42e1ee92614d6e430`  
		Last Modified: Wed, 20 Apr 2022 17:43:31 GMT  
		Size: 239.2 MB (239162184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb06026309bf4ee95de3a56281f392cddaad08a74c5056617cee6a3cbad0840`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757a381d58433d12adbc8267c4306c48e05ceab27e9b7180e6ab5153115398a9`  
		Last Modified: Wed, 20 Apr 2022 17:43:51 GMT  
		Size: 86.6 MB (86566693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2d2e540aad82640f395c83b534034224c4743c463281a9308bcd39e755a9a5`  
		Last Modified: Wed, 20 Apr 2022 17:43:39 GMT  
		Size: 309.3 KB (309290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc64f783db31ecba0dea771f5c67d54898bd9e111176ecd00620deaa53fef6e`  
		Last Modified: Wed, 20 Apr 2022 17:43:49 GMT  
		Size: 76.0 MB (75976251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:93dbc8057d883b94580a8234ec329cda459fea35afe75515fb0f9a61d8be3e83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402814804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd23d08ebda2ecf5c0c0951aace97a48e98f0e7ff9ff80bc25cb84f4d52d6288`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:10:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:10:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 20 Apr 2022 12:10:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 20 Apr 2022 12:10:22 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:10:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 20 Apr 2022 12:10:24 GMT
ENV ROS_DISTRO=noetic
# Wed, 20 Apr 2022 12:11:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:11:39 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 20 Apr 2022 12:11:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 20 Apr 2022 12:11:42 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:12:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:12:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 20 Apr 2022 12:13:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3957d218911547e664ee734939dc71ad089b29ed94b50f538786d667373e1ce5`  
		Last Modified: Wed, 20 Apr 2022 12:18:50 GMT  
		Size: 10.7 MB (10688204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2c217f5a5971a62fad5aac5564915eaf89c57b2110a7751a364f5a0de02dd7`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4a549feaf8502a671617c04bc2c2a084e6374b096bd615bebf4d2b3278be0a`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a05822887f56bc9d0b9364d7c755b5baee6c94b00f61dd5c41b4c2392919797`  
		Last Modified: Wed, 20 Apr 2022 12:19:19 GMT  
		Size: 184.4 MB (184369896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8501994f2ad5e8e01905fad8c5f1491a035971eab743a788c7208cf18255c4e`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd36c64b99b0defab15ab0ce0f85dbf6fbab02bd969287c79becce5d9293059c`  
		Last Modified: Wed, 20 Apr 2022 12:19:38 GMT  
		Size: 84.4 MB (84352350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0359920e3958bfbe6523bec5a0c24d8479e58e68ab41c3c437aa9806e83e776e`  
		Last Modified: Wed, 20 Apr 2022 12:19:27 GMT  
		Size: 309.2 KB (309235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e22341ca497d2ab03ede7e0d29948509d06168bfff83be501fc2c9fb1499be`  
		Last Modified: Wed, 20 Apr 2022 12:19:37 GMT  
		Size: 73.9 MB (73865013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:8076aa2a1acb8782dafa600b60ac18d61240a4214a5780482938a7f82fadf1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:62e0f0bf5659f14e229c216fa8b63e1ee9d2ca697ad8a5471bfe157b9957efad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.0 MB (343021947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fd733d2da3cc8a934cace2a21423ed6c30c11016a16c493a06b9b3f312039b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:26:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:26:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 22 Apr 2022 03:28:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:28 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:28:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:28:28 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:28:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:29:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a113e5bfc6a41a0f6d9401ad372ec451407fd55bff2862a2023976889322604`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c65e0abed62803e4b89b3aa305b9b4f0262f25940675f4b8fa7ad7bb9f01a9`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90362b1253ae0b3ad24a095a66a71c2437d714ea43529f9af6cf1f9ee26e7d6`  
		Last Modified: Fri, 22 Apr 2022 03:50:08 GMT  
		Size: 176.9 MB (176875279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424da76ce8b30c3127dada4dbec6e2374d087e7e2b0951038c14545d05b87cc7`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fb42a12f184b9b6ad2c9b99a06bdfba4eb6b8c9d97cb8eb224a20386496a4a`  
		Last Modified: Fri, 22 Apr 2022 03:50:26 GMT  
		Size: 50.9 MB (50933515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9199749d47db40394c6f583da9bf1786de2f23b56c00534df5ab66d5e7ff7`  
		Last Modified: Fri, 22 Apr 2022 03:50:18 GMT  
		Size: 314.8 KB (314824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647f59c451e50b55164b1df4f395c7658e7583fbee1cb10ac1d0c4231a7abf39`  
		Last Modified: Fri, 22 Apr 2022 03:50:30 GMT  
		Size: 79.6 MB (79602400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:4fde0076ff1a895147ac2024675ff31ba8d303480a76aefe0c0fe4f4da840e9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288657790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5ed39b32a22763a4e60b12651dc742897d6eb060f5ca112244773945a49537`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:39:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:39:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:39:27 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:41:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:41:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:41:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:41:54 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:42:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:42:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:43:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788bc5672cc0168109c03624bd9c0486dc436058f2ef6bd58aa20183c16330dc`  
		Last Modified: Sat, 30 Apr 2022 00:58:13 GMT  
		Size: 1.2 MB (1182235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f050457c70471d51e645d9056bf76421874818d4dcb3c2d9167cc4c7c59f1`  
		Last Modified: Sat, 30 Apr 2022 00:58:12 GMT  
		Size: 4.7 MB (4676780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf102ed76521e041cbd91514e5b37b5e35694a768c899009f51ba52983b3d4d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b493804b771bd37872f55298ac60b41ddb64199e41c6cbd02a5bd78b13f2e17`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf0953c9382836b5d5e61b0e28e2f23c2431ef644d2ddc2d4a5bffbadff9b15`  
		Last Modified: Sat, 30 Apr 2022 01:00:16 GMT  
		Size: 157.4 MB (157423830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5012cfe0e5842d29eb696b50431a424ba513d5c1554715f456713b05532596d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faae41d6b1935d771645ed3646ee3838471dd083a2f92d29b121834b2a712fab`  
		Last Modified: Sat, 30 Apr 2022 01:00:51 GMT  
		Size: 40.5 MB (40501299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dea40ff78bf9cdbb2384fb35a4bb7127dac17db236f078dcc3d9de59148a06`  
		Last Modified: Sat, 30 Apr 2022 01:00:28 GMT  
		Size: 315.7 KB (315673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d375b84b753999e87a8ed0b405d15fd34c522a1f831031dad0599a36d2f84491`  
		Last Modified: Sat, 30 Apr 2022 01:01:07 GMT  
		Size: 60.5 MB (60481908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0947defb184c2b20e8ecc6e46de7f5cea05f9153f501b7de2631711c44034219
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322027098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901688928341e7b725a0f474197821ddabbb0e5966213c9a6ac648fe518fb26d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:20:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:20:44 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:20:45 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:20:46 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:21:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:21:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:21:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:22:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:22:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:22:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1a842c5f450bf757d4efae2d77d0b3637b2f76a02794282656ef03f45e1f1`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e026a627567dcb9c599ab69248d8c084364d4df165bc5257f923c2709f493ab`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527d513e9f97294799a5126bcf25e7f7b73ff93ceb27622f1b3838d580fcde9`  
		Last Modified: Sat, 30 Apr 2022 00:38:47 GMT  
		Size: 171.3 MB (171293442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc48433487f9d4e46329a07c1247899a65bab17103180e95e2da17c25f686d5`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9776aee7c7d20a2a679ec671b31130800b8048248586171aa655e89df4b91f4a`  
		Last Modified: Sat, 30 Apr 2022 00:39:05 GMT  
		Size: 45.0 MB (44988594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890ccdeaa4aedd37f00917bbddd6365cd5dc7f1746a97c5520462003cccd6b3a`  
		Last Modified: Sat, 30 Apr 2022 00:38:58 GMT  
		Size: 315.6 KB (315611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8b7144add68575402586085ccee53c0002fd54ef7e2813f589098a7cce933e`  
		Last Modified: Sat, 30 Apr 2022 00:39:09 GMT  
		Size: 71.8 MB (71753617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:2ab9be3cd70ac04893150f88a37a5b7edd9ae35f4e0119afe48acdfe4daaa911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:d44e2d917030a80e982ed14e0450d57be0a03baa9dc90d5810f8620707f157da
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212171208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fa98b743825a049a552c2f66c918e1b3190587b8e8f26ae9e62bea74906cfa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:26:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:26:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 22 Apr 2022 03:28:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:28 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:28:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:28:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a113e5bfc6a41a0f6d9401ad372ec451407fd55bff2862a2023976889322604`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c65e0abed62803e4b89b3aa305b9b4f0262f25940675f4b8fa7ad7bb9f01a9`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90362b1253ae0b3ad24a095a66a71c2437d714ea43529f9af6cf1f9ee26e7d6`  
		Last Modified: Fri, 22 Apr 2022 03:50:08 GMT  
		Size: 176.9 MB (176875279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424da76ce8b30c3127dada4dbec6e2374d087e7e2b0951038c14545d05b87cc7`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:8d17d6a993ab786d8ae8747ab4d2f45c09f70ee1b720bce78bdb93d0aa5a3437
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187358910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30146a9cf0c776eae9f57a3a17c70b0465f85988404510ace36f3d928137f667`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:39:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:39:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:39:27 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:41:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:41:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:41:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:41:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788bc5672cc0168109c03624bd9c0486dc436058f2ef6bd58aa20183c16330dc`  
		Last Modified: Sat, 30 Apr 2022 00:58:13 GMT  
		Size: 1.2 MB (1182235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f050457c70471d51e645d9056bf76421874818d4dcb3c2d9167cc4c7c59f1`  
		Last Modified: Sat, 30 Apr 2022 00:58:12 GMT  
		Size: 4.7 MB (4676780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf102ed76521e041cbd91514e5b37b5e35694a768c899009f51ba52983b3d4d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b493804b771bd37872f55298ac60b41ddb64199e41c6cbd02a5bd78b13f2e17`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf0953c9382836b5d5e61b0e28e2f23c2431ef644d2ddc2d4a5bffbadff9b15`  
		Last Modified: Sat, 30 Apr 2022 01:00:16 GMT  
		Size: 157.4 MB (157423830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5012cfe0e5842d29eb696b50431a424ba513d5c1554715f456713b05532596d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:603cce6a1cb690b83b7fda6ed27b689d97462e67d04b7dd803b1cca971d326ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204969276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f66387e9eada2d5826273519b20d1dcb3a85cbfcef655873df0291343df6eb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:20:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:20:44 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:20:45 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:20:46 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:21:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:21:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:21:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1a842c5f450bf757d4efae2d77d0b3637b2f76a02794282656ef03f45e1f1`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e026a627567dcb9c599ab69248d8c084364d4df165bc5257f923c2709f493ab`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527d513e9f97294799a5126bcf25e7f7b73ff93ceb27622f1b3838d580fcde9`  
		Last Modified: Sat, 30 Apr 2022 00:38:47 GMT  
		Size: 171.3 MB (171293442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc48433487f9d4e46329a07c1247899a65bab17103180e95e2da17c25f686d5`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:89d2d4a66f45461a687e24602ae35bce5ce102bccf86d41a7a1c9b6163cd6e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:84351d18f44271dd8a4ace0db9e9a7c7ffa02a108ff424b3abcd8b055312a296
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300493675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdddb757d3d82bc10e186b274307e6f5b72f5aeb6590ba010135f94263fd1881`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:37:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:37:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 20 Apr 2022 17:37:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 20 Apr 2022 17:37:26 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 17:37:26 GMT
ENV LC_ALL=C.UTF-8
# Wed, 20 Apr 2022 17:37:26 GMT
ENV ROS_DISTRO=noetic
# Wed, 20 Apr 2022 17:38:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:38:27 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 20 Apr 2022 17:38:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 20 Apr 2022 17:38:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20546aaa06f50802eafdb39e7339d4cb6230c7a1aff32a53c46d1fcfed8f2dd5`  
		Last Modified: Wed, 20 Apr 2022 17:43:00 GMT  
		Size: 10.9 MB (10892097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abde7f24de9cf0bbb2249385441601015b239338b7901eae3402cb42a98c589`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afac4f8c5429cab550330c262feb633f708f9eda06ab0962fa784c88a9c3459a`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8609835955c8073fb8ee41d1c9ebb686c08c5a154f81dc42e1ee92614d6e430`  
		Last Modified: Wed, 20 Apr 2022 17:43:31 GMT  
		Size: 239.2 MB (239162184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb06026309bf4ee95de3a56281f392cddaad08a74c5056617cee6a3cbad0840`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3a167a3e4a34b48fdac018fdb84126e3a9ea5c99e0a51cda3cfa472cba4e59aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244288206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d559d174d4ed076af61ea7fde4dca79121305b27a81c85da84fb2ed1dd24c426`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:10:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:10:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 20 Apr 2022 12:10:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 20 Apr 2022 12:10:22 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:10:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 20 Apr 2022 12:10:24 GMT
ENV ROS_DISTRO=noetic
# Wed, 20 Apr 2022 12:11:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:11:39 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 20 Apr 2022 12:11:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 20 Apr 2022 12:11:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3957d218911547e664ee734939dc71ad089b29ed94b50f538786d667373e1ce5`  
		Last Modified: Wed, 20 Apr 2022 12:18:50 GMT  
		Size: 10.7 MB (10688204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2c217f5a5971a62fad5aac5564915eaf89c57b2110a7751a364f5a0de02dd7`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4a549feaf8502a671617c04bc2c2a084e6374b096bd615bebf4d2b3278be0a`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a05822887f56bc9d0b9364d7c755b5baee6c94b00f61dd5c41b4c2392919797`  
		Last Modified: Wed, 20 Apr 2022 12:19:19 GMT  
		Size: 184.4 MB (184369896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8501994f2ad5e8e01905fad8c5f1491a035971eab743a788c7208cf18255c4e`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:2ab9be3cd70ac04893150f88a37a5b7edd9ae35f4e0119afe48acdfe4daaa911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:d44e2d917030a80e982ed14e0450d57be0a03baa9dc90d5810f8620707f157da
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212171208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fa98b743825a049a552c2f66c918e1b3190587b8e8f26ae9e62bea74906cfa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:26:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:26:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 22 Apr 2022 03:28:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:28 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:28:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:28:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a113e5bfc6a41a0f6d9401ad372ec451407fd55bff2862a2023976889322604`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c65e0abed62803e4b89b3aa305b9b4f0262f25940675f4b8fa7ad7bb9f01a9`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90362b1253ae0b3ad24a095a66a71c2437d714ea43529f9af6cf1f9ee26e7d6`  
		Last Modified: Fri, 22 Apr 2022 03:50:08 GMT  
		Size: 176.9 MB (176875279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424da76ce8b30c3127dada4dbec6e2374d087e7e2b0951038c14545d05b87cc7`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:8d17d6a993ab786d8ae8747ab4d2f45c09f70ee1b720bce78bdb93d0aa5a3437
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187358910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30146a9cf0c776eae9f57a3a17c70b0465f85988404510ace36f3d928137f667`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:39:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:39:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:39:27 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:41:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:41:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:41:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:41:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788bc5672cc0168109c03624bd9c0486dc436058f2ef6bd58aa20183c16330dc`  
		Last Modified: Sat, 30 Apr 2022 00:58:13 GMT  
		Size: 1.2 MB (1182235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f050457c70471d51e645d9056bf76421874818d4dcb3c2d9167cc4c7c59f1`  
		Last Modified: Sat, 30 Apr 2022 00:58:12 GMT  
		Size: 4.7 MB (4676780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf102ed76521e041cbd91514e5b37b5e35694a768c899009f51ba52983b3d4d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b493804b771bd37872f55298ac60b41ddb64199e41c6cbd02a5bd78b13f2e17`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf0953c9382836b5d5e61b0e28e2f23c2431ef644d2ddc2d4a5bffbadff9b15`  
		Last Modified: Sat, 30 Apr 2022 01:00:16 GMT  
		Size: 157.4 MB (157423830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5012cfe0e5842d29eb696b50431a424ba513d5c1554715f456713b05532596d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:603cce6a1cb690b83b7fda6ed27b689d97462e67d04b7dd803b1cca971d326ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204969276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f66387e9eada2d5826273519b20d1dcb3a85cbfcef655873df0291343df6eb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:20:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:20:44 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:20:45 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:20:46 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:21:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:21:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:21:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1a842c5f450bf757d4efae2d77d0b3637b2f76a02794282656ef03f45e1f1`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e026a627567dcb9c599ab69248d8c084364d4df165bc5257f923c2709f493ab`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527d513e9f97294799a5126bcf25e7f7b73ff93ceb27622f1b3838d580fcde9`  
		Last Modified: Sat, 30 Apr 2022 00:38:47 GMT  
		Size: 171.3 MB (171293442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc48433487f9d4e46329a07c1247899a65bab17103180e95e2da17c25f686d5`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:e262b4b58d7394cfe9e2dc49b36e9b985541f26f0fee78c40d4cfea0d4f2924b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:60f2a37f45af89cb5a543e58e191560ccc0da14b3ed1346578abc6873d702571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263707932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce213b690e983e6d1f65eec950595f8104e0b5a2a8c61823889ee8536220239`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:26 GMT
ADD file:76dd6cab5732b31272279bb8868954cbbecf591f596f0c318524454e95eabfb9 in / 
# Thu, 21 Apr 2022 23:00:26 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:42:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:45 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:42:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:42:46 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:42:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:42:46 GMT
ENV ROS_DISTRO=rolling
# Fri, 22 Apr 2022 03:44:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:44:24 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:44:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:44:24 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:45:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:45:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:45:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:46:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8527c5f86ecc162d68a9d38c8f4c6a6443158c67417e8bc2c3cea9f3868394eb`  
		Last Modified: Thu, 21 Apr 2022 23:02:00 GMT  
		Size: 30.4 MB (30421209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341919f757e419f6142944f5ea95c19b61bf1ff648abdfff94ed8c99c0bfd52c`  
		Last Modified: Fri, 22 Apr 2022 03:55:07 GMT  
		Size: 1.2 MB (1191091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0455c8ef748e7b3e35f60511f8e8053ee76492c9a72a5afd00d55d351854556f`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 3.8 MB (3826746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b72761451ff916be9282f71adece9e357fc9710e86559b986d1f01583fd312`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3452459740e87b470a88f20122447689e1640a2b865eb50f2f4a866ad75d391`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2037c4fb46b3cec9022f679d45d7834d6c89ac325348efc7af3d5d92bcd7658`  
		Last Modified: Fri, 22 Apr 2022 03:55:22 GMT  
		Size: 106.4 MB (106381750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0221e7e4829eedc9594c53ce3492bccdc39ea2c1b77da83a10fdb689100c68`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c7fbeb7e1d7385b2109f0df086ca744db3d917acd012c123fa8edc585a2080`  
		Last Modified: Fri, 22 Apr 2022 03:55:46 GMT  
		Size: 98.8 MB (98754384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b30b9dcc84973150cb0c195863fd24646a6ba41a76b5f0b33c806b25f12281c`  
		Last Modified: Fri, 22 Apr 2022 03:55:33 GMT  
		Size: 268.9 KB (268885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8e6a2755512e3269961eabe5ea4b4f1aec52de907316bb4f8654466d684b8a`  
		Last Modified: Fri, 22 Apr 2022 03:55:32 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba940d517ddac55ea1379c9f2cff56d93e8aa91f44e1303dc4a4261a1ef6810`  
		Last Modified: Fri, 22 Apr 2022 03:55:36 GMT  
		Size: 22.9 MB (22859264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d0e911a94a4c436c6eaac9f332755592ed90fe0be25b9af63f9a2f49ba05f158
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255862942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb412fe1d9860ee058814b5c7aaa792e3483edb85047600538597591910b5b63`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:52 GMT
ADD file:1e18e22e32f06a7e93275cf3a2eb2a1d3892be27628bdae2de4b2aadb992bd50 in / 
# Fri, 29 Apr 2022 22:49:53 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:32:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:32:29 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:32:30 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:32:31 GMT
ENV ROS_DISTRO=rolling
# Sat, 30 Apr 2022 00:33:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:19 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:33:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:33:21 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:34:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:34:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:34:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:34:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b84950154c181a602d2e93b68e84660f96dc78f94ae36f3df2db8d5701abb6a5`  
		Last Modified: Fri, 29 Apr 2022 22:52:07 GMT  
		Size: 28.4 MB (28376457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4339dcf07e4fd919aa10dc0e01fb8f44184f74bf6baf5aef6e8fdd30f5e603`  
		Last Modified: Sat, 30 Apr 2022 00:43:58 GMT  
		Size: 1.2 MB (1192681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0db3fdf5b04e561797500fc1d19d79a37ca0586b71bee71ce2acaee153d4dee`  
		Last Modified: Sat, 30 Apr 2022 00:43:56 GMT  
		Size: 3.6 MB (3594435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af71d8cd404a31e077722270696cf33d59cff54d35c9dad864264138bc3ac`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e01b1250d40bc108a995e5fc6c1630b0abdbfff31529a87a4096271f2a6115`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ae3a3b720aed16343416b9bb5eea4967087c21dee2c39948d0ca129037dd4f`  
		Last Modified: Sat, 30 Apr 2022 00:44:12 GMT  
		Size: 103.8 MB (103773129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be65bd445679ba8af650c6dd6742dc9a2d31871d4bac42819d92857e3a5892d`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ea6f66376f6e1da9bb78a2df21de836c30ea4379d4641ce9b7a1dfce84b6b4`  
		Last Modified: Sat, 30 Apr 2022 00:44:38 GMT  
		Size: 96.2 MB (96157476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a8f645f0a9603e60db84a3de8b50d76b5e58918fc81c2b4b19cea51a1a2a1`  
		Last Modified: Sat, 30 Apr 2022 00:44:24 GMT  
		Size: 269.8 KB (269758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773bf167794f3f7af31d32325c1d102af94787ef5a9d239074eafe9b5582dc75`  
		Last Modified: Sat, 30 Apr 2022 00:44:24 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ab25ab23b7e441a52f03a15aec7da83f14b6f0843949bdbfee2aa35beb1787`  
		Last Modified: Sat, 30 Apr 2022 00:44:28 GMT  
		Size: 22.5 MB (22494500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:e262b4b58d7394cfe9e2dc49b36e9b985541f26f0fee78c40d4cfea0d4f2924b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:60f2a37f45af89cb5a543e58e191560ccc0da14b3ed1346578abc6873d702571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263707932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce213b690e983e6d1f65eec950595f8104e0b5a2a8c61823889ee8536220239`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:26 GMT
ADD file:76dd6cab5732b31272279bb8868954cbbecf591f596f0c318524454e95eabfb9 in / 
# Thu, 21 Apr 2022 23:00:26 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:42:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:45 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:42:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:42:46 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:42:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:42:46 GMT
ENV ROS_DISTRO=rolling
# Fri, 22 Apr 2022 03:44:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:44:24 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:44:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:44:24 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:45:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:45:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:45:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:46:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8527c5f86ecc162d68a9d38c8f4c6a6443158c67417e8bc2c3cea9f3868394eb`  
		Last Modified: Thu, 21 Apr 2022 23:02:00 GMT  
		Size: 30.4 MB (30421209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341919f757e419f6142944f5ea95c19b61bf1ff648abdfff94ed8c99c0bfd52c`  
		Last Modified: Fri, 22 Apr 2022 03:55:07 GMT  
		Size: 1.2 MB (1191091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0455c8ef748e7b3e35f60511f8e8053ee76492c9a72a5afd00d55d351854556f`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 3.8 MB (3826746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b72761451ff916be9282f71adece9e357fc9710e86559b986d1f01583fd312`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3452459740e87b470a88f20122447689e1640a2b865eb50f2f4a866ad75d391`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2037c4fb46b3cec9022f679d45d7834d6c89ac325348efc7af3d5d92bcd7658`  
		Last Modified: Fri, 22 Apr 2022 03:55:22 GMT  
		Size: 106.4 MB (106381750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0221e7e4829eedc9594c53ce3492bccdc39ea2c1b77da83a10fdb689100c68`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c7fbeb7e1d7385b2109f0df086ca744db3d917acd012c123fa8edc585a2080`  
		Last Modified: Fri, 22 Apr 2022 03:55:46 GMT  
		Size: 98.8 MB (98754384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b30b9dcc84973150cb0c195863fd24646a6ba41a76b5f0b33c806b25f12281c`  
		Last Modified: Fri, 22 Apr 2022 03:55:33 GMT  
		Size: 268.9 KB (268885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8e6a2755512e3269961eabe5ea4b4f1aec52de907316bb4f8654466d684b8a`  
		Last Modified: Fri, 22 Apr 2022 03:55:32 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba940d517ddac55ea1379c9f2cff56d93e8aa91f44e1303dc4a4261a1ef6810`  
		Last Modified: Fri, 22 Apr 2022 03:55:36 GMT  
		Size: 22.9 MB (22859264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d0e911a94a4c436c6eaac9f332755592ed90fe0be25b9af63f9a2f49ba05f158
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255862942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb412fe1d9860ee058814b5c7aaa792e3483edb85047600538597591910b5b63`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:52 GMT
ADD file:1e18e22e32f06a7e93275cf3a2eb2a1d3892be27628bdae2de4b2aadb992bd50 in / 
# Fri, 29 Apr 2022 22:49:53 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:32:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:32:29 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:32:30 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:32:31 GMT
ENV ROS_DISTRO=rolling
# Sat, 30 Apr 2022 00:33:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:19 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:33:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:33:21 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:34:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:34:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:34:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:34:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b84950154c181a602d2e93b68e84660f96dc78f94ae36f3df2db8d5701abb6a5`  
		Last Modified: Fri, 29 Apr 2022 22:52:07 GMT  
		Size: 28.4 MB (28376457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4339dcf07e4fd919aa10dc0e01fb8f44184f74bf6baf5aef6e8fdd30f5e603`  
		Last Modified: Sat, 30 Apr 2022 00:43:58 GMT  
		Size: 1.2 MB (1192681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0db3fdf5b04e561797500fc1d19d79a37ca0586b71bee71ce2acaee153d4dee`  
		Last Modified: Sat, 30 Apr 2022 00:43:56 GMT  
		Size: 3.6 MB (3594435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af71d8cd404a31e077722270696cf33d59cff54d35c9dad864264138bc3ac`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e01b1250d40bc108a995e5fc6c1630b0abdbfff31529a87a4096271f2a6115`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ae3a3b720aed16343416b9bb5eea4967087c21dee2c39948d0ca129037dd4f`  
		Last Modified: Sat, 30 Apr 2022 00:44:12 GMT  
		Size: 103.8 MB (103773129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be65bd445679ba8af650c6dd6742dc9a2d31871d4bac42819d92857e3a5892d`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ea6f66376f6e1da9bb78a2df21de836c30ea4379d4641ce9b7a1dfce84b6b4`  
		Last Modified: Sat, 30 Apr 2022 00:44:38 GMT  
		Size: 96.2 MB (96157476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a8f645f0a9603e60db84a3de8b50d76b5e58918fc81c2b4b19cea51a1a2a1`  
		Last Modified: Sat, 30 Apr 2022 00:44:24 GMT  
		Size: 269.8 KB (269758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773bf167794f3f7af31d32325c1d102af94787ef5a9d239074eafe9b5582dc75`  
		Last Modified: Sat, 30 Apr 2022 00:44:24 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ab25ab23b7e441a52f03a15aec7da83f14b6f0843949bdbfee2aa35beb1787`  
		Last Modified: Sat, 30 Apr 2022 00:44:28 GMT  
		Size: 22.5 MB (22494500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:e262b4b58d7394cfe9e2dc49b36e9b985541f26f0fee78c40d4cfea0d4f2924b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:60f2a37f45af89cb5a543e58e191560ccc0da14b3ed1346578abc6873d702571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263707932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce213b690e983e6d1f65eec950595f8104e0b5a2a8c61823889ee8536220239`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:26 GMT
ADD file:76dd6cab5732b31272279bb8868954cbbecf591f596f0c318524454e95eabfb9 in / 
# Thu, 21 Apr 2022 23:00:26 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:42:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:45 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:42:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:42:46 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:42:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:42:46 GMT
ENV ROS_DISTRO=rolling
# Fri, 22 Apr 2022 03:44:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:44:24 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:44:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:44:24 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:45:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:45:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:45:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:46:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8527c5f86ecc162d68a9d38c8f4c6a6443158c67417e8bc2c3cea9f3868394eb`  
		Last Modified: Thu, 21 Apr 2022 23:02:00 GMT  
		Size: 30.4 MB (30421209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341919f757e419f6142944f5ea95c19b61bf1ff648abdfff94ed8c99c0bfd52c`  
		Last Modified: Fri, 22 Apr 2022 03:55:07 GMT  
		Size: 1.2 MB (1191091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0455c8ef748e7b3e35f60511f8e8053ee76492c9a72a5afd00d55d351854556f`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 3.8 MB (3826746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b72761451ff916be9282f71adece9e357fc9710e86559b986d1f01583fd312`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3452459740e87b470a88f20122447689e1640a2b865eb50f2f4a866ad75d391`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2037c4fb46b3cec9022f679d45d7834d6c89ac325348efc7af3d5d92bcd7658`  
		Last Modified: Fri, 22 Apr 2022 03:55:22 GMT  
		Size: 106.4 MB (106381750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0221e7e4829eedc9594c53ce3492bccdc39ea2c1b77da83a10fdb689100c68`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c7fbeb7e1d7385b2109f0df086ca744db3d917acd012c123fa8edc585a2080`  
		Last Modified: Fri, 22 Apr 2022 03:55:46 GMT  
		Size: 98.8 MB (98754384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b30b9dcc84973150cb0c195863fd24646a6ba41a76b5f0b33c806b25f12281c`  
		Last Modified: Fri, 22 Apr 2022 03:55:33 GMT  
		Size: 268.9 KB (268885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8e6a2755512e3269961eabe5ea4b4f1aec52de907316bb4f8654466d684b8a`  
		Last Modified: Fri, 22 Apr 2022 03:55:32 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba940d517ddac55ea1379c9f2cff56d93e8aa91f44e1303dc4a4261a1ef6810`  
		Last Modified: Fri, 22 Apr 2022 03:55:36 GMT  
		Size: 22.9 MB (22859264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d0e911a94a4c436c6eaac9f332755592ed90fe0be25b9af63f9a2f49ba05f158
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255862942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb412fe1d9860ee058814b5c7aaa792e3483edb85047600538597591910b5b63`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:52 GMT
ADD file:1e18e22e32f06a7e93275cf3a2eb2a1d3892be27628bdae2de4b2aadb992bd50 in / 
# Fri, 29 Apr 2022 22:49:53 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:32:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:32:29 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:32:30 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:32:31 GMT
ENV ROS_DISTRO=rolling
# Sat, 30 Apr 2022 00:33:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:19 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:33:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:33:21 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:34:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:34:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:34:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:34:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b84950154c181a602d2e93b68e84660f96dc78f94ae36f3df2db8d5701abb6a5`  
		Last Modified: Fri, 29 Apr 2022 22:52:07 GMT  
		Size: 28.4 MB (28376457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4339dcf07e4fd919aa10dc0e01fb8f44184f74bf6baf5aef6e8fdd30f5e603`  
		Last Modified: Sat, 30 Apr 2022 00:43:58 GMT  
		Size: 1.2 MB (1192681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0db3fdf5b04e561797500fc1d19d79a37ca0586b71bee71ce2acaee153d4dee`  
		Last Modified: Sat, 30 Apr 2022 00:43:56 GMT  
		Size: 3.6 MB (3594435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af71d8cd404a31e077722270696cf33d59cff54d35c9dad864264138bc3ac`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e01b1250d40bc108a995e5fc6c1630b0abdbfff31529a87a4096271f2a6115`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ae3a3b720aed16343416b9bb5eea4967087c21dee2c39948d0ca129037dd4f`  
		Last Modified: Sat, 30 Apr 2022 00:44:12 GMT  
		Size: 103.8 MB (103773129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be65bd445679ba8af650c6dd6742dc9a2d31871d4bac42819d92857e3a5892d`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ea6f66376f6e1da9bb78a2df21de836c30ea4379d4641ce9b7a1dfce84b6b4`  
		Last Modified: Sat, 30 Apr 2022 00:44:38 GMT  
		Size: 96.2 MB (96157476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a8f645f0a9603e60db84a3de8b50d76b5e58918fc81c2b4b19cea51a1a2a1`  
		Last Modified: Sat, 30 Apr 2022 00:44:24 GMT  
		Size: 269.8 KB (269758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773bf167794f3f7af31d32325c1d102af94787ef5a9d239074eafe9b5582dc75`  
		Last Modified: Sat, 30 Apr 2022 00:44:24 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ab25ab23b7e441a52f03a15aec7da83f14b6f0843949bdbfee2aa35beb1787`  
		Last Modified: Sat, 30 Apr 2022 00:44:28 GMT  
		Size: 22.5 MB (22494500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:2041d3f0688a65037291d5c1a6bc03d509b7c295b1302f729d85f3566c8c5f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f0db02e019e6a4b3934609861d6bd367d4d7ea1a5e549d9d4bf61b728a97d80b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141823212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15372d384c90753f1c0cffc69b1eab508dc0a8431ff96bb212b34f8218fd8b52`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:26 GMT
ADD file:76dd6cab5732b31272279bb8868954cbbecf591f596f0c318524454e95eabfb9 in / 
# Thu, 21 Apr 2022 23:00:26 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:42:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:45 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:42:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:42:46 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:42:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:42:46 GMT
ENV ROS_DISTRO=rolling
# Fri, 22 Apr 2022 03:44:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:44:24 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:44:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:44:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8527c5f86ecc162d68a9d38c8f4c6a6443158c67417e8bc2c3cea9f3868394eb`  
		Last Modified: Thu, 21 Apr 2022 23:02:00 GMT  
		Size: 30.4 MB (30421209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341919f757e419f6142944f5ea95c19b61bf1ff648abdfff94ed8c99c0bfd52c`  
		Last Modified: Fri, 22 Apr 2022 03:55:07 GMT  
		Size: 1.2 MB (1191091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0455c8ef748e7b3e35f60511f8e8053ee76492c9a72a5afd00d55d351854556f`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 3.8 MB (3826746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b72761451ff916be9282f71adece9e357fc9710e86559b986d1f01583fd312`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3452459740e87b470a88f20122447689e1640a2b865eb50f2f4a866ad75d391`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2037c4fb46b3cec9022f679d45d7834d6c89ac325348efc7af3d5d92bcd7658`  
		Last Modified: Fri, 22 Apr 2022 03:55:22 GMT  
		Size: 106.4 MB (106381750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0221e7e4829eedc9594c53ce3492bccdc39ea2c1b77da83a10fdb689100c68`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fbdfb4cc6c578f26264bd25d1f0dee739ebf7c799a6051764b6982e235e92f0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136939071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939b7344405c1ba5f1bad7ee3277b1574d8adec1f2eb8b1b7f26b50344646ed2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:52 GMT
ADD file:1e18e22e32f06a7e93275cf3a2eb2a1d3892be27628bdae2de4b2aadb992bd50 in / 
# Fri, 29 Apr 2022 22:49:53 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:32:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:32:29 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:32:30 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:32:31 GMT
ENV ROS_DISTRO=rolling
# Sat, 30 Apr 2022 00:33:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:19 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:33:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:33:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b84950154c181a602d2e93b68e84660f96dc78f94ae36f3df2db8d5701abb6a5`  
		Last Modified: Fri, 29 Apr 2022 22:52:07 GMT  
		Size: 28.4 MB (28376457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4339dcf07e4fd919aa10dc0e01fb8f44184f74bf6baf5aef6e8fdd30f5e603`  
		Last Modified: Sat, 30 Apr 2022 00:43:58 GMT  
		Size: 1.2 MB (1192681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0db3fdf5b04e561797500fc1d19d79a37ca0586b71bee71ce2acaee153d4dee`  
		Last Modified: Sat, 30 Apr 2022 00:43:56 GMT  
		Size: 3.6 MB (3594435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af71d8cd404a31e077722270696cf33d59cff54d35c9dad864264138bc3ac`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e01b1250d40bc108a995e5fc6c1630b0abdbfff31529a87a4096271f2a6115`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ae3a3b720aed16343416b9bb5eea4967087c21dee2c39948d0ca129037dd4f`  
		Last Modified: Sat, 30 Apr 2022 00:44:12 GMT  
		Size: 103.8 MB (103773129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be65bd445679ba8af650c6dd6742dc9a2d31871d4bac42819d92857e3a5892d`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-jammy`

```console
$ docker pull ros@sha256:2041d3f0688a65037291d5c1a6bc03d509b7c295b1302f729d85f3566c8c5f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:f0db02e019e6a4b3934609861d6bd367d4d7ea1a5e549d9d4bf61b728a97d80b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141823212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15372d384c90753f1c0cffc69b1eab508dc0a8431ff96bb212b34f8218fd8b52`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:26 GMT
ADD file:76dd6cab5732b31272279bb8868954cbbecf591f596f0c318524454e95eabfb9 in / 
# Thu, 21 Apr 2022 23:00:26 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:42:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:45 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:42:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:42:46 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:42:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:42:46 GMT
ENV ROS_DISTRO=rolling
# Fri, 22 Apr 2022 03:44:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:44:24 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:44:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:44:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8527c5f86ecc162d68a9d38c8f4c6a6443158c67417e8bc2c3cea9f3868394eb`  
		Last Modified: Thu, 21 Apr 2022 23:02:00 GMT  
		Size: 30.4 MB (30421209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341919f757e419f6142944f5ea95c19b61bf1ff648abdfff94ed8c99c0bfd52c`  
		Last Modified: Fri, 22 Apr 2022 03:55:07 GMT  
		Size: 1.2 MB (1191091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0455c8ef748e7b3e35f60511f8e8053ee76492c9a72a5afd00d55d351854556f`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 3.8 MB (3826746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b72761451ff916be9282f71adece9e357fc9710e86559b986d1f01583fd312`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3452459740e87b470a88f20122447689e1640a2b865eb50f2f4a866ad75d391`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2037c4fb46b3cec9022f679d45d7834d6c89ac325348efc7af3d5d92bcd7658`  
		Last Modified: Fri, 22 Apr 2022 03:55:22 GMT  
		Size: 106.4 MB (106381750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0221e7e4829eedc9594c53ce3492bccdc39ea2c1b77da83a10fdb689100c68`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fbdfb4cc6c578f26264bd25d1f0dee739ebf7c799a6051764b6982e235e92f0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136939071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939b7344405c1ba5f1bad7ee3277b1574d8adec1f2eb8b1b7f26b50344646ed2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:52 GMT
ADD file:1e18e22e32f06a7e93275cf3a2eb2a1d3892be27628bdae2de4b2aadb992bd50 in / 
# Fri, 29 Apr 2022 22:49:53 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:32:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:32:29 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:32:30 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:32:31 GMT
ENV ROS_DISTRO=rolling
# Sat, 30 Apr 2022 00:33:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:19 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:33:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:33:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b84950154c181a602d2e93b68e84660f96dc78f94ae36f3df2db8d5701abb6a5`  
		Last Modified: Fri, 29 Apr 2022 22:52:07 GMT  
		Size: 28.4 MB (28376457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4339dcf07e4fd919aa10dc0e01fb8f44184f74bf6baf5aef6e8fdd30f5e603`  
		Last Modified: Sat, 30 Apr 2022 00:43:58 GMT  
		Size: 1.2 MB (1192681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0db3fdf5b04e561797500fc1d19d79a37ca0586b71bee71ce2acaee153d4dee`  
		Last Modified: Sat, 30 Apr 2022 00:43:56 GMT  
		Size: 3.6 MB (3594435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af71d8cd404a31e077722270696cf33d59cff54d35c9dad864264138bc3ac`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e01b1250d40bc108a995e5fc6c1630b0abdbfff31529a87a4096271f2a6115`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ae3a3b720aed16343416b9bb5eea4967087c21dee2c39948d0ca129037dd4f`  
		Last Modified: Sat, 30 Apr 2022 00:44:12 GMT  
		Size: 103.8 MB (103773129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be65bd445679ba8af650c6dd6742dc9a2d31871d4bac42819d92857e3a5892d`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

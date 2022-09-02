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

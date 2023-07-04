## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:280e3b2923ac2b7a741cf65c1f8a32ad5f3bdc4a588ab6221a5df140a0e13a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:ec8953a89ab8dfe1738c60f681534607bdcc857bf31b4ea08287f0591c2c037e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **952.3 MB (952254277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f1eea91da5ca26679b3aca584a5c533050fd4bfba081b9fd25a24246217f1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 03:41:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:41:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:41:43 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Jun 2023 03:41:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 16 Jun 2023 03:41:44 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jun 2023 03:41:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Jun 2023 03:41:45 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Jun 2023 03:43:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:43:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Jun 2023 03:43:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Jun 2023 03:43:11 GMT
CMD ["bash"]
# Fri, 16 Jun 2023 03:44:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:44:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Jun 2023 03:44:08 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Jun 2023 03:44:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:52:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b169f458fb68eaad31436347ddfc7e25dd97c37d8cb63f22e84e7f95d4fa19b`  
		Last Modified: Fri, 16 Jun 2023 04:03:37 GMT  
		Size: 1.2 MB (1212828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bf80c9011de772b9b9ef6bbfe82a4f648cba6a09b044082641c5a232558d5a`  
		Last Modified: Fri, 16 Jun 2023 04:03:35 GMT  
		Size: 3.8 MB (3828743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa9834c66b60b85dc4ddfef495ea84f47531b25092c93ce7cea642ccf57ef2b`  
		Last Modified: Fri, 16 Jun 2023 04:03:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11d2a49f11b048e53a72852bd937876370b9ba2c2448fff57054b14f67466f0`  
		Last Modified: Fri, 16 Jun 2023 04:03:34 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbaaf0d07ce9923344bb5649335dc9cb1d9d75b9072a4184813e3b6e96cb98c`  
		Last Modified: Fri, 16 Jun 2023 04:03:50 GMT  
		Size: 106.3 MB (106346667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40d88d0af61448739222d5fd5bd85608277cce56a574273ff20a89fafee8515`  
		Last Modified: Fri, 16 Jun 2023 04:03:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06384a5e54f3042dafc74cc55288bce3a86696a3c17cf79b130581cdd63910b`  
		Last Modified: Fri, 16 Jun 2023 04:04:12 GMT  
		Size: 97.9 MB (97949822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e750d54d785aa1696c573420a62fbb7249cde12d2084a2fab4201df081b90eb7`  
		Last Modified: Fri, 16 Jun 2023 04:03:59 GMT  
		Size: 304.7 KB (304732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d351a048bcc5f2d84a3e60e35390a6f29c2da9dd56e1d7478de0b6015895c42`  
		Last Modified: Fri, 16 Jun 2023 04:03:59 GMT  
		Size: 2.4 KB (2410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d66d96470f76515998af23908ea849dca005a88cdf897bde234aa1a43bdd548`  
		Last Modified: Fri, 16 Jun 2023 04:04:03 GMT  
		Size: 23.1 MB (23082395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ee2fdbc06c020771b437e47cef5bc8e78aa40bd8ff770ee5c16e8dec7929b6`  
		Last Modified: Fri, 16 Jun 2023 04:05:52 GMT  
		Size: 689.1 MB (689093223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4d8fb695550857c8570e04c0a51fcbda56719acb15180bb5f97cc33133fd1de4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **913.7 MB (913735876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0f1a5675115b29c71228e209141c46fd87b090a0b583f56e41b00f2c648e9b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 14:39:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:39:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:39:32 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 04 Jul 2023 14:39:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 14:39:33 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 14:39:33 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 14:39:33 GMT
ENV ROS_DISTRO=humble
# Tue, 04 Jul 2023 14:41:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:41:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 14:41:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 14:41:06 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:41:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:41:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 14:41:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 14:42:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:52:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00229127f6e92c07e3d74389e863ed6853d2d18643b36b4305c0618bd0dde009`  
		Last Modified: Tue, 04 Jul 2023 15:02:02 GMT  
		Size: 1.2 MB (1214643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b203d955e7643d1bb7ec9891155ddb1401e9f8ef11e41eff2ea80a7477a1e4a2`  
		Last Modified: Tue, 04 Jul 2023 15:02:00 GMT  
		Size: 3.8 MB (3802027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c278f102957a8f2e4cef72c46fb72240db242ec7800b4e9f3660cdd59adb5d`  
		Last Modified: Tue, 04 Jul 2023 15:01:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b369fa41d7f7a70ee18742f04da6ab36f01e9331cd686a3fc0d10f2a61df1ee`  
		Last Modified: Tue, 04 Jul 2023 15:01:59 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc99b708e63ea51d08155711080144b68401240806daf3d55ff31da8ce2e6e8`  
		Last Modified: Tue, 04 Jul 2023 15:02:14 GMT  
		Size: 104.1 MB (104091352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4587e83797ba402344f156014188711bc267dad06b4fc07b9b76d84206961887`  
		Last Modified: Tue, 04 Jul 2023 15:01:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4681cb50e4211cf1a6641009dd51e6330ee41ec7d56c69974b08bcad3e1eb97`  
		Last Modified: Tue, 04 Jul 2023 15:02:33 GMT  
		Size: 95.6 MB (95583335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64814832cf8516f200bd7dd874fa74752b972925ab9c3589cff205384d75de09`  
		Last Modified: Tue, 04 Jul 2023 15:02:23 GMT  
		Size: 307.1 KB (307139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22ee3968485d390f331fe27b0544cdaa0341b0cf480ee4322c0dc756fe3160c`  
		Last Modified: Tue, 04 Jul 2023 15:02:23 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e450a263466aac0036b7b14cb06363d88c97575eb95b4d03e7cd1541305e43b6`  
		Last Modified: Tue, 04 Jul 2023 15:02:26 GMT  
		Size: 22.5 MB (22503697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89358fb3d71856b83b2a7b91f147e47a9bd2f8d75266587d9a3063d4df9cc987`  
		Last Modified: Tue, 04 Jul 2023 15:04:07 GMT  
		Size: 657.8 MB (657837811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

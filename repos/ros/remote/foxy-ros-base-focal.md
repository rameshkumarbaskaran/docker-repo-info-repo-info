## `ros:foxy-ros-base-focal`

```console
$ docker pull ros@sha256:48a407daea36ad72febe0c1cd90a5cbf4c417794100f0b9a3031d1f616141775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:5991759125bfb3b5f7b99ea8d89519c620973f2fafe9f578b06683a187dd4b90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250986541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9001fb3c6d9cbfb1fc4f48fbc9912c8a1f645faf74fc77738e7f39a8277d13a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:00:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:00:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:11:43 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 18 Apr 2023 01:11:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 18 Apr 2023 01:11:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Apr 2023 01:11:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 18 Apr 2023 01:11:44 GMT
ENV ROS_DISTRO=foxy
# Tue, 18 Apr 2023 01:12:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:12:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 18 Apr 2023 01:12:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 18 Apr 2023 01:12:40 GMT
CMD ["bash"]
# Tue, 18 Apr 2023 01:13:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:13:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 18 Apr 2023 01:13:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 18 Apr 2023 01:13:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5ff3f6c5dd326a8361d5d9fba50621a210a6b840cadcc97c516817cb8cf8d7`  
		Last Modified: Tue, 18 Apr 2023 01:15:00 GMT  
		Size: 1.2 MB (1157164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b302bcd474554096ffccaf8412038965be0feec446d247de776919747c75591`  
		Last Modified: Tue, 18 Apr 2023 01:14:59 GMT  
		Size: 5.6 MB (5553578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11384cc19c203f12069b104485229b1cde3e07fb646ecb09f115a1ed23251042`  
		Last Modified: Tue, 18 Apr 2023 01:17:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e1899a5dd0280e2bbb519c2cede595b7705867c7e57a775237ac5d972976d`  
		Last Modified: Tue, 18 Apr 2023 01:17:26 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed172a7f8a3773d473ad96809401a410d4517ae43bc854da56d2c3ed28f0ee8`  
		Last Modified: Tue, 18 Apr 2023 01:17:45 GMT  
		Size: 120.4 MB (120409529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697c4bfe41b1cdea0ed9cd295f48b4d9acb1711ae5a550c0b0c460c903020520`  
		Last Modified: Tue, 18 Apr 2023 01:17:26 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275738f8603356f715759926c672904eafa8bfac12a6f4fc1bb25f30a2f2e67e`  
		Last Modified: Tue, 18 Apr 2023 01:18:03 GMT  
		Size: 73.3 MB (73341056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0cfeddf32468988708b8205f0dd73996e224c00857773fa9557bdbfa385e4d`  
		Last Modified: Tue, 18 Apr 2023 01:17:54 GMT  
		Size: 260.0 KB (259961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3049fa8b21143456bf6302da9c1f5d27a1c4f9e8b05028511aa67f3bbabd481`  
		Last Modified: Tue, 18 Apr 2023 01:17:53 GMT  
		Size: 2.4 KB (2427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288a0278b454639d3064fd38db41ae5a3d05e16ffa4bf223b9e78fb59d37f8a6`  
		Last Modified: Tue, 18 Apr 2023 01:17:57 GMT  
		Size: 21.7 MB (21681848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:faf71017f30cd4a71e27447d574207fc5e10da8cc6546b983c3fff6ec6a84477
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226807812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c72845950c710d7c343b5e65337dd70242701e34b0340a3d4ee9324c22d69c7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:10:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:10:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:23:12 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 16 Mar 2023 03:23:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Mar 2023 03:23:13 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 03:23:13 GMT
ENV LC_ALL=C.UTF-8
# Thu, 16 Mar 2023 03:23:13 GMT
ENV ROS_DISTRO=foxy
# Thu, 16 Mar 2023 03:24:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:24:06 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 16 Mar 2023 03:24:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 16 Mar 2023 03:24:06 GMT
CMD ["bash"]
# Thu, 16 Mar 2023 03:24:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:24:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 16 Mar 2023 03:24:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 16 Mar 2023 03:24:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c235c7a3c272479c47e3fdeef457877dd1bce12f4b4d8726aeb2b8e16d6acae4`  
		Last Modified: Thu, 16 Mar 2023 03:46:17 GMT  
		Size: 1.2 MB (1155462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e62e51f71a010b6fdbdb16725b3bbfca6a13fca1e447d14e311d361db90f4`  
		Last Modified: Thu, 16 Mar 2023 03:46:15 GMT  
		Size: 5.5 MB (5532807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42860775fce781d98f8f21abfafa48660e634182b69b05266851498055971a82`  
		Last Modified: Thu, 16 Mar 2023 03:48:28 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7191287fc71fa37ace07c3fb721fe8b0df2516866da1e7b98f48aa71b8bdb94e`  
		Last Modified: Thu, 16 Mar 2023 03:48:28 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e24d2145f0cc2cf9a85047ab49b1f2f4b457e7b81b534c1bfc25642cd3a10fd`  
		Last Modified: Thu, 16 Mar 2023 03:48:43 GMT  
		Size: 104.6 MB (104568150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27f4054f4fcc5c1a7c641b6a19891c7fe042a2d4ba353b8eb7d094b1ccde304`  
		Last Modified: Thu, 16 Mar 2023 03:48:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b61acdd97d95df9976326ba8a1dc79a739c367e9d0232e2ae3560909a891af4`  
		Last Modified: Thu, 16 Mar 2023 03:48:59 GMT  
		Size: 67.7 MB (67684730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef11b685a5e9052a6bd9772d42b4900972bc1037ca8648eae13801e200578820`  
		Last Modified: Thu, 16 Mar 2023 03:48:52 GMT  
		Size: 279.9 KB (279917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8d4285dfe20611b685fe67cf842b70a9e8b6409de0e9d12bcc27174be70897`  
		Last Modified: Thu, 16 Mar 2023 03:48:51 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab10b5ea657202d97bef2d89bc8b1d0d91f7b99e5f04ee9ef87100edfc1dccd`  
		Last Modified: Thu, 16 Mar 2023 03:48:54 GMT  
		Size: 20.4 MB (20385758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

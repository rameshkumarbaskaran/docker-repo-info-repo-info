## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:138ead33eec3bcfafaa4595e4b9a6929997fa8e7e418f14366f43773e9f88b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:0b8d4b1d363a67cf3c95eb289f00a428230aa794032ef06e274235f1ec22a904
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268601984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a591daad46f014598854c581bde6d5327ea870515c178f9525d9fd4813a8e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 21:45:33 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:45:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:45:39 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 03 May 2023 21:45:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 May 2023 21:45:41 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 21:45:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 May 2023 21:57:22 GMT
ENV ROS_DISTRO=rolling
# Wed, 03 May 2023 21:58:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:58:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 03 May 2023 21:58:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 May 2023 21:58:29 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:59:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:59:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 May 2023 21:59:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 03 May 2023 21:59:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d709c34b032e9c25f3ef7dbc9cc5be0ab87d014082e04d1f4a5d20e2970446b`  
		Last Modified: Wed, 03 May 2023 22:04:52 GMT  
		Size: 1.2 MB (1239802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58a8c29b4dfa9054fe01f5590245b9ad2e27c309027d00b628451f55bfde59c`  
		Last Modified: Wed, 03 May 2023 22:04:50 GMT  
		Size: 3.8 MB (3828401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707c946d99b6f2ae4da84c6c0af0b3204f17c5371e0ef1e1968fc20d3c812123`  
		Last Modified: Wed, 03 May 2023 22:04:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89451566146a587c0f7bde9c5bd208af5e73072fa556ff6ad6ac85c213406cb6`  
		Last Modified: Wed, 03 May 2023 22:04:49 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7285dfa96f611fd7adc01ba69ac7e4a2f1908b2e0789b6af59c697d81ef586ac`  
		Last Modified: Wed, 03 May 2023 22:07:39 GMT  
		Size: 124.1 MB (124111474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6607aaf2a2bb9ae2485f009f0e839192b6a1e5a9236fef31b92e88e11da8412`  
		Last Modified: Wed, 03 May 2023 22:07:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d7c154e1b997c1b21c7505dfb66305a3062256015ec7a7890e1b6ef3eacd3f`  
		Last Modified: Wed, 03 May 2023 22:07:57 GMT  
		Size: 85.0 MB (84998074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c86a7baccad3d6c956fc7871ccfb6668dd150271b737949ff71f9c1c4b91ad3`  
		Last Modified: Wed, 03 May 2023 22:07:47 GMT  
		Size: 283.9 KB (283944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c84c738f9e7df26ff7d69e76c60b208ac7bf7b078a0ef362fd027cb97710f`  
		Last Modified: Wed, 03 May 2023 22:07:47 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b11880a7eca1765742848615c1ab9d3c6452d148e5be64bddbfe47e82b7e497`  
		Last Modified: Wed, 03 May 2023 22:07:50 GMT  
		Size: 23.7 MB (23705240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:553531ee55347d9190085cdb229e0abbfb50e580afd1e782fd1048a8323003e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263245418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1afae2f1ad78c47fa927576dd5f061e7887cad9199f59ec98a2e782553d171`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:19:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:20:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:20:18 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Jun 2023 00:20:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Jun 2023 00:20:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Jun 2023 00:20:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Jun 2023 00:37:33 GMT
ENV ROS_DISTRO=rolling
# Fri, 02 Jun 2023 00:38:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:38:14 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Jun 2023 00:38:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Jun 2023 00:38:14 GMT
CMD ["bash"]
# Fri, 02 Jun 2023 00:38:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:38:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Jun 2023 00:38:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Jun 2023 00:38:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755c90e9cf79faad5cb53bf52c5426df1ff04c218894ffbb077e2524f6d717e2`  
		Last Modified: Fri, 02 Jun 2023 00:43:37 GMT  
		Size: 1.2 MB (1212932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35deec7a88f66396ce147c78c621f166491b3bb0d43295ac2a27879c9d37369e`  
		Last Modified: Fri, 02 Jun 2023 00:43:35 GMT  
		Size: 3.8 MB (3800450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ef7ef73bca581875e598a71ca009ce9fded1b1da4ce3b0c008979125eb05d7`  
		Last Modified: Fri, 02 Jun 2023 00:43:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037d33ca89bd5d376d834aebec1592a65631f40a1423a08a248d2b1c8df162c6`  
		Last Modified: Fri, 02 Jun 2023 00:43:34 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ae22005ca62c74f2251e85c2a21524375ba0becb6d508e2607b5db093ddfe0`  
		Last Modified: Fri, 02 Jun 2023 00:48:11 GMT  
		Size: 123.7 MB (123718906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de066b41a04e9f87e1fd43528b4563aa6325aaee7ec59e952fba8c66d3d89e51`  
		Last Modified: Fri, 02 Jun 2023 00:47:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cc556d09a17f3f30a56f6365f867bb6a45417bb6d75f2fdc0e4fd690cd799a`  
		Last Modified: Fri, 02 Jun 2023 00:48:27 GMT  
		Size: 82.7 MB (82736060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef615f81becaa25357eae9ec1e4a4ce4877206b83ec281b7ca4c6f097133649`  
		Last Modified: Fri, 02 Jun 2023 00:48:20 GMT  
		Size: 287.4 KB (287404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565c8add78ef1da942f3b8febf52b86308502cad2b4a085b091d57a49211a87c`  
		Last Modified: Fri, 02 Jun 2023 00:48:19 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e0a197629382875eb6a739f531a299bd43a2b6bd109b33fc97adb8c6a16015`  
		Last Modified: Fri, 02 Jun 2023 00:48:22 GMT  
		Size: 23.1 MB (23095775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

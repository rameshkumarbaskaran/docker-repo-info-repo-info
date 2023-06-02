## `ros:latest`

```console
$ docker pull ros@sha256:2ef23daf67731f2f1f27b0a3af321c15b1e499cf521a31f0e4a3b036a5384b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:f05e713cd384afe798581f9bbf312a249102fb37a184049b9457e9fef90d137e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263174534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e9065680771dc75b9640d663e4e5c2c96952c91b485681b427be72ed07e5e4`
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
# Wed, 03 May 2023 21:45:41 GMT
ENV ROS_DISTRO=humble
# Wed, 03 May 2023 21:47:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:47:17 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 03 May 2023 21:47:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 May 2023 21:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:48:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:48:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 May 2023 21:48:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 03 May 2023 21:49:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:cde6a04e024906cded5edf825e781c98cf96fbbf94fa12b76c330722940eceb8`  
		Last Modified: Wed, 03 May 2023 22:05:05 GMT  
		Size: 106.3 MB (106336297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9588c9c20d7b8f44868b7fc58557ac21f8e7e305a1d876de9f1074e10f95050`  
		Last Modified: Wed, 03 May 2023 22:04:49 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ae8aa1e91cbff4c3f988a146ffc0206d3e1f66955d42de907bb2e1422ac312`  
		Last Modified: Wed, 03 May 2023 22:05:27 GMT  
		Size: 98.0 MB (97953962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563b38330c500c2d1dc3ba3fc3436efb4fe69c77e3eefb798da0dbf2f045741b`  
		Last Modified: Wed, 03 May 2023 22:05:14 GMT  
		Size: 300.1 KB (300107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71be3bc7a9e9be52aa054f3abbfe1466bad3c982a4b5df0139365a1e8d8aa99f`  
		Last Modified: Wed, 03 May 2023 22:05:14 GMT  
		Size: 2.4 KB (2422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce9eacb30f5cbc4a5b4fef0e07ec3d7e292008bb2429d9a7c5b47c1f424c0c2`  
		Last Modified: Wed, 03 May 2023 22:05:18 GMT  
		Size: 23.1 MB (23080914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3140912829e183885762fe98c7ce87034f7085349558be363fb5906ed2d79f06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257976334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c858e9f6289e8a84ea7110ea4ddcc910968894db3701a237cc83b0ce2fd37be`
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
# Fri, 02 Jun 2023 00:20:19 GMT
ENV ROS_DISTRO=humble
# Fri, 02 Jun 2023 00:22:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:22:14 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Jun 2023 00:22:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Jun 2023 00:22:14 GMT
CMD ["bash"]
# Fri, 02 Jun 2023 00:23:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:23:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Jun 2023 00:23:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Jun 2023 00:24:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:636334b7d9bfab9fe9d103e17da49192beda0a33c3aa20bb74d216ae8fca27f9`  
		Last Modified: Fri, 02 Jun 2023 00:43:48 GMT  
		Size: 106.2 MB (106199197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4cf4fc7798d9f02c0a8b5d6b9b0147ad310eadf884def4147b317343aca2c7`  
		Last Modified: Fri, 02 Jun 2023 00:43:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8188ec43a23c801ed34a1afcf1a377e04b100236bc57c37a1679e24b7cfca`  
		Last Modified: Fri, 02 Jun 2023 00:44:08 GMT  
		Size: 95.6 MB (95566741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34850de15b46b5eb68fa77777066fe77cb9d2728e8b23d8713b280f6f42ad1f4`  
		Last Modified: Fri, 02 Jun 2023 00:43:56 GMT  
		Size: 303.7 KB (303717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74542b0b6699eb64054ee25efb05e5c048266dbab424d1574117f34ee1a1ac5c`  
		Last Modified: Fri, 02 Jun 2023 00:43:56 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c68c7d0ab7ff92686bd6ed4c3818d8ac62548f9cdbc8e487c6d5a947e20d47`  
		Last Modified: Fri, 02 Jun 2023 00:44:00 GMT  
		Size: 22.5 MB (22499425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

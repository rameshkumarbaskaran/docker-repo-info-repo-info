## `ros:rolling-perception-jammy`

```console
$ docker pull ros@sha256:d79ccd7561dcacb4b4fa66ca6e7ee080ff1007589e08d752dd6f1689b068df2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:c707693a17cb1202f7d3b768375b47a05a0b094774da0232c28521a08f8d3f7d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1088044067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6945dfdc6002b8534b26426c1e357864873a77407d82cd9b9eeb4e39ea43ba39`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:07:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:07:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:07:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 02 Nov 2022 19:07:15 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Nov 2022 19:07:15 GMT
ENV LANG=C.UTF-8
# Wed, 02 Nov 2022 19:07:15 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Nov 2022 19:19:39 GMT
ENV ROS_DISTRO=rolling
# Wed, 02 Nov 2022 19:20:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:20:21 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 02 Nov 2022 19:20:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Nov 2022 19:20:22 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:20:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:20:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Nov 2022 19:20:53 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 02 Nov 2022 19:21:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:23:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0e309791760cb897f78d6ecdca3ecfa35842379a8f68578fae97e3ed231487`  
		Last Modified: Wed, 02 Nov 2022 19:24:38 GMT  
		Size: 1.2 MB (1174801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda1968667a68200295ab81fbbe7a340eefffe28e7765ccce0ac08e4e840058f`  
		Last Modified: Wed, 02 Nov 2022 19:24:35 GMT  
		Size: 3.8 MB (3828037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80ba109583179b86f91d9cef7488e67ac530a78c620ebe127cde962b001e8bf`  
		Last Modified: Wed, 02 Nov 2022 19:24:35 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00beac66efa2733f4c56752491978562f4fd073a619736ec1ee66f17d44324c7`  
		Last Modified: Wed, 02 Nov 2022 19:24:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11614817332af0948a51dccc0ac2fec8909f110de95b78985b29b8c3f7e970c1`  
		Last Modified: Wed, 02 Nov 2022 19:27:43 GMT  
		Size: 106.4 MB (106391794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fa3a122b2ab87848b5d17fb2971645d70a05f26186dd83469908b5fc2782c9`  
		Last Modified: Wed, 02 Nov 2022 19:27:26 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c81e1547a26a3218c2267d44cb59398accac32565a64a6526e08ec328e7c02`  
		Last Modified: Wed, 02 Nov 2022 19:28:07 GMT  
		Size: 97.9 MB (97877379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858964a9bd3e2e8940d46dbde3c2ce321709ef75f592a61f57a5ca4e07fa2831`  
		Last Modified: Wed, 02 Nov 2022 19:27:53 GMT  
		Size: 289.4 KB (289400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0640f0773691621eb15edf8ccd1698f345f1b4699b5af20ff717c88bb98c9829`  
		Last Modified: Wed, 02 Nov 2022 19:27:53 GMT  
		Size: 2.4 KB (2428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed0d6a369f889af68dd4862416c0e68f68a9969b60471cce35083066e2f6016`  
		Last Modified: Wed, 02 Nov 2022 19:27:57 GMT  
		Size: 23.2 MB (23226886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7436de3271fc8bff591a3ebe7e1b4aa8f00c58b5b3eef5caff71c6f00296aa91`  
		Last Modified: Wed, 02 Nov 2022 19:29:58 GMT  
		Size: 824.8 MB (824825317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:063df331521058ec5e22196b792af1de98131252038c2bafffd7549eec23fbd1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1038299070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dea3bee71f251642e1c5303029eabc420bcaf8bf30b36f3c2caa7b6f1417e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:21:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:21:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:21:31 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 02 Nov 2022 19:21:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Nov 2022 19:21:33 GMT
ENV LANG=C.UTF-8
# Wed, 02 Nov 2022 19:21:33 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Nov 2022 19:35:10 GMT
ENV ROS_DISTRO=rolling
# Wed, 02 Nov 2022 19:35:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:35:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 02 Nov 2022 19:35:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Nov 2022 19:35:46 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:36:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:36:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Nov 2022 19:36:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 02 Nov 2022 19:36:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:38:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11760287344b02d03930af87d27c6b9dc1acc8842adc4df018fbc979edafe07e`  
		Last Modified: Wed, 02 Nov 2022 19:39:41 GMT  
		Size: 1.2 MB (1175024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57286bbac2dc9c1c64117272c5610b0ccabf76c64c0d83ada53661e5bd6c7235`  
		Last Modified: Wed, 02 Nov 2022 19:39:38 GMT  
		Size: 3.8 MB (3799957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe77194dbcb3cb1b9324930f565438ef05948cba7bb01a453e85a976f50cb1f`  
		Last Modified: Wed, 02 Nov 2022 19:39:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeeadbd7d6fc1cd7ec48cf66192a01ee8304012593c12a1aaa6934e051205a1`  
		Last Modified: Wed, 02 Nov 2022 19:39:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe01c46c01bb82aca483b1c908f1f744fbf5f514d7bc29127dc2d13c92c43fd`  
		Last Modified: Wed, 02 Nov 2022 19:42:12 GMT  
		Size: 104.1 MB (104124486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b03d2faf31fcaa3607b8d6642d0d7aebc0c888fc741c6b7477337a853bbe199`  
		Last Modified: Wed, 02 Nov 2022 19:41:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b049aee909eee07c3fa6b0c4f58011d3c0b7fe37b557f63a4d7e9478d6426c`  
		Last Modified: Wed, 02 Nov 2022 19:42:35 GMT  
		Size: 95.5 MB (95469657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8551cbc2119bf668a98a498c06abc19d631c957ccee72b943b0e777f8d753d5`  
		Last Modified: Wed, 02 Nov 2022 19:42:22 GMT  
		Size: 289.4 KB (289398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0972484bf36906e4dd12b81cac9aa26295bd1d13f6838fab80ff0e64f43087fe`  
		Last Modified: Wed, 02 Nov 2022 19:42:22 GMT  
		Size: 2.4 KB (2426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541b9210000350e8829f8d302124c9abcadadb3cfe9864f3e7a31501dbe09394`  
		Last Modified: Wed, 02 Nov 2022 19:42:25 GMT  
		Size: 22.6 MB (22649561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab469ceb2c33ece432bce9e4ff984d91168e47ced17780485b30a39c0e2e6911`  
		Last Modified: Wed, 02 Nov 2022 19:43:59 GMT  
		Size: 782.4 MB (782403993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

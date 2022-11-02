## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:4fa7f4421a72e4623b9f580b28cc8669207c72fc4b2e887bad3d564b37939552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:9bf1a5b14fd9b2266178a5b95667fa2d8e861d335fdc9a0cdd7daf074f5939b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262837012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c144c1e970a33e387b79eb5588ae795fb1539a2de1d6a04750b10231258a960d`
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
# Wed, 02 Nov 2022 19:07:16 GMT
ENV ROS_DISTRO=humble
# Wed, 02 Nov 2022 19:08:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:08:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 02 Nov 2022 19:08:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Nov 2022 19:08:49 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:09:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:09:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Nov 2022 19:09:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 02 Nov 2022 19:10:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:74da46ef266f8ba534cb4dde37c2da0e270d1df1225aa78548cd0ab2b59ebd3a`  
		Last Modified: Wed, 02 Nov 2022 19:24:52 GMT  
		Size: 106.2 MB (106223087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed47f73c5e60922a92b32f660f99c0fb408f814b243dc7de94ace2dee1f33a09`  
		Last Modified: Wed, 02 Nov 2022 19:24:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0402bce15ac4ac00a43cf4b18e2406e71314ceaf39a5cc92ca1357413f87c029`  
		Last Modified: Wed, 02 Nov 2022 19:25:16 GMT  
		Size: 97.9 MB (97876837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a10a5da761f7db56ec4aa72c2922ceb8350bd90d044c31e8a21e0b1ccd7ec81`  
		Last Modified: Wed, 02 Nov 2022 19:25:02 GMT  
		Size: 295.6 KB (295632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74417cdbd164d16f1389679e94d83364890a14a1a7ec5ebaa726f5da444cc413`  
		Last Modified: Wed, 02 Nov 2022 19:25:02 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a9a4846b9f36feace908e6ce30cb0f05300da3e6854bb9b812dbbeb046f1de`  
		Last Modified: Wed, 02 Nov 2022 19:25:06 GMT  
		Size: 23.0 MB (23008159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5dcca810d0528bb38f274a1490eb803f4c87c0f33c071d05b72eb3d336c43888
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255534260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de556a740eb984e38e40b39bebcfb8c41d76603a7f4e16761e928f4c755edf3`
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
# Wed, 02 Nov 2022 19:21:33 GMT
ENV ROS_DISTRO=humble
# Wed, 02 Nov 2022 19:23:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:23:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 02 Nov 2022 19:23:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Nov 2022 19:23:07 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:23:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:24:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Nov 2022 19:24:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 02 Nov 2022 19:24:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:fae686679d19077688e7d06954e6e0f6754ffebb1e29ca823f62e08f8bd45825`  
		Last Modified: Wed, 02 Nov 2022 19:39:54 GMT  
		Size: 104.0 MB (103974109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9d5bd38521973ce8aaca4d8a7e6412e7d953b8984efc2bc83877aa3d1ac27c`  
		Last Modified: Wed, 02 Nov 2022 19:39:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470c91ae91f6f95613901a50063d68e3cff7271aa2bd22ee31e103e1a87a7b99`  
		Last Modified: Wed, 02 Nov 2022 19:40:16 GMT  
		Size: 95.5 MB (95469195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b70e807f120abf970bc2df136833c1349c7c57acf3d33be8789ba4bf1f48945`  
		Last Modified: Wed, 02 Nov 2022 19:40:05 GMT  
		Size: 295.6 KB (295631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6600ecdf5a14f5c94bd2a8d429da5e7f68adc291f97eb186d6be36d67d25fd3f`  
		Last Modified: Wed, 02 Nov 2022 19:40:05 GMT  
		Size: 2.4 KB (2409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baba103933cf30b26056f7a3af3942ec5f3bf5f7360286f5bd562e7c6f77ade7`  
		Last Modified: Wed, 02 Nov 2022 19:40:08 GMT  
		Size: 22.4 MB (22433366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

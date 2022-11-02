## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:6acf4ee414eb55e96cc3e02534357c0101c64b7ee81ed1ab02efc703d1bb314f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:ef150a962ad2b2bfe7dc29f22bc3eb784a041d3a0f374117d9a841780a55ee16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141653949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0cc72a40bf88f4527d256cdd115504d89e5e9c58f64683588332e63cdef1b6`
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

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c5ff981860c2649a53c87d612b762dfcca19dde2f45fffc719bc73f7e4a94abf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137333659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447465179f02058eab9bbb39d630e187e25c9f7819b918ddd8de8a0c10aeaf52`
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

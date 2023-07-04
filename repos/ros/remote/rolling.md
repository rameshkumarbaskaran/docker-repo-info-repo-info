## `ros:rolling`

```console
$ docker pull ros@sha256:c148024f1af44fde863facfe576f0aa510a0acaf0b1cd4785b4dc82e2562d965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:8497de34b4fe4b0df00111367044c08064e38fb418b1a33df6dd2bfdbdde7dc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268602115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ad0b914c35f8238a129916ac0034e4c3d1fbb552bb4d81abec3e7d61848578`
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
# Fri, 16 Jun 2023 03:56:05 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Jun 2023 03:56:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:56:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Jun 2023 03:56:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Jun 2023 03:56:45 GMT
CMD ["bash"]
# Fri, 16 Jun 2023 03:57:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:57:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Jun 2023 03:57:15 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Jun 2023 03:57:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:633a85d8b769a40385318439a6f0f1cad7c66a4116b0059a2c48c5c4342830bf`  
		Last Modified: Fri, 16 Jun 2023 04:08:46 GMT  
		Size: 124.1 MB (124135661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca2b18dfa14242c98eb39564e643e0d31b3be2d041ad51b216e2ca5ffe9fd95`  
		Last Modified: Fri, 16 Jun 2023 04:08:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171da17a95f927ae2c266d0d3de58b3fe4341927154d17e35721facfe3eac4f4`  
		Last Modified: Fri, 16 Jun 2023 04:09:06 GMT  
		Size: 85.0 MB (84994585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3468ea45a1acf261f7788a676e5842a16525bcd22e5c962fcda17578cea607d5`  
		Last Modified: Fri, 16 Jun 2023 04:08:55 GMT  
		Size: 288.4 KB (288357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a388e36085189206d87204728e5488d1842c2bb7aa1a1f220ee7918585cd7354`  
		Last Modified: Fri, 16 Jun 2023 04:08:55 GMT  
		Size: 2.4 KB (2405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9083010f25afa882d316ac8c410ca3dc4b74217062605e9d8013032f4dad4d20`  
		Last Modified: Fri, 16 Jun 2023 04:08:59 GMT  
		Size: 23.7 MB (23706079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:92b6a5001e47ae5066362bce6cf0c75cdaaa1c17bea7f899d81fd829fb12c7f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261190693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba98e4afa86a5d08fa70e2208765b1d52e3da8f382a4fc0fdae491d3cc88d7c`
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
# Tue, 04 Jul 2023 14:55:51 GMT
ENV ROS_DISTRO=rolling
# Tue, 04 Jul 2023 14:56:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:56:31 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 14:56:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 14:56:31 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:56:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:56:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 14:56:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 14:57:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:934fe752a2ee51b5ee65e779e62c11b4d010de2627c22aad530bf339442254a3`  
		Last Modified: Tue, 04 Jul 2023 15:06:40 GMT  
		Size: 121.6 MB (121646630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8b74a8b78fc888acf5353ade379044a3c4401d9cfa1a8a627099e7abc5aeb5`  
		Last Modified: Tue, 04 Jul 2023 15:06:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e7693b7f950c38c41729372425390b0d1c18a939a4f7f8768692d2758b6595`  
		Last Modified: Tue, 04 Jul 2023 15:06:56 GMT  
		Size: 82.7 MB (82737126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe56d8305f1e6ac0120f77b665376bfd0ac33a7a7ade6224b2fe24a936488c1d`  
		Last Modified: Tue, 04 Jul 2023 15:06:49 GMT  
		Size: 290.5 KB (290464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42311ceca794a942ff2ced664bbdadeb8b91734e8c4cdc435ae480583b4a6701`  
		Last Modified: Tue, 04 Jul 2023 15:06:48 GMT  
		Size: 2.4 KB (2405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f1ff2859eb8f182e0bac366d6ea3420a7f0f5201b0b28d1fb04ac1494fba49`  
		Last Modified: Tue, 04 Jul 2023 15:06:52 GMT  
		Size: 23.1 MB (23103969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

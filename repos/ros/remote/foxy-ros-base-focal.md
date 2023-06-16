## `ros:foxy-ros-base-focal`

```console
$ docker pull ros@sha256:e831548b8afc7ed345a1234196c07859ef8e0658c108f9a636aeab7f1940eeb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:09edbc23d95bb24b6d32b963ab231915dc5f53ebbe1a485ed80c3cc65ea30eb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251192581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3015a604ff49c3abae5860bb6178f04b00a5eb77f9e1cdd750eb71dc025aea1e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:57 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:58 GMT
ADD file:655d373cb551d0dd5d7867f88a4f98908dc3f16190986f693e88c423e6f21b8d in / 
# Mon, 05 Jun 2023 17:08:58 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:26:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:30:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:38:43 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Jun 2023 03:38:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 16 Jun 2023 03:38:44 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jun 2023 03:38:44 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Jun 2023 03:38:44 GMT
ENV ROS_DISTRO=foxy
# Fri, 16 Jun 2023 03:39:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:39:44 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Jun 2023 03:39:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Jun 2023 03:39:44 GMT
CMD ["bash"]
# Fri, 16 Jun 2023 03:40:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:40:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Jun 2023 03:40:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Jun 2023 03:40:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f0412dfb1aaea4892c13dab6f771bcd79641a4bdcb521ce881f5dcfc0df9a7a5`  
		Last Modified: Tue, 06 Jun 2023 09:20:27 GMT  
		Size: 28.6 MB (28580519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733ac94a680e3659eb88af9a60aa46eabe11de358d05cb19cf9d535083358650`  
		Last Modified: Fri, 16 Jun 2023 02:35:08 GMT  
		Size: 1.2 MB (1198722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c1fc3d4979a8cbea7949ab14296db71b51de166f987d5b8427b73ada3f02c0`  
		Last Modified: Fri, 16 Jun 2023 03:59:52 GMT  
		Size: 5.6 MB (5553799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3eff5a20cb49beeb08300ad92aa92769ff55b41f28ffa912b7629fc9508a40`  
		Last Modified: Fri, 16 Jun 2023 04:02:22 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654c3018234b0bd67a2e90bcf0f12b25a7181a9e32ea10b02709553e0adbb4b0`  
		Last Modified: Fri, 16 Jun 2023 04:02:22 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bcc91e8004fdeae5d2bab3940341e63b96c2766ef5f2f45d6a7b5ffe821366`  
		Last Modified: Fri, 16 Jun 2023 04:02:40 GMT  
		Size: 120.4 MB (120399883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744aeb09540670851e8f96bcacb101e8090a2534fbd1bb18eb684a89d58fc91d`  
		Last Modified: Fri, 16 Jun 2023 04:02:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182ad8f3506144a52c5952ed7d4be11cd8822f3ae42f6afb94ba566cdc6d52a8`  
		Last Modified: Fri, 16 Jun 2023 04:03:00 GMT  
		Size: 73.5 MB (73508184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce78a2bf00b16f0e8daf34d88fe85a54eab1a2821f5514eea122ce7bf1da2cbd`  
		Last Modified: Fri, 16 Jun 2023 04:02:50 GMT  
		Size: 264.4 KB (264358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a6aa18dfe5594b8571bdc1b66f3e981ec81f1ab084ffa08ce041987d10a31c`  
		Last Modified: Fri, 16 Jun 2023 04:02:50 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39897cab3d6cf7dc6fa6da86db99df7cc33048644cb1671b7258c48b1bfb353f`  
		Last Modified: Fri, 16 Jun 2023 04:02:53 GMT  
		Size: 21.7 MB (21682241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1c4343c9ddddf206a6dc17b91dfb227a1774210ffda7042ef1262c6ed0fbee45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227092960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e969df4ff2e47f3f6cc53502b5444887f067e2e8cc8f3c27148cba6f3fa05b26`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:07:59 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:07:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:02 GMT
ADD file:6c0661b94e27ede70ca2a8842bdab5bc26b9ae4760b17870eda9d595672795ff in / 
# Mon, 05 Jun 2023 17:08:02 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:04:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:05:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:19:22 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Jun 2023 01:19:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 16 Jun 2023 01:19:23 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jun 2023 01:19:24 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Jun 2023 01:19:24 GMT
ENV ROS_DISTRO=foxy
# Fri, 16 Jun 2023 01:20:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:20:17 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Jun 2023 01:20:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Jun 2023 01:20:17 GMT
CMD ["bash"]
# Fri, 16 Jun 2023 01:20:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:20:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Jun 2023 01:20:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Jun 2023 01:20:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29c851dfb906fc3c51d9a9d53a0cfa8ea88e10040baaf47155e04bf87ce3f3a5`  
		Last Modified: Fri, 09 Jun 2023 02:40:24 GMT  
		Size: 27.2 MB (27200436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8ce101c5379362c5d849146976146cdb15940589c3378f71530e726706b160`  
		Last Modified: Fri, 16 Jun 2023 01:43:18 GMT  
		Size: 1.2 MB (1199977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde7326ceba9de7061d919892605fd699e778fbaf87d16a5e3c3506e23a475fa`  
		Last Modified: Fri, 16 Jun 2023 01:43:16 GMT  
		Size: 5.5 MB (5533346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff005d43de0495d08ba8fab702b5a0b2a17e5fda87b3b29b8b6c2aa466af36e6`  
		Last Modified: Fri, 16 Jun 2023 01:45:39 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e623381dd590f881b6d778aae3d52a60123d53a9d321c5e4806f0d9b3a4ef39`  
		Last Modified: Fri, 16 Jun 2023 01:45:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28553edd6cdcf5cf14ecbcdcf441c24b01fee7ddb5cb43531838155aab41dccc`  
		Last Modified: Fri, 16 Jun 2023 01:46:01 GMT  
		Size: 104.6 MB (104611250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74fe9fb151c0863ea44c9c53bb94ecc0123ba796a5ee8bc7184f6a972941641`  
		Last Modified: Fri, 16 Jun 2023 01:45:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3267b8d9c088af1f7cdfe33f53f9f846891493df870f18d7768d87bc7013e0`  
		Last Modified: Fri, 16 Jun 2023 01:46:17 GMT  
		Size: 67.9 MB (67871748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77011554b999d13f0b9d1503fc4240e392eb8b8d8369c0c15c568fac8aabb90d`  
		Last Modified: Fri, 16 Jun 2023 01:46:09 GMT  
		Size: 264.4 KB (264358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135fac5e8dffcd24f463dc2d69b721a06ef0c98a9864e14c0c3c9a560c65e83f`  
		Last Modified: Fri, 16 Jun 2023 01:46:09 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdeffb56c570402f71cf2349f5c52edb465da5b45e52058a801414cb3b95f9a`  
		Last Modified: Fri, 16 Jun 2023 01:46:13 GMT  
		Size: 20.4 MB (20407016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

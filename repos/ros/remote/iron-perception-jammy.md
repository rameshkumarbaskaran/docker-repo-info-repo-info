## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:7cc7c6943d26a272a56fb01a303ac8e2c5293c0b2d7e69ebfa4ed5579baeafaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:3fde4d5abb69e4d10106af4a7334fc4a412b49fd2874c7ec8e37a0640d04bb04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **958.3 MB (958317463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f910b2235d88f9a769d3409daf7d779650461dc4c65d6dc690c5fcfc64d456`
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
# Fri, 16 Jun 2023 03:52:41 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Jun 2023 03:53:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:53:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Jun 2023 03:53:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Jun 2023 03:53:26 GMT
CMD ["bash"]
# Fri, 16 Jun 2023 03:53:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:53:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Jun 2023 03:53:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Jun 2023 03:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:55:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:fb9a4b6088658276f8fd1f323dccdcbb861073b76cd6349072032f5fdaa2308b`  
		Last Modified: Fri, 16 Jun 2023 04:06:19 GMT  
		Size: 124.1 MB (124124424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8e6f6e49e9b268b418486630a7ba4b97c13b80a80f9264b2a655e0f0a395d7`  
		Last Modified: Fri, 16 Jun 2023 04:06:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9439087c92f7f6e12a142bd39dc7cb8a1ca5d69f39bb6fd3ca975acb89c9d6ac`  
		Last Modified: Fri, 16 Jun 2023 04:06:39 GMT  
		Size: 85.0 MB (84994710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34237af467a507ca4d19e10a051e77c334109ef97c28f8df3d0138188d5facf0`  
		Last Modified: Fri, 16 Jun 2023 04:06:28 GMT  
		Size: 291.6 KB (291640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8439ca8819e994b1e7dcd6debd7f51f0c0ca681463f29e88c0d676fba1637630`  
		Last Modified: Fri, 16 Jun 2023 04:06:28 GMT  
		Size: 2.4 KB (2427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc933ad7e1ecb3369fd1ba6557a11d42c83c4fb1e3dedafecc4dd69606c3b4b0`  
		Last Modified: Fri, 16 Jun 2023 04:06:32 GMT  
		Size: 23.7 MB (23673251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea445e950d5ff71f0dca0f2722e50be59d87f2c3309d0e5b1293381c7cce2451`  
		Last Modified: Fri, 16 Jun 2023 04:08:17 GMT  
		Size: 689.8 MB (689755983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e23fbdf99473f486bf44b942d6aaf3128152d34273fc4c41dd7ea96bad29a7db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.6 MB (919580956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fdeab7306d1f14a0c7eccac9801825ddc08511f51299cb4b6c4f82fdc8cdaca`
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
# Tue, 04 Jul 2023 14:52:30 GMT
ENV ROS_DISTRO=iron
# Tue, 04 Jul 2023 14:53:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:53:15 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 14:53:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 14:53:15 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:53:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:53:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 14:53:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 14:53:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:55:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:733ac60340acf4f8387c6b6179b8802a4d95c8a764c3275e4b40dcf43bbc18e7`  
		Last Modified: Tue, 04 Jul 2023 15:04:37 GMT  
		Size: 121.6 MB (121594149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bc2c0b5866181e7b667506bf7186bed428e235b1f57501f01c1523f2967c6f`  
		Last Modified: Tue, 04 Jul 2023 15:04:16 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f2d048a238d45b0bb97de4679a5201642c788107f3fadc5dffab30584467e4`  
		Last Modified: Tue, 04 Jul 2023 15:04:54 GMT  
		Size: 82.7 MB (82736920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ba4ee66a2fe7e8250e08ad5ef26eb39fd9302d05030d7d5b0e029ab68d0578`  
		Last Modified: Tue, 04 Jul 2023 15:04:46 GMT  
		Size: 293.8 KB (293838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe9b0009bf0e31d2aee3d80fa185f8d16b3f596a535639dabfcd6eb502f80fe`  
		Last Modified: Tue, 04 Jul 2023 15:04:46 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3befa7d317c0c7dac526b38de97ecb51a996a3d9e49e1178cdebe3d2b225cd`  
		Last Modified: Tue, 04 Jul 2023 15:04:49 GMT  
		Size: 23.1 MB (23068245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036c38cd2ca44bd4b897a9e6a91bd6e2023be22797e17aaef8e6d6b3951c8bc1`  
		Last Modified: Tue, 04 Jul 2023 15:06:17 GMT  
		Size: 658.5 MB (658475285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

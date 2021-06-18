## `ros:galactic-ros1-bridge-focal`

```console
$ docker pull ros@sha256:b3016ad8fa5ce0f1964beedf891d88ba20c038f59a570b6eccb39fd5135e12f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:81a25ad83d26c179eb9b63b60933fc77f20c8cc68dfae1b168b542510709ffb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322553266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343d6ece9ede76a8dbc169b285948d227c28b301b0ab37f47764f57ece3ec6b0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:24:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:57:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:12:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 18 Jun 2021 02:12:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Jun 2021 02:12:51 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jun 2021 02:12:51 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Jun 2021 02:15:42 GMT
ENV ROS_DISTRO=galactic
# Fri, 18 Jun 2021 02:16:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:16:27 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 18 Jun 2021 02:16:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Jun 2021 02:16:28 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:16:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:16:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Jun 2021 02:16:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 18 Jun 2021 02:17:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:17:24 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Jun 2021 02:17:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Jun 2021 02:17:25 GMT
ENV ROS1_DISTRO=noetic
# Fri, 18 Jun 2021 02:17:25 GMT
ENV ROS2_DISTRO=galactic
# Fri, 18 Jun 2021 02:17:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:18:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:18:00 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7068ef4db9e492493ff87fbf9095d1e4880263be63a6f42639411a96d5ed57f8`  
		Last Modified: Fri, 18 Jun 2021 02:27:02 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef2bdf44548ac5fc0e44b69348d2e10929673915bf3217b590b7535feaf9d95`  
		Last Modified: Fri, 18 Jun 2021 02:27:00 GMT  
		Size: 5.5 MB (5546913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7391322adec07e74f2aba8edc862a4e4763771b8e7834acce634c5dbecb658`  
		Last Modified: Fri, 18 Jun 2021 02:30:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae6eda429a76621671058b7c9dedc8b5681069907a1940daeb55913e06cd4cf`  
		Last Modified: Fri, 18 Jun 2021 02:30:19 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ada5f16a026eab8a221d51db2c20e9ea37c3072a0b2c281604fff5aad6696b1`  
		Last Modified: Fri, 18 Jun 2021 02:32:25 GMT  
		Size: 103.6 MB (103613318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb5ea6029f88f11c4d97cb320027f91b4fbfdd58ae7180d2bf1bb5c23d00f35`  
		Last Modified: Fri, 18 Jun 2021 02:32:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9f55b4fa18ae28d3d3490dbf2e89ec6b258acaced76fab09c769e7c21738f2`  
		Last Modified: Fri, 18 Jun 2021 02:32:48 GMT  
		Size: 66.6 MB (66550544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf9274976ef70285b0e42376a86ed012534d5a01283c03c9fdda991545c3c11`  
		Last Modified: Fri, 18 Jun 2021 02:32:36 GMT  
		Size: 234.4 KB (234425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10677ba132e2f8550410ea57e748edc342b44c8445b594c14a698f113c9ffe8a`  
		Last Modified: Fri, 18 Jun 2021 02:32:35 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8d6631a8510e42592ff9485f745b27133e502c2ba2c621ec936e3ac56caab4`  
		Last Modified: Fri, 18 Jun 2021 02:32:41 GMT  
		Size: 22.1 MB (22095295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67b827799f8410ffac85eacd7ba4da0d2375ae6a99c5c45f8c2f7688f014371`  
		Last Modified: Fri, 18 Jun 2021 02:33:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fe4710e4bf4c1167669a16f859d5cdb27c0eecfe90e01110558b697210a403`  
		Last Modified: Fri, 18 Jun 2021 02:33:02 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada466ddc6b96b7af9abc72a23c6e7cc55a74162f8fa73ce97996ac018ea43a4`  
		Last Modified: Fri, 18 Jun 2021 02:33:24 GMT  
		Size: 78.4 MB (78409357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6db6cddc1ed7a70ccdeb1610359ec4b968e5536cfe49642b1f063dd9d4d6f9`  
		Last Modified: Fri, 18 Jun 2021 02:33:07 GMT  
		Size: 16.4 MB (16362214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf26bba415264851b5c953e79eccd6bdf209638624ab654fc27475f021aeef7`  
		Last Modified: Fri, 18 Jun 2021 02:33:02 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3ce6570b41159f145ede08290de39f0094e22f0ef182413751d1dbc79a175b9e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310704649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8779df7ca086e881603699755bb16d974ea331ed1bfc2ad5a90ae1de78a09016`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:16:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:16:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:21:28 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 18 Jun 2021 01:21:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Jun 2021 01:21:30 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jun 2021 01:21:30 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Jun 2021 01:23:55 GMT
ENV ROS_DISTRO=galactic
# Fri, 18 Jun 2021 01:24:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:24:36 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 18 Jun 2021 01:24:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Jun 2021 01:24:36 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:25:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:25:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Jun 2021 01:25:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 18 Jun 2021 01:25:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:25:40 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Jun 2021 01:25:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Jun 2021 01:25:41 GMT
ENV ROS1_DISTRO=noetic
# Fri, 18 Jun 2021 01:25:41 GMT
ENV ROS2_DISTRO=galactic
# Fri, 18 Jun 2021 01:26:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:26:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:26:16 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c561e77a6581855b0d4bcc7b9679a0821de33d9475c1aafa35306fd01018cc`  
		Last Modified: Fri, 18 Jun 2021 01:36:32 GMT  
		Size: 1.2 MB (1183649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b8cb9206c66daa80abb822d79f1304b0788918a2f9ba31628d947338478acc`  
		Last Modified: Fri, 18 Jun 2021 01:36:30 GMT  
		Size: 5.5 MB (5512873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5209be94969f98c26b06c264ea08cf71bb1283c69ce7ca685f96e270e387d3`  
		Last Modified: Fri, 18 Jun 2021 01:39:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eba4e54c2e10d6e40ec38a204350abcbb7acc2e9d1756e4cfdf8ed8ac35161a`  
		Last Modified: Fri, 18 Jun 2021 01:39:51 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3c281cd5faa4737a808df230ea8794460973abcfe6c9b9b340613dd43e4474`  
		Last Modified: Fri, 18 Jun 2021 01:41:56 GMT  
		Size: 100.0 MB (99999949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07bbebd3cebc33ba53aa35ed6230d6a5f209def2bfc680adf558778cbcc8405`  
		Last Modified: Fri, 18 Jun 2021 01:41:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63335e56c7209ab61e062d6938b7c35ea66a035c16c0da9eead06aec55a6e421`  
		Last Modified: Fri, 18 Jun 2021 01:42:19 GMT  
		Size: 60.9 MB (60920663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c81783b2c87d108d80f56dd45dfee5ef77561810c5d09f5b4cb8798fbe1677`  
		Last Modified: Fri, 18 Jun 2021 01:42:08 GMT  
		Size: 234.4 KB (234418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fa178075a0611f211a97568d17fbb8ae885c3ceb93a304e288934b729af49a`  
		Last Modified: Fri, 18 Jun 2021 01:42:08 GMT  
		Size: 2.0 KB (2036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aca8c035cfe4288740839b4acc527bcc1ccf3923cd663119acfb3b35bb2e4d`  
		Last Modified: Fri, 18 Jun 2021 01:42:12 GMT  
		Size: 21.4 MB (21430620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8827e22752ca2a0e9f9a2339c50fee3ea8f706a7c9c0c7090522d075b58f91`  
		Last Modified: Fri, 18 Jun 2021 01:42:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776f2b10add4db42bb4452a5002747bc6fc661c470de95c4ce386321e198a80c`  
		Last Modified: Fri, 18 Jun 2021 01:42:36 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823da43639f3474623e51135f7b66cafabc795dac90d3795475b6d7971a87df5`  
		Last Modified: Fri, 18 Jun 2021 01:42:58 GMT  
		Size: 78.4 MB (78368758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e50b48efe0b3fbc4d4be12bfd497acb25e0e398faf3b7f95785e431421c6d61`  
		Last Modified: Fri, 18 Jun 2021 01:42:40 GMT  
		Size: 15.9 MB (15889849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d1eca4f5cbdc522d300100dc2ca11fd25c67328a3bab9a11f07c2dea52774`  
		Last Modified: Fri, 18 Jun 2021 01:42:36 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

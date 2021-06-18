## `ros:rolling-ros1-bridge`

```console
$ docker pull ros@sha256:98161e62b6d4d01e905c45deae895fa0092d830bfe75eab6c1706b9e8c30748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:f3eda3ea6e4b097bb2c8f08eef1d804c64f486d76fe70a16dbc9566bdd2b9287
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321262923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299aed0c28d698fc0d30005feebaeb19c4db40a65a8bfda5077a585b904223eb`
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
# Fri, 18 Jun 2021 02:18:05 GMT
ENV ROS_DISTRO=rolling
# Fri, 18 Jun 2021 02:18:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:18:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 18 Jun 2021 02:18:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Jun 2021 02:18:49 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:19:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:19:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Jun 2021 02:19:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 18 Jun 2021 02:19:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:19:47 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Jun 2021 02:19:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Jun 2021 02:19:49 GMT
ENV ROS1_DISTRO=noetic
# Fri, 18 Jun 2021 02:19:49 GMT
ENV ROS2_DISTRO=rolling
# Fri, 18 Jun 2021 02:20:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:20:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.10.1-1*     ros-rolling-demo-nodes-cpp=0.15.0-1*     ros-rolling-demo-nodes-py=0.15.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:20:26 GMT
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
	-	`sha256:de20d81bd4173a8339fec869e6e366ade6bc0fe364230a03c10df78cf96f9076`  
		Last Modified: Fri, 18 Jun 2021 02:33:59 GMT  
		Size: 103.6 MB (103615082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427cb0aea3e4fffb341a10ccca49e0def7d1efbe7edbeacb6a0d83460d208b5a`  
		Last Modified: Fri, 18 Jun 2021 02:33:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837448df0815a613ee720a81c9f44ab668e5e4b2b2616b6f31a4495fea465839`  
		Last Modified: Fri, 18 Jun 2021 02:34:23 GMT  
		Size: 66.6 MB (66550472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2420cde9136fdf7d018e6571536582bd69834d41d6f368fb1c18b4c250c02bcf`  
		Last Modified: Fri, 18 Jun 2021 02:34:11 GMT  
		Size: 233.9 KB (233906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4da8004060a34a319a474c460b80e1554f49287d7b0f6caed1ad1fe56fc325`  
		Last Modified: Fri, 18 Jun 2021 02:34:11 GMT  
		Size: 2.0 KB (2032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe7a80f8badad65537ffae8798f29e730fa7544eec2776c97651295d0f70f5c`  
		Last Modified: Fri, 18 Jun 2021 02:34:16 GMT  
		Size: 22.1 MB (22112431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2223c216945e3173e68c2c7a500219b338b0cd99698a843ac182d2775a79898`  
		Last Modified: Fri, 18 Jun 2021 02:34:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe759e8c92b56e706d56bc8d57690f6a4c9f4be6441d8914bffc122167b2a3d`  
		Last Modified: Fri, 18 Jun 2021 02:34:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d2347f07e71fe05985b3ec49b07db5a4c527e8d8c3cd1b7ccf82226b6db9b9`  
		Last Modified: Fri, 18 Jun 2021 02:34:59 GMT  
		Size: 78.4 MB (78410443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e643896b536ffd9b3195c3de2991757e06005c986cd264a221f188ae89151`  
		Last Modified: Fri, 18 Jun 2021 02:34:42 GMT  
		Size: 15.1 MB (15052441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe5a309ec844c860dcdc4d2ee8cc0bfd97bf10184a7a762c0d998af43f4f5af`  
		Last Modified: Fri, 18 Jun 2021 02:34:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:509721406f962fda338a96d93880cdff5332e1af6194561d73e812fb46ca29c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309458223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17bf27ac7c4419c7678c486093312b7122f73f9116b037f0667f85f9910d10e`
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
# Fri, 18 Jun 2021 01:26:23 GMT
ENV ROS_DISTRO=rolling
# Fri, 18 Jun 2021 01:27:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:27:03 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 18 Jun 2021 01:27:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Jun 2021 01:27:04 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:27:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:27:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Jun 2021 01:27:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 18 Jun 2021 01:27:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:28:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Jun 2021 01:28:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Jun 2021 01:28:08 GMT
ENV ROS1_DISTRO=noetic
# Fri, 18 Jun 2021 01:28:09 GMT
ENV ROS2_DISTRO=rolling
# Fri, 18 Jun 2021 01:28:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:28:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.10.1-1*     ros-rolling-demo-nodes-cpp=0.15.0-1*     ros-rolling-demo-nodes-py=0.15.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:28:44 GMT
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
	-	`sha256:87bab0643538a88d3237e1034009da28994975922425be6c79e06599667902ec`  
		Last Modified: Fri, 18 Jun 2021 01:43:30 GMT  
		Size: 100.0 MB (99995784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3aa4adc2b9dbbabfbe5de417d9c78e594674a4073380274bdc09509b6a717a4`  
		Last Modified: Fri, 18 Jun 2021 01:43:11 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e76e8ff735e23ef93c1cf44e242fedcb3b6e64a4b2a997c805c35bcee5c873`  
		Last Modified: Fri, 18 Jun 2021 01:43:59 GMT  
		Size: 60.9 MB (60920414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1df38f1e163e319dd6129117780d6180bc8da2a601e74b550af1d5befff34e`  
		Last Modified: Fri, 18 Jun 2021 01:43:47 GMT  
		Size: 233.9 KB (233901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cb6fb4d817acd74ea55098bd6e036e4b5209499d19354e72daba5f51c9b3a8`  
		Last Modified: Fri, 18 Jun 2021 01:43:47 GMT  
		Size: 2.0 KB (2047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410e6c24794ec3018d5effc08528698df0ff5573a7a3b39e14ce6de24e2f9c1d`  
		Last Modified: Fri, 18 Jun 2021 01:43:51 GMT  
		Size: 21.4 MB (21449057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c88ab0e230b56f3d70dc8bd6086185f33c6cf8691e3636ab1aa8ed3ee20bb9e`  
		Last Modified: Fri, 18 Jun 2021 01:44:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75033272b9606e67db1d30b41ca9ff4ec77d2202ea1f45a4af8c72fb455b26d`  
		Last Modified: Fri, 18 Jun 2021 01:44:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd74012273e262686f50ee17beb69b592dbde8e21ba7950482664641b4b0a8e`  
		Last Modified: Fri, 18 Jun 2021 01:44:33 GMT  
		Size: 78.4 MB (78368152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4a9e437753adba152a9f605e3a44baf39ca2168ebbf1b7532a7601a3125ede`  
		Last Modified: Fri, 18 Jun 2021 01:44:19 GMT  
		Size: 14.6 MB (14630507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84555ec2e7115b410ff325e240f2acdc36d84ab16e73f226675800fb3f09c356`  
		Last Modified: Fri, 18 Jun 2021 01:44:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

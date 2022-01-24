## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:a3df82bdc0575212c2c93d8913ee05dbdab624054a83722827254444b7631f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:7e4e7383fed8cee2b9d167e06cde05d491831e9e30d63a0821b98171f4c50030
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.8 MB (345848796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8bd2e2e4147eacb183e28e50658cb81c5fbd606a8553f8a7f55a1424cf1c627`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:09:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:09:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:22:49 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 07 Jan 2022 04:22:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 07 Jan 2022 04:22:58 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jan 2022 04:22:58 GMT
ENV LC_ALL=C.UTF-8
# Fri, 07 Jan 2022 04:22:58 GMT
ENV ROS_DISTRO=foxy
# Fri, 07 Jan 2022 04:23:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:24:00 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 07 Jan 2022 04:24:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 07 Jan 2022 04:24:00 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:24:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:24:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 07 Jan 2022 04:24:50 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 07 Jan 2022 04:25:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:25:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 07 Jan 2022 04:25:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 07 Jan 2022 04:25:16 GMT
ENV ROS1_DISTRO=noetic
# Fri, 07 Jan 2022 04:25:16 GMT
ENV ROS2_DISTRO=foxy
# Mon, 24 Jan 2022 19:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 24 Jan 2022 19:55:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 24 Jan 2022 19:55:07 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07d6b806a5eae974734f3df21a5799c46db4c8dc12ffc6bab4a8ca2f802d1b5`  
		Last Modified: Fri, 07 Jan 2022 04:34:49 GMT  
		Size: 1.2 MB (1182238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f179e9829abe90277c32bc8a0ae588e6e8cc1695c6fc68725929e756102e57`  
		Last Modified: Fri, 07 Jan 2022 04:34:47 GMT  
		Size: 5.5 MB (5546941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9703d7991cf24346be83227ed5301b773e0d61d93effd34a9263fd4c67504f`  
		Last Modified: Fri, 07 Jan 2022 04:37:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ee04ca82bf5b24a9b55f2bdbfb80b5ea009b8419a3e8611d2d0a551404face`  
		Last Modified: Fri, 07 Jan 2022 04:37:46 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e5fcbc56cc018564403b3e0d7a2ba1c551dbbfef70614bab532a6cec5e4b17`  
		Last Modified: Fri, 07 Jan 2022 04:38:06 GMT  
		Size: 120.1 MB (120084781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca376e51cfddbb5565d4cb5bcd27b84bd29b7814c3a10f1f27d006fd2fdb5f57`  
		Last Modified: Fri, 07 Jan 2022 04:37:46 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce6db45f220ec4a768963fbf00033b6f7591d9485c3aba2b9b1a4cded3c6e14`  
		Last Modified: Fri, 07 Jan 2022 04:38:27 GMT  
		Size: 70.9 MB (70857002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f29fb66d2b2ac4fc5c4792af937f08192b56597651670a8e9c50033168736ea`  
		Last Modified: Fri, 07 Jan 2022 04:38:17 GMT  
		Size: 248.0 KB (247988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962c59003bb7bd2d1ecbcb0ce6a54795c7047db81b534f807837c0b56db2f43b`  
		Last Modified: Fri, 07 Jan 2022 04:38:17 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d2c6e532f1e832e4514e246cdd3c73654b2e2d065e9170ef5b28dac48ba046`  
		Last Modified: Fri, 07 Jan 2022 04:38:19 GMT  
		Size: 10.3 MB (10288814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a848922735be67a54da86ca5c12bfe94a37cafbf38338666e4b357e52d33459d`  
		Last Modified: Fri, 07 Jan 2022 04:38:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0188b8603e20cb241ba9ee2a4f803df3998bc141216a82eb0d648cecd27192d8`  
		Last Modified: Fri, 07 Jan 2022 04:38:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad26c3ba95887e9d9a232ed2fb9039fbf21eb3abdad27a42ab509d96bcaf54d9`  
		Last Modified: Mon, 24 Jan 2022 19:58:28 GMT  
		Size: 76.3 MB (76299062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ce84cd827cee158a64f76e9d1b2f00cb8e4db650a0d0d72a08ae1d45de8b1e`  
		Last Modified: Mon, 24 Jan 2022 19:58:20 GMT  
		Size: 32.8 MB (32770419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b00db5d24916e607219b0d993ab2db6c4ffdf0226a9da7720ce3140afa3bce`  
		Last Modified: Mon, 24 Jan 2022 19:58:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a18804a2a518af9798d39fbe5f39b64383e9e023e1764caef793eb60c798f5a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313538491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6168480373001075297888d07b8d08b37750838020b328b0ce486a6796bc12`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:15:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:15:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:21:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 07 Jan 2022 03:21:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 07 Jan 2022 03:21:31 GMT
ENV LANG=C.UTF-8
# Fri, 07 Jan 2022 03:21:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 07 Jan 2022 03:21:33 GMT
ENV ROS_DISTRO=foxy
# Fri, 07 Jan 2022 03:22:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:22:27 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 07 Jan 2022 03:22:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 07 Jan 2022 03:22:29 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:23:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:23:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 07 Jan 2022 03:23:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 07 Jan 2022 03:23:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:23:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 07 Jan 2022 03:23:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 07 Jan 2022 03:23:44 GMT
ENV ROS1_DISTRO=noetic
# Fri, 07 Jan 2022 03:23:45 GMT
ENV ROS2_DISTRO=foxy
# Mon, 24 Jan 2022 19:42:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 24 Jan 2022 19:43:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 24 Jan 2022 19:43:07 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1b5c31769a3e9a4ae40d97f3d7edbb0e388c814d495803544ea752c6e9d6ce`  
		Last Modified: Fri, 07 Jan 2022 03:35:30 GMT  
		Size: 1.2 MB (1184196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94701350f1a3f3c228c3daa7b1471a93f50e71219e0bf9152dedc5131dbdc27`  
		Last Modified: Fri, 07 Jan 2022 03:35:28 GMT  
		Size: 5.3 MB (5322571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ad9922ff69bb25ec018c299f28319acded05b5533ed0199dcde7dfdaf6f38d`  
		Last Modified: Fri, 07 Jan 2022 03:38:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f333e9ff5288dcdc1fe0dd0332bc451df49b84edb59aba98cfd562e29f254d`  
		Last Modified: Fri, 07 Jan 2022 03:38:13 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e66a92a9fd6a8886d123d670db5303b8dd67ddd77a81725baeb2a0b505ced2a`  
		Last Modified: Fri, 07 Jan 2022 03:38:30 GMT  
		Size: 104.3 MB (104278769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28861e6a517aa6142fc99de642cca95e1dd5a89fd9ed6a6b91f4fb027858c9`  
		Last Modified: Fri, 07 Jan 2022 03:38:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595e70d35be41ad697b7032634ba5ac686f40fb7d1f3a3831d3ab3bd181700f2`  
		Last Modified: Fri, 07 Jan 2022 03:38:52 GMT  
		Size: 65.0 MB (64978411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4de71e579016c7dd5135332644ab4822e7de561bf903b27f4b7abf4463d2e9a`  
		Last Modified: Fri, 07 Jan 2022 03:38:42 GMT  
		Size: 247.9 KB (247929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4c68e716a4fe65ae789bc8663115985441757e1dd471ceb660c034af46acb3`  
		Last Modified: Fri, 07 Jan 2022 03:38:42 GMT  
		Size: 2.0 KB (2040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff754c55fcced401707c7c7c28dee657d3c984b05bd0eb84f455b7a34e8838`  
		Last Modified: Fri, 07 Jan 2022 03:38:44 GMT  
		Size: 9.1 MB (9086053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be18a064e2514eca521a6cc4d9b7040766b8757c57d4eead497cd00bbb3bc5ad`  
		Last Modified: Fri, 07 Jan 2022 03:39:10 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf43f23dfa0d1beee60a93e52efc0607fc08a36a3c62779e10e1317c36893c`  
		Last Modified: Mon, 24 Jan 2022 19:47:46 GMT  
		Size: 76.1 MB (76131997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212510fdafe6dea26fc145d19d916b9e58279f23b1a0dc98a8f1bd2e0f3cbf8d`  
		Last Modified: Mon, 24 Jan 2022 19:47:35 GMT  
		Size: 25.1 MB (25132608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0e4bdfc786c2b4b9ac562a138d2a215c5de2a3f0c2ac4f9b21b008695141e8`  
		Last Modified: Mon, 24 Jan 2022 19:47:31 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

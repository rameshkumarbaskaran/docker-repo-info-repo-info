## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:23057a8b5b5f605187378c65129216db6659b8ba0d717d90b34495af6256de68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:845fc60bb1307a03bf649f02283e0cfe1304fbf4823b8541fb1a0060c543b43f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.5 MB (348478447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665532b112476db2c919c9d6ea566b426ee92be833f5eb901fff3e427584f343`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:10:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:11:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:22:52 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 07 Jun 2022 01:22:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 01:22:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 01:22:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 01:22:53 GMT
ENV ROS_DISTRO=foxy
# Tue, 07 Jun 2022 01:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:23:54 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 07 Jun 2022 01:23:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jun 2022 01:23:54 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:24:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:24:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jun 2022 01:24:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 07 Jun 2022 01:24:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:24:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 01:25:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 01:25:00 GMT
ENV ROS1_DISTRO=noetic
# Tue, 07 Jun 2022 01:25:00 GMT
ENV ROS2_DISTRO=foxy
# Tue, 07 Jun 2022 01:25:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:25:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:25:38 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1e38681d9b6d153af3be7e0550217dc0dfb994512346ebc7d9a7a602651e74`  
		Last Modified: Tue, 07 Jun 2022 01:47:20 GMT  
		Size: 1.2 MB (1181179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a44b59555aadd115e37e45f079fef0ca694c5888fcd16350e10a693138a6db4`  
		Last Modified: Tue, 07 Jun 2022 01:47:19 GMT  
		Size: 5.5 MB (5547097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f29772f338ee6a1336a8cfeab6d4550be032d0e9cea76c782ba25f708e14a6`  
		Last Modified: Tue, 07 Jun 2022 01:50:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b699c33a19954e95275906408065472c7989f2a8bc685a5c9ffc5f7a70446e7`  
		Last Modified: Tue, 07 Jun 2022 01:50:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb42810f84e69169e13f4ba7e14a1a7fa6d81dba996d2b091493577783be695e`  
		Last Modified: Tue, 07 Jun 2022 01:50:21 GMT  
		Size: 120.1 MB (120077388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f92457a493c04a77f0ac61cd065d158768a70191e86bf92fc446076123f8e7`  
		Last Modified: Tue, 07 Jun 2022 01:50:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476e616a90701bee44fbc310458b18ce75a4bdfe5680a22b27dba9a84bf0ef1c`  
		Last Modified: Tue, 07 Jun 2022 01:50:41 GMT  
		Size: 73.3 MB (73321142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa71ae8a0c62c2ef33328de080cdabeefda3946cc96f59ccad1ecba1796a9209`  
		Last Modified: Tue, 07 Jun 2022 01:50:31 GMT  
		Size: 257.1 KB (257124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9ad82940247dc7731be3759d12e58bd52af7b3b53b4731f2d88990db31c281`  
		Last Modified: Tue, 07 Jun 2022 01:50:31 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0def727ac7744929624ad45072377c38e2b427e4acda1e1c0b108c45e6cae0f`  
		Last Modified: Tue, 07 Jun 2022 01:50:35 GMT  
		Size: 21.7 MB (21663791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3d2bc7757d3d9d4bb3b8f6a36ae62da3d95745ee4f11a56e38fdf554486938`  
		Last Modified: Tue, 07 Jun 2022 01:50:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ebc1131df0b50eabcf4d4c6f3247f87ddbbffc13edbfa443427e13add36ad4`  
		Last Modified: Tue, 07 Jun 2022 01:50:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12074399c950505a578a1947414ca27201fa77d5d64a7acd791e9a54957a4f68`  
		Last Modified: Tue, 07 Jun 2022 01:51:10 GMT  
		Size: 76.3 MB (76316167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed4199ae2cdec8ea37d6ec3ae7cdeab825069a3f7d924bb5cbea0c4a5dc8f65`  
		Last Modified: Tue, 07 Jun 2022 01:51:00 GMT  
		Size: 21.5 MB (21536602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4fe45deb83c6b2ef4410607491f98ec61e82e32dde9b31b45a8868a4fc9248`  
		Last Modified: Tue, 07 Jun 2022 01:50:55 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8f2bdfbbd35f27434eacb61e1cc753f6a3dc69edecd9aee5dc13f245a51ff50c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.4 MB (317367145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c948ad83552ce31ced72bd4815e0565b48911d21c957a24f2099e6549becc79f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:25:55 GMT
ENV ROS_DISTRO=foxy
# Sat, 30 Apr 2022 00:26:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:26:47 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:26:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:26:49 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:27:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:27:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:27:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:27:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:05 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:09 GMT
ENV ROS1_DISTRO=noetic
# Sat, 30 Apr 2022 00:28:10 GMT
ENV ROS2_DISTRO=foxy
# Sat, 30 Apr 2022 00:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:54 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e954138377bd97441a0963808a8c70e6c51bf87155d6bdb671530efd4a2af527`  
		Last Modified: Sat, 30 Apr 2022 00:41:20 GMT  
		Size: 104.3 MB (104266243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91245cadd2f0a13ba1496609e0e2f0f4b18302e97d37290d08553b24b77ad13`  
		Last Modified: Sat, 30 Apr 2022 00:41:02 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60afb6ca72387ba9902306d593fa053a9f27a64edd9dac6ed60164bd6606bc70`  
		Last Modified: Sat, 30 Apr 2022 00:41:42 GMT  
		Size: 68.7 MB (68673212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d22cef684130e343bfe87220672bc69f71f542aee8adce35eb893f194b2107b`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 254.9 KB (254867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf97d0af157d8836375c4d09c7145909aa0c3043f4011e862c55162dbb4101a`  
		Last Modified: Sat, 30 Apr 2022 00:41:32 GMT  
		Size: 2.2 KB (2160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e657dd15b5ed4ccfe5d24e8cab5e2b032fe73c6e2edd134d2610969e5c8dc2a`  
		Last Modified: Sat, 30 Apr 2022 00:41:35 GMT  
		Size: 20.4 MB (20373496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa861354fd70fd36143a3e94a568ce9e81bdbc1c5e222a6143efac91778d8fa`  
		Last Modified: Sat, 30 Apr 2022 00:42:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf14151782a20560e27aca7e73441befbb3c36d7dd202484e5b17bc7c5ce4050`  
		Last Modified: Sat, 30 Apr 2022 00:42:20 GMT  
		Size: 76.2 MB (76156204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772a1b46f28edc250d9ba807da3c6f52c46ce707d4b58ff24ea6463fae42c70c`  
		Last Modified: Sat, 30 Apr 2022 00:42:08 GMT  
		Size: 14.0 MB (13964661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a723bcdccecac05d4dd6103b787a4f069f613618a753c6cbe7fdfe2bdf6143`  
		Last Modified: Sat, 30 Apr 2022 00:42:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

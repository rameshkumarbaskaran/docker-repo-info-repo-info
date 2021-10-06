## `ros:rolling-ros1-bridge`

```console
$ docker pull ros@sha256:c6c2a21c66cc476730dcf8a53e3e950a3877e54811d491f5e7ecf7d461873a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:29f2a52a85ba4ad8783f9a0d9a7cff407faa1865366cec57d7d40596001f1e0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326314794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85495488c7077b5c56e27bb8d7a95b5d13f6c5930824b6901aaaf8aea112662b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:03:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:02:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:14:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 01 Oct 2021 06:14:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 01 Oct 2021 06:14:52 GMT
ENV LANG=C.UTF-8
# Fri, 01 Oct 2021 06:14:52 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Oct 2021 06:19:35 GMT
ENV ROS_DISTRO=rolling
# Fri, 01 Oct 2021 06:20:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:20:20 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 01 Oct 2021 06:20:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Oct 2021 06:20:20 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 06:20:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:20:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 01 Oct 2021 06:20:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 01 Oct 2021 06:21:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Oct 2021 20:44:24 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 05 Oct 2021 20:44:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 05 Oct 2021 20:44:37 GMT
ENV ROS1_DISTRO=noetic
# Tue, 05 Oct 2021 20:44:37 GMT
ENV ROS2_DISTRO=rolling
# Wed, 06 Oct 2021 18:46:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.13-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 18:46:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.10.1-1*     ros-rolling-demo-nodes-cpp=0.16.0-1*     ros-rolling-demo-nodes-py=0.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 18:46:43 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da6d2c6667ea5660473b4dbbded093f5fb0330bb09072dd5f023fe8917898f5`  
		Last Modified: Fri, 01 Oct 2021 05:15:23 GMT  
		Size: 1.2 MB (1183161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d76f6f81fcfbb67046fda7409d7f51373035330bf4b0b3f29d51ce1531379df`  
		Last Modified: Fri, 01 Oct 2021 06:24:29 GMT  
		Size: 5.5 MB (5547583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffe3314eae3636a83a175622f5ee93d41381af25d5201e7fb77518f504348b6`  
		Last Modified: Fri, 01 Oct 2021 06:27:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ed232d940ce0dca7a045676daa5b6f75ca20f1f218fa69fc26eb95d6e625d2`  
		Last Modified: Fri, 01 Oct 2021 06:27:14 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b554d81fe16e0e94a43e8b06d838c8f786d52a9a0b89ecc0e8efb40c1a29aefb`  
		Last Modified: Fri, 01 Oct 2021 06:29:18 GMT  
		Size: 104.2 MB (104197012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d563e32523bf169883756bc09604daa8bf3bbbab8d20a0b1349afe202a434ea`  
		Last Modified: Fri, 01 Oct 2021 06:29:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32897aa3db60b88f4b19dc1072577c8e618ea9ec9ac9572e3f456f8a6df83871`  
		Last Modified: Fri, 01 Oct 2021 06:29:38 GMT  
		Size: 70.8 MB (70796896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18badf94b2b42a43cb4073ca4ed7a0d4a3bff87d40210af1205c9d866ca7beea`  
		Last Modified: Fri, 01 Oct 2021 06:29:28 GMT  
		Size: 246.1 KB (246073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a08879a1756fb090aa917136637f44131517da1fa1fc60ff224cc782071b84`  
		Last Modified: Fri, 01 Oct 2021 06:29:28 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0552cadc20be7acdc95b229c976252440b8e57b9a228c86c5396d06528134d95`  
		Last Modified: Fri, 01 Oct 2021 06:29:32 GMT  
		Size: 22.2 MB (22185027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570fcdb58ae0055a846b607d5c9837424d7619892b326b184bf363aea73a4006`  
		Last Modified: Wed, 06 Oct 2021 18:48:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aa3d0da719649cc3a0b903a1239844169f8c04480209e9ffbf2ae72ffaf6c7`  
		Last Modified: Wed, 06 Oct 2021 18:48:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347af2f0b7ca1643db787a3f4597206b3e19452578c3c51507e3313c33dce1c8`  
		Last Modified: Wed, 06 Oct 2021 18:48:59 GMT  
		Size: 78.4 MB (78425928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415ef1fbd75cb2153cadb7ee491288880806bb91bc18b8d623402804ae67960`  
		Last Modified: Wed, 06 Oct 2021 18:48:46 GMT  
		Size: 15.2 MB (15159140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7483d3c4e0ee512c17197d6a9c17bf1a30de7e48e060a2f6b8221df2493d2d`  
		Last Modified: Wed, 06 Oct 2021 18:48:43 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:05b6abb3ce69d39dfadc94c3ab1c647e1d4ffedc68a311f9866f8f7f28a28ae0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 MB (314457746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a872d7ef30122d7ffc8174cce60afa5ece6b8a7e6b090a9a66916bf3e31a91ba`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 04:05:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:05:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:10:13 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 01 Oct 2021 04:10:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 01 Oct 2021 04:10:17 GMT
ENV LANG=C.UTF-8
# Fri, 01 Oct 2021 04:10:18 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Oct 2021 04:14:48 GMT
ENV ROS_DISTRO=rolling
# Fri, 01 Oct 2021 04:15:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:15:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 01 Oct 2021 04:15:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Oct 2021 04:15:43 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 04:16:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:16:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 01 Oct 2021 04:16:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 01 Oct 2021 04:16:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 18:31:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Oct 2021 18:31:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 06 Oct 2021 18:31:36 GMT
ENV ROS1_DISTRO=noetic
# Wed, 06 Oct 2021 18:31:37 GMT
ENV ROS2_DISTRO=rolling
# Wed, 06 Oct 2021 18:32:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.13-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 18:32:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.10.1-1*     ros-rolling-demo-nodes-cpp=0.16.0-1*     ros-rolling-demo-nodes-py=0.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 18:32:14 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca36dcb5509e6b267d7d917bd37bab3a2fe9b3bb7fc75f0ac08d43124d65dcaa`  
		Last Modified: Fri, 01 Oct 2021 04:21:14 GMT  
		Size: 1.2 MB (1183644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a8b61bc4869c8fd71f74e111385e4330a1f33dc9a4e9479a0721d070693113`  
		Last Modified: Fri, 01 Oct 2021 04:21:12 GMT  
		Size: 5.5 MB (5512866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485f6bb99f825bcf3317a0b34e2dc1a4a5e29d1a809722d3d925e0854b098518`  
		Last Modified: Fri, 01 Oct 2021 04:24:08 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd308002f060ef67048c13d059b7b55b15e9842c70fb6f42908d2b93609acbb4`  
		Last Modified: Fri, 01 Oct 2021 04:24:08 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08513d2f3e9188ae8ea6d5851048f335e9c160d03ee48ae75c7fb8c9afad07fa`  
		Last Modified: Fri, 01 Oct 2021 04:26:25 GMT  
		Size: 100.6 MB (100568224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c5264a8b044c054fe5d9dc04a5a0cf3c914e4cd3535ad6c8596a0b96a15d8b`  
		Last Modified: Fri, 01 Oct 2021 04:26:07 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0eff781a6f77828c4915114584bf3e9edd8f1308a168ac79afb665152fdf4a`  
		Last Modified: Fri, 01 Oct 2021 04:26:50 GMT  
		Size: 65.1 MB (65138693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a016822bb5cd49ab4e71c1082464dd37689aa7471fb306ede1cfca5eff18220`  
		Last Modified: Fri, 01 Oct 2021 04:26:39 GMT  
		Size: 246.1 KB (246075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6383fd0264d5da6acd9e3196f0af5956a67341cb79394c65199650516764b90`  
		Last Modified: Fri, 01 Oct 2021 04:26:39 GMT  
		Size: 2.0 KB (2046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de74966aa3dcc6e30ddb16cb05a7df14f98ddc6802642e40a280e6a3bfad557c`  
		Last Modified: Fri, 01 Oct 2021 04:26:43 GMT  
		Size: 21.5 MB (21527018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa0f071e518963a4248fc80f114259b707533c3f916e75d5a01e7ee79a60648`  
		Last Modified: Wed, 06 Oct 2021 18:35:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3bd2078b527ae661273461c5caf4daa476bba837c40b55c50ee44cb5c1e8c0`  
		Last Modified: Wed, 06 Oct 2021 18:35:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdf35e79bbb9e83e42ad524f321385391ab90bbf873c2ee7b115fd648e226c5`  
		Last Modified: Wed, 06 Oct 2021 18:35:42 GMT  
		Size: 78.4 MB (78375673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aa162a3b8b0c70d64c16745d6b7ef9fa248bbbc7488608cae9ef1f5b0d71c6`  
		Last Modified: Wed, 06 Oct 2021 18:35:29 GMT  
		Size: 14.7 MB (14728059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aac408fee0e1ade5bc155a3bdfb772003d31cc06b8f0edcf1c881567030179`  
		Last Modified: Wed, 06 Oct 2021 18:35:26 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

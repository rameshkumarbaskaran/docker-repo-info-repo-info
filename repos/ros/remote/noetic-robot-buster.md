## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:e9dffd374565b64b3a6eef22a5234ccbe6f94ed2b683d93a7b34d78ebe186f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:76da6fdfc920d580dd77b5311d28a2246a080b1e04d96e3822f6970c8985fc81
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.3 MB (484315218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383699f39acd50aa28fe8deb438cdb474de6d9fadbc5bd688ea320931d2752e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:41 GMT
ADD file:89234bb2f86c7eb890235a48904d1c9898a8d287a525c4fe5698d4a04cdd8f12 in / 
# Fri, 26 Mar 2021 15:20:42 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:18:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:19:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 27 Mar 2021 09:19:01 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 27 Mar 2021 09:19:01 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 09:19:01 GMT
ENV LC_ALL=C.UTF-8
# Sat, 27 Mar 2021 09:19:02 GMT
ENV ROS_DISTRO=noetic
# Sat, 27 Mar 2021 09:20:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:20:07 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 27 Mar 2021 09:20:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 27 Mar 2021 09:20:07 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:20:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:20:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 27 Mar 2021 09:21:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:21:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8bf9c589d5f9475f1fcc050e02308d6b4eeb86eab7752ef948a13693e81a6aaa`  
		Last Modified: Fri, 26 Mar 2021 15:27:11 GMT  
		Size: 50.4 MB (50400278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f449035c3af90c31ff21aac54677ddaa94af7b4199927b2f133e67e8595890b`  
		Last Modified: Sat, 27 Mar 2021 09:29:31 GMT  
		Size: 10.9 MB (10891856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456137ab974bca1d8f62d7d5680410744326ca834b1a0b28f08439320b0760e6`  
		Last Modified: Sat, 27 Mar 2021 09:29:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1385d40e15645e2c90531a6509af986cdf1443339297d7fe19d8279b932c5ca`  
		Last Modified: Sat, 27 Mar 2021 09:29:28 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb71cc1ea410520d668b783bdd3e0a1a5c7b5f781d4adc019127c0b6c76a3f1c`  
		Last Modified: Sat, 27 Mar 2021 09:30:24 GMT  
		Size: 239.0 MB (238991317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886c7fa5d1013621ff1cbf8d90848d0ccd58d5769abfb273e8a5760ea7cbdd10`  
		Last Modified: Sat, 27 Mar 2021 09:29:28 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09ce8b79379dd299aa16f768d61fbecdd248503ba14153c488473212c646325`  
		Last Modified: Sat, 27 Mar 2021 09:30:49 GMT  
		Size: 86.6 MB (86566359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac64f5538503a14d3bfde99b870e7313c132f18a63f039d615ebac954589ed`  
		Last Modified: Sat, 27 Mar 2021 09:30:33 GMT  
		Size: 274.0 KB (274003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feaf0f42bd10ccb191c0271e1ed66a9a8a47b8abcf30bcb9e13c6a33eea92abf`  
		Last Modified: Sat, 27 Mar 2021 09:30:45 GMT  
		Size: 76.0 MB (75974718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb3119fce55de8d3872f6b8d8f0b6bf90d84e8ed59749c0f42677b82554859a`  
		Last Modified: Sat, 27 Mar 2021 09:31:00 GMT  
		Size: 21.2 MB (21214850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:43f83a6f922ba018330d92e1d633e89599c615642f1dbaffd2913377a216a2cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.9 MB (423863201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb5acfa6b14ab3462232a2796b1effb65588043ae159f35da4210c27d1fea0e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:41:27 GMT
ADD file:536306ac674764a6a921b71adcbb4440797b916a0583b9270cd1565d62642e4d in / 
# Fri, 26 Mar 2021 15:41:30 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 08:44:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:44:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 27 Mar 2021 08:44:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 27 Mar 2021 08:44:56 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 08:44:57 GMT
ENV LC_ALL=C.UTF-8
# Sat, 27 Mar 2021 08:44:58 GMT
ENV ROS_DISTRO=noetic
# Sat, 27 Mar 2021 08:46:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:47:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 27 Mar 2021 08:47:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 27 Mar 2021 08:47:04 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 08:47:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:47:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 27 Mar 2021 08:48:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:383261dafcc4f63ecae5f2d661d1ef8d0a5e1c9f4b1f12285115baca7d101d5a`  
		Last Modified: Fri, 26 Mar 2021 15:48:21 GMT  
		Size: 49.2 MB (49196215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5ff3f5d28c8af3f88665a2aa84284c359ed12aa33168c1a64a78f0ade71297`  
		Last Modified: Sat, 27 Mar 2021 09:00:29 GMT  
		Size: 10.9 MB (10883463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74fad49a464d1b87097bc055363ccb50dc8a92828ad693eb5e1ee949e41b56e`  
		Last Modified: Sat, 27 Mar 2021 09:00:27 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f561924c9d78e4a9873808f60fb46676818c58ab68fb4ecd8fcc00d3953f0e7`  
		Last Modified: Sat, 27 Mar 2021 09:00:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b4a7908a17a34219acf017102f05b6e2720d17bc539a55d3916795c4c949f1`  
		Last Modified: Sat, 27 Mar 2021 09:01:34 GMT  
		Size: 184.2 MB (184194463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c4e20a52ff1b28780dfe7a728e042eb5ba0421aaa6b2e917eb1a9588932ac4`  
		Last Modified: Sat, 27 Mar 2021 09:00:27 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8741f36ba2b22dc88c2e8ea1a96fb35db8c241e26be5ba22490eb924ad0e2b3d`  
		Last Modified: Sat, 27 Mar 2021 09:02:03 GMT  
		Size: 84.4 MB (84356647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b843b98642a4e0c1c6d6d815da87944cb62ae5cb3e404337cdbe149ded992b`  
		Last Modified: Sat, 27 Mar 2021 09:01:41 GMT  
		Size: 274.0 KB (274013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49335c38dce3605251b7f99abc427e604ae046368520952ec2af753ac3279308`  
		Last Modified: Sat, 27 Mar 2021 09:02:00 GMT  
		Size: 74.1 MB (74088666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1da49a2fb162436058a4dbd35ec881f0e18bd38df1a23a97494d0a57d22f88`  
		Last Modified: Sat, 27 Mar 2021 09:02:18 GMT  
		Size: 20.9 MB (20867899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

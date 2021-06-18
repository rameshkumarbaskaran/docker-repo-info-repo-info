## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:84f5968e3e142bf7b0d619ba67dc8e228898743ef3fd329d74be041226922594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:c9560582e17e8eed4a72bb18433d1e6f56b70d62513d307993c776bb886d1a78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 MB (334891393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950431941162e51c6aa584d795928655524e74288527c44ba2202809e19b0301`
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
# Fri, 18 Jun 2021 01:57:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Jun 2021 01:57:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Jun 2021 01:57:51 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jun 2021 01:57:51 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Jun 2021 01:57:51 GMT
ENV ROS_DISTRO=noetic
# Fri, 18 Jun 2021 02:00:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:00:58 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 18 Jun 2021 02:00:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Jun 2021 02:00:58 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:01:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:01:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Jun 2021 02:03:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7b805325df4d3716458978c48a5566aa6f2dbeb0be999f44c7f2eb4f6df55e11`  
		Last Modified: Fri, 18 Jun 2021 02:26:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64023780da8e71f6b88553fcffa3bc15bf627c1b1fc0aaf8ddc9af812128ec9`  
		Last Modified: Fri, 18 Jun 2021 02:26:59 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d6d4726d161eb1b509db57b293c81ce05ceff9931bed70bd4faaa996412b4e`  
		Last Modified: Fri, 18 Jun 2021 02:27:39 GMT  
		Size: 173.3 MB (173312527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077ea8650d58e6131af39d81de66161336ce9c8fc6fd3b3ef3430f6b0c2bda02`  
		Last Modified: Fri, 18 Jun 2021 02:26:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e80c4f5578a19f588ad6027bb260daf83091fb9f24409dd71d4d31ec276489`  
		Last Modified: Fri, 18 Jun 2021 02:27:59 GMT  
		Size: 46.4 MB (46383706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b114571870237830af2427dc7692d57b06140899ae969d0c462a35df493e39dd`  
		Last Modified: Fri, 18 Jun 2021 02:27:50 GMT  
		Size: 307.2 KB (307182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e00a8de6086cf9af436698858140f30da4b4024f10b9f5270bf4b25bf77950f`  
		Last Modified: Fri, 18 Jun 2021 02:28:05 GMT  
		Size: 79.6 MB (79602485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:cbe95a64cfdaf927723119c35a44bc6e74458fb469f0dda63bb72dd3b886657b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283715127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c62e431459f3305175a89b0443a3b7f0fc76c8c11f930ccb8f4d20e453d2a4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:07 GMT
ADD file:80eca60b823985c38c6de6b89041c5b4c6c668371ec1651af2252d3e29802b48 in / 
# Thu, 17 Jun 2021 23:32:08 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:39:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:39:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:39:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Jun 2021 00:39:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Jun 2021 00:39:26 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jun 2021 00:39:26 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Jun 2021 00:39:26 GMT
ENV ROS_DISTRO=noetic
# Fri, 18 Jun 2021 00:40:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:40:22 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 18 Jun 2021 00:40:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Jun 2021 00:40:23 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:40:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:40:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Jun 2021 00:41:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:10ded72e3c7fd53116a7f233f140c1e56753fdee4f5cbd888b9e62f3b6684a5f`  
		Last Modified: Thu, 17 Jun 2021 23:34:59 GMT  
		Size: 24.1 MB (24051742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8cede0e2e2dd5d208ef924463c999e69cb6fc1ba2307638552691d952b69fc`  
		Last Modified: Fri, 18 Jun 2021 00:51:37 GMT  
		Size: 1.2 MB (1183539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270aed8a77df54e18c79b0a229b46987065bb0ea02f33648a733798958dd0f6b`  
		Last Modified: Fri, 18 Jun 2021 00:51:35 GMT  
		Size: 4.7 MB (4676498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1e9a5b1478dbbb8fb8e8bfd33a08ff80bab33be91503bb30a54b726281c8a9`  
		Last Modified: Fri, 18 Jun 2021 00:51:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b3303d4a12b07ea1903b5cc79b486342c231dd7dd39a9453e932141e7f1f1`  
		Last Modified: Fri, 18 Jun 2021 00:51:34 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165aff3d1855dc9605e8ff882bf0ef6f3a2070675e76f4ffc0e3b2232bde2182`  
		Last Modified: Fri, 18 Jun 2021 00:52:16 GMT  
		Size: 157.2 MB (157180161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11687330ead2d1d115616c6d694c08854445c59caa4b0772837df8c2e0a87f2`  
		Last Modified: Fri, 18 Jun 2021 00:51:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbbe51271308fe6a1af1a169182b0f15582f368c872736775e764109f238983`  
		Last Modified: Fri, 18 Jun 2021 00:52:37 GMT  
		Size: 35.8 MB (35832534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0835fe755c71537f5323873f30c148f7f77b4e38fb3feda80d127848da6110d0`  
		Last Modified: Fri, 18 Jun 2021 00:52:30 GMT  
		Size: 307.2 KB (307174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2c08ad57952ad399129ef6732755ffe72648326f6eb85c67957c08133b5a09`  
		Last Modified: Fri, 18 Jun 2021 00:52:44 GMT  
		Size: 60.5 MB (60481071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2cacf86423c2c0975315fed27525f218224e20bd0872870472187b72b9577a2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 MB (314579790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e70451757ae814799c9bb72e863aa12b8011a49c6049366f2c86e7c86038c`
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
# Fri, 18 Jun 2021 01:16:58 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Jun 2021 01:16:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Jun 2021 01:17:00 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jun 2021 01:17:00 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Jun 2021 01:17:00 GMT
ENV ROS_DISTRO=noetic
# Fri, 18 Jun 2021 01:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:17:48 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 18 Jun 2021 01:17:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Jun 2021 01:17:48 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:18:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:18:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Jun 2021 01:18:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:221feb81eb1f2a726e60f133308042f938d56c17d93bb58e579331ac82db4361`  
		Last Modified: Fri, 18 Jun 2021 01:36:29 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e854a63e407af8a98ce9423f465f741b1391622ab778b194ffdd73b401d1f09`  
		Last Modified: Fri, 18 Jun 2021 01:36:29 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31e769dc6dc1b2825400e8c4f1f822c2f6793a851ccb1f5befc9d365546b54f`  
		Last Modified: Fri, 18 Jun 2021 01:37:09 GMT  
		Size: 167.8 MB (167791425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267b59e42fab796f88f9034141f4ef8b681764faa78cdcdd15e6fcc841e712c7`  
		Last Modified: Fri, 18 Jun 2021 01:36:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d19dcde6b5d00235d5458675c834b27246ded78afbcafd52415832b238c527`  
		Last Modified: Fri, 18 Jun 2021 01:37:28 GMT  
		Size: 40.7 MB (40650604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f55e8737df32cfb68aef8faf31c80e8a806987bdcb9b01ea2c40c56f0261092`  
		Last Modified: Fri, 18 Jun 2021 01:37:21 GMT  
		Size: 307.2 KB (307169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80366f56b9dfbc22e74d7236626b43457126c0b3a4021691dbf536679e15f025`  
		Last Modified: Fri, 18 Jun 2021 01:37:34 GMT  
		Size: 72.0 MB (71972855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

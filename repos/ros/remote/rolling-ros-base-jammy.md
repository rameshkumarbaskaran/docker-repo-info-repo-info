## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:6d6e5cb59212ff91016910217a2b437dd5ea4b4cf8fe7cecabf8e006782cf4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:da1a2d2e9e41bd9c29cb3c99a8cb4b45f8d8c87fbab20c8f3399819bebb74de8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262719439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436e82c5b0bca3bd441eaded5e62eefc4c3b7bfa6903d1a814e70b9192e560ee`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:25 GMT
ADD file:11157b07dde10107f3f6f2b892c869ea83868475d5825167b5f466a7e410eb05 in / 
# Mon, 06 Jun 2022 22:21:26 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:28:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:28:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:28:35 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 07 Jun 2022 01:28:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 01:28:36 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 01:28:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 01:40:28 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Jun 2022 01:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:41:09 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 07 Jun 2022 01:41:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jun 2022 01:41:09 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:41:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:41:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jun 2022 01:41:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 07 Jun 2022 01:42:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:405f018f9d1d0f351c196b841a7c7f226fb8ea448acd6339a9ed8741600275a2`  
		Last Modified: Wed, 01 Jun 2022 03:03:39 GMT  
		Size: 30.4 MB (30423715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d1d4bf62a3722d7122bc1b8ee8ad3051fcaf598ca72ad725fea76cb53f6b3c`  
		Last Modified: Tue, 07 Jun 2022 01:52:41 GMT  
		Size: 1.2 MB (1191642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5c906965a7cb2488a6e23da68abe175ee9acffbe27e61b1152cfff4fbf840b`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 3.8 MB (3827182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c1af53ce2d5965bf4c8489cf5459894d2e6c3f6b00538c076d38e41668d6cf`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8d3945eb76a1a2076630ee2752a89342d614a9298134e198075975ec08400d`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9c71936f086360e13475372b678edf9e90dda0249fc0cb007070b136f0b431`  
		Last Modified: Tue, 07 Jun 2022 01:55:42 GMT  
		Size: 106.1 MB (106131399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba72d83ed0d2e6bbd2f45b43761d9699bdc1bdeecc565de30d7c4c75696f0b5`  
		Last Modified: Tue, 07 Jun 2022 01:55:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e141275ac844961d5e6aae4adaff24bbc71e569676a50e4ceb83aac78b808c03`  
		Last Modified: Tue, 07 Jun 2022 01:56:14 GMT  
		Size: 97.8 MB (97838742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecab1f16ec251a3dfbd7c86db15d68f7937ac612f6b6342c89b6f7272eeb318`  
		Last Modified: Tue, 07 Jun 2022 01:56:00 GMT  
		Size: 273.2 KB (273161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e01aa968f971f9b30c74f1b45be67addb7b3ac071b1d2879a5f99184f6bd40c`  
		Last Modified: Tue, 07 Jun 2022 01:56:00 GMT  
		Size: 2.3 KB (2272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cf2ef0c2f0d6cdbddea8135625ff2a75b8f0358d46a81e65d0e8622c5bf671`  
		Last Modified: Tue, 07 Jun 2022 01:56:04 GMT  
		Size: 23.0 MB (23028911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b8f9f5f7d780bb6fa5a46e03b049d3eaf125128d96f0cefbc19085dfeced544e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257494582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5341bd45c056deaab818656b22a4f6be407b12332cff43de93b6fbe7e5b730df`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:52 GMT
ADD file:1e18e22e32f06a7e93275cf3a2eb2a1d3892be27628bdae2de4b2aadb992bd50 in / 
# Fri, 29 Apr 2022 22:49:53 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:32:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:32:29 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:32:30 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:32:31 GMT
ENV ROS_DISTRO=rolling
# Fri, 27 May 2022 00:01:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 27 May 2022 00:01:50 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 27 May 2022 00:01:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 27 May 2022 00:01:52 GMT
CMD ["bash"]
# Fri, 27 May 2022 00:02:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 27 May 2022 00:02:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 27 May 2022 00:02:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 27 May 2022 00:03:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b84950154c181a602d2e93b68e84660f96dc78f94ae36f3df2db8d5701abb6a5`  
		Last Modified: Fri, 29 Apr 2022 22:52:07 GMT  
		Size: 28.4 MB (28376457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4339dcf07e4fd919aa10dc0e01fb8f44184f74bf6baf5aef6e8fdd30f5e603`  
		Last Modified: Sat, 30 Apr 2022 00:43:58 GMT  
		Size: 1.2 MB (1192681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0db3fdf5b04e561797500fc1d19d79a37ca0586b71bee71ce2acaee153d4dee`  
		Last Modified: Sat, 30 Apr 2022 00:43:56 GMT  
		Size: 3.6 MB (3594435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af71d8cd404a31e077722270696cf33d59cff54d35c9dad864264138bc3ac`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e01b1250d40bc108a995e5fc6c1630b0abdbfff31529a87a4096271f2a6115`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb42783cc3927279718097f695acb188af7247f4635771cc2e94fd788d4b0118`  
		Last Modified: Fri, 27 May 2022 00:10:41 GMT  
		Size: 106.4 MB (106386146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c9f41ded8565c1f327636498d36859881d62a32bdc9dff5b92e047d59012dd`  
		Last Modified: Fri, 27 May 2022 00:10:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91de34af377d115902131c5b5ca87d21c9fffb69370e16847717d2e1a2a40bd4`  
		Last Modified: Fri, 27 May 2022 00:11:07 GMT  
		Size: 95.2 MB (95224066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731ff29b8d2944a451a664aa964b37ab3dae63c3ea232467461df0af1282e4e8`  
		Last Modified: Fri, 27 May 2022 00:10:53 GMT  
		Size: 271.5 KB (271498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ba5086e791ab84c3886a744c998db4d34535d380f06dea5be896569e00b76`  
		Last Modified: Fri, 27 May 2022 00:10:53 GMT  
		Size: 2.2 KB (2175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736e7996fb31e59ebb99c1d6d574b039f8d52c9d6e1e6a665c4f3e7ca7ff604d`  
		Last Modified: Fri, 27 May 2022 00:10:57 GMT  
		Size: 22.4 MB (22444755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

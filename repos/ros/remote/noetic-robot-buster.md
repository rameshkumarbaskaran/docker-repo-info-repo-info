## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:7b227f5a6d82bc59a52ec46bdb5e78c8832b22a708ce53ccb159f02b884822f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:d36de1929bdfff42944402798520e0a2c49b2cc8493369580ef38eed39b2852d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.6 MB (484649266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948ba1e76ff153297d91cd713eb4d71bb00d3d1e65a2b3eef8adf980c3ca4afa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:33 GMT
ADD file:dc52371b5f4608e5887e8c657ff951d1895e0047960f44b153c4a55ebf1726d5 in / 
# Thu, 09 Feb 2023 03:20:33 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 11:02:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 11:02:10 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 09 Feb 2023 11:02:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 09 Feb 2023 11:02:12 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 11:02:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 09 Feb 2023 11:02:12 GMT
ENV ROS_DISTRO=noetic
# Thu, 09 Feb 2023 11:03:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 11:03:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 09 Feb 2023 11:03:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 09 Feb 2023 11:03:36 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 11:04:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 11:04:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 09 Feb 2023 11:04:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 11:05:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2404786f3febb4866f85b0c8f52b0b0b94dfdb6543e94cd65f961c68f325ff7`  
		Last Modified: Thu, 09 Feb 2023 03:25:32 GMT  
		Size: 50.4 MB (50449613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb999b8f3a9c7e636ecfd923eab21dab4ad56a6e3e310ae695a43fd62c15d1e6`  
		Last Modified: Thu, 09 Feb 2023 11:09:45 GMT  
		Size: 10.9 MB (10897059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd0c17feddc0d5789db91293690ac182ed96538d0ded0ccd2d0f5f469cdee78`  
		Last Modified: Thu, 09 Feb 2023 11:09:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffc213c160645ebd9d58dae23404a6674a1d8406053e9df8404ea590e0076a1`  
		Last Modified: Thu, 09 Feb 2023 11:09:44 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c4103f7699bacf08762eca77b1ff9ec4d55eb718fe790240abc06fb3b16474`  
		Last Modified: Thu, 09 Feb 2023 11:10:16 GMT  
		Size: 239.2 MB (239207331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0d003a8d1db0ecd1033580e9d3bbba3e32d9bb734b95c13e106d204b27065d`  
		Last Modified: Thu, 09 Feb 2023 11:09:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe84347070d668c166c22040d1df57e0c8cfe10caaecfa6436190b125f3dc9e`  
		Last Modified: Thu, 09 Feb 2023 11:10:36 GMT  
		Size: 86.6 MB (86620960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba92d1342fa78d83010e7582624db32acb6f9da4d30957b5438ca807c0bea4b3`  
		Last Modified: Thu, 09 Feb 2023 11:10:23 GMT  
		Size: 337.8 KB (337796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e70ef99469b77ef2ddec00093f5a670e81ea03172888773da63fdd67356935e`  
		Last Modified: Thu, 09 Feb 2023 11:10:33 GMT  
		Size: 76.0 MB (75978186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4624ace5d296326b3d478163394b55ce8716849c3941004f36e892e0432c151`  
		Last Modified: Thu, 09 Feb 2023 11:10:45 GMT  
		Size: 21.2 MB (21155905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e4a9b45588ec67e03fc510c7e582667774087d589aae7e943b6550dce18e1d3c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.2 MB (424192360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3697a8b1ac20d6b8e172c854a21dab5252f3ee038559f4776c91b67adaa5a6d0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:48 GMT
ADD file:fba5b8ea423b27a3182ca7344a0d2365acc105b05b21a0da48675799058af042 in / 
# Thu, 09 Feb 2023 03:58:49 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:15:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:15:05 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 09 Feb 2023 13:15:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 09 Feb 2023 13:15:07 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 13:15:07 GMT
ENV LC_ALL=C.UTF-8
# Thu, 09 Feb 2023 13:15:07 GMT
ENV ROS_DISTRO=noetic
# Thu, 09 Feb 2023 13:16:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:16:30 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 09 Feb 2023 13:16:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 09 Feb 2023 13:16:30 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:16:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:16:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 09 Feb 2023 13:17:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:18:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4b9dcf1a413259e77edbbd27343105dd36806b4cafcd111a22643d0f4b9a619f`  
		Last Modified: Thu, 09 Feb 2023 04:02:52 GMT  
		Size: 49.2 MB (49239119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbeffac6e755c55ebc32761775893250af5de5937fe86bbce73fa5ca13dad817`  
		Last Modified: Thu, 09 Feb 2023 13:23:06 GMT  
		Size: 10.9 MB (10902693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25876d1034c5386b7b7207834902f95a6c0e85760ab81e65bb2667acacb2d34`  
		Last Modified: Thu, 09 Feb 2023 13:23:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4b05b7c27b880f3dced1b89a54d02e422a2c9d4083d79d2430bfe30731043`  
		Last Modified: Thu, 09 Feb 2023 13:23:04 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6ab2e9a4a8a790f5a7a01754319951b849cbdee8a97736345e80cfdb8fe683`  
		Last Modified: Thu, 09 Feb 2023 13:23:28 GMT  
		Size: 184.4 MB (184402571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d6f3465ae8ec213dd7aec86b848f7c0a84cc723e288aa24117dfb4fa698e5`  
		Last Modified: Thu, 09 Feb 2023 13:23:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ddf6981b42834d060391c88f2dfa0f3e613cb40cc131fe7ce099b87a07dfd6`  
		Last Modified: Thu, 09 Feb 2023 13:23:42 GMT  
		Size: 84.4 MB (84397667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d294ed5f09a4de249a276d8aa2bd31be6237792af02738510d019072cbbdb8c5`  
		Last Modified: Thu, 09 Feb 2023 13:23:34 GMT  
		Size: 337.8 KB (337798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3eb4c610b7f9f3a2f8e7e139996fffd53f56e7acfe17c9530993a61232b0a56`  
		Last Modified: Thu, 09 Feb 2023 13:23:42 GMT  
		Size: 74.1 MB (74090543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1aee1b38ad8dc2f450618338a8dba95b647ddc601a506e15ef5e7b5988863f`  
		Last Modified: Thu, 09 Feb 2023 13:23:51 GMT  
		Size: 20.8 MB (20819558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

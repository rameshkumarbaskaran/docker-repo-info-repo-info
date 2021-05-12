## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:6f0906924814fb2381a3bdaf52ae3e0d7aba81c5338728f534b40e3cf15b5aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:7eaa6cf87b112465dd5983bf8e5a48258d62434618b1ce322b6a05e21ca9c59d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **967.9 MB (967943677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7463cf0deefcab64b17c8143b74138259be717035bf32eeed5250146657067d0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 17:14:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:14:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 12 May 2021 17:14:48 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 12 May 2021 17:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 17:14:49 GMT
ENV LC_ALL=C.UTF-8
# Wed, 12 May 2021 17:14:49 GMT
ENV ROS_DISTRO=noetic
# Wed, 12 May 2021 17:15:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:16:00 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 12 May 2021 17:16:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 12 May 2021 17:16:00 GMT
CMD ["bash"]
# Wed, 12 May 2021 17:16:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:16:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 12 May 2021 17:16:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:19:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a04ce26341db0d6591d2793ca267552485c51f4cbb273019ac821d671266ce`  
		Last Modified: Wed, 12 May 2021 17:24:25 GMT  
		Size: 10.9 MB (10891745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad660b1585da7e0367ce63f17fafc6908ff07cb37a86a990231df068909dced`  
		Last Modified: Wed, 12 May 2021 17:24:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6dde1ade4b0aa9d209f722a79ece3f88a0e7fecdbcd0c233656fc47e4ef53`  
		Last Modified: Wed, 12 May 2021 17:24:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf712e517ccc21a01aacc8ab5654a6fac578b379c312ebc3ab51765cf9331da`  
		Last Modified: Wed, 12 May 2021 17:25:00 GMT  
		Size: 239.0 MB (239023064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65e290ea31d62ef896514aeb7f8713ec481fae9a7bc2545d8d6fd5866a166d4`  
		Last Modified: Wed, 12 May 2021 17:24:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c528feb900a83e812b6024977e2cba1da37b8adfa4a614e33270bfaaab1b124`  
		Last Modified: Wed, 12 May 2021 17:25:23 GMT  
		Size: 86.6 MB (86566812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0712aed3134850c56406a80e44efbb8e6625cc7af98a26fb4471c7b28b6aa96`  
		Last Modified: Wed, 12 May 2021 17:25:09 GMT  
		Size: 294.7 KB (294670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b95904395d9c16df1c5d1e7384fd7b7b96ebad28f179923d6d3f99e9ee8d62`  
		Last Modified: Wed, 12 May 2021 17:25:20 GMT  
		Size: 76.0 MB (75974816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a3bc145bd23d635f2214bfd76c47d6bd8e317965e15918aa47a5421dffc0b0`  
		Last Modified: Wed, 12 May 2021 17:27:04 GMT  
		Size: 504.8 MB (504757489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c4f9f551ff915654ed1ab870267c9af27125d9fb54fc6bf0a709b0eba431e78b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **884.7 MB (884697771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e9d95379b08ac2ed2101852ac61cbf0cf42d2d78631ae4eeaf2250b58accf8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Wed, 12 May 2021 16:56:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 16:56:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 12 May 2021 16:57:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 12 May 2021 16:57:09 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 16:57:13 GMT
ENV LC_ALL=C.UTF-8
# Wed, 12 May 2021 16:57:19 GMT
ENV ROS_DISTRO=noetic
# Wed, 12 May 2021 16:59:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 16:59:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 12 May 2021 16:59:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 12 May 2021 16:59:56 GMT
CMD ["bash"]
# Wed, 12 May 2021 17:00:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:00:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 12 May 2021 17:01:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:08:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a47c6f60e0789df9deab1c6d0d7f8cb24c16d7eacd96db1dc4ccc95359879d`  
		Last Modified: Wed, 12 May 2021 17:18:13 GMT  
		Size: 10.9 MB (10883481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbb414b3cb36665cec81afb9b89e3323578c7734b2b562c99d1c433e7be0c9b`  
		Last Modified: Wed, 12 May 2021 17:18:08 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0ad3e90bde76c71c2d64c447984fc8023340c1aa4f2eb2faa019575ed1ebb2`  
		Last Modified: Wed, 12 May 2021 17:18:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2d8745df976af5256c021771458ba83dc18f5cf3f1fcd6a2e4a791c5e0feb0`  
		Last Modified: Wed, 12 May 2021 17:20:13 GMT  
		Size: 184.2 MB (184206188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f2501093dc7562cf54ae9a5cc4359a6e42c618564f0fb15cc0803e4a7f02af`  
		Last Modified: Wed, 12 May 2021 17:18:08 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9042dc93cbb22220f92d30a7fd12033a8f4c6961070a767c00271d0b4fa2d95`  
		Last Modified: Wed, 12 May 2021 17:21:03 GMT  
		Size: 84.4 MB (84358065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00aa4d21f4f97ad7a33a14ac41958646cf2d6c2cc5364c4d5306fc413ac861b`  
		Last Modified: Wed, 12 May 2021 17:20:25 GMT  
		Size: 294.7 KB (294671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e4ce8ef1fa4e484ca16ed7e501aa5dab20b8f386aedadc0b59c5d68ece33cb`  
		Last Modified: Wed, 12 May 2021 17:21:00 GMT  
		Size: 74.1 MB (74088538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29eab5040f808584555eca11bee2e70b17c5121f3093d4c6dd4ff951a878a970`  
		Last Modified: Wed, 12 May 2021 17:24:37 GMT  
		Size: 481.6 MB (481639640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

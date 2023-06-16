## `ros:rolling-perception`

```console
$ docker pull ros@sha256:89fe3730271a56b684065cb18307a1d43d8d37249225dfc4df37dc43596efbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:404112afacd92f527f984c5eb67fa99545778bebc4493f90108b3ac68b728b6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **958.4 MB (958372278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b906d3d4a9070d782cb6d380f249baa14b49bc9c90b2f6a36168243630bd27`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 03:41:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:41:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:41:43 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Jun 2023 03:41:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 16 Jun 2023 03:41:44 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jun 2023 03:41:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Jun 2023 03:56:05 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Jun 2023 03:56:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:56:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Jun 2023 03:56:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Jun 2023 03:56:45 GMT
CMD ["bash"]
# Fri, 16 Jun 2023 03:57:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:57:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Jun 2023 03:57:15 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Jun 2023 03:57:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:59:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b169f458fb68eaad31436347ddfc7e25dd97c37d8cb63f22e84e7f95d4fa19b`  
		Last Modified: Fri, 16 Jun 2023 04:03:37 GMT  
		Size: 1.2 MB (1212828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bf80c9011de772b9b9ef6bbfe82a4f648cba6a09b044082641c5a232558d5a`  
		Last Modified: Fri, 16 Jun 2023 04:03:35 GMT  
		Size: 3.8 MB (3828743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa9834c66b60b85dc4ddfef495ea84f47531b25092c93ce7cea642ccf57ef2b`  
		Last Modified: Fri, 16 Jun 2023 04:03:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11d2a49f11b048e53a72852bd937876370b9ba2c2448fff57054b14f67466f0`  
		Last Modified: Fri, 16 Jun 2023 04:03:34 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633a85d8b769a40385318439a6f0f1cad7c66a4116b0059a2c48c5c4342830bf`  
		Last Modified: Fri, 16 Jun 2023 04:08:46 GMT  
		Size: 124.1 MB (124135661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca2b18dfa14242c98eb39564e643e0d31b3be2d041ad51b216e2ca5ffe9fd95`  
		Last Modified: Fri, 16 Jun 2023 04:08:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171da17a95f927ae2c266d0d3de58b3fe4341927154d17e35721facfe3eac4f4`  
		Last Modified: Fri, 16 Jun 2023 04:09:06 GMT  
		Size: 85.0 MB (84994585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3468ea45a1acf261f7788a676e5842a16525bcd22e5c962fcda17578cea607d5`  
		Last Modified: Fri, 16 Jun 2023 04:08:55 GMT  
		Size: 288.4 KB (288357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a388e36085189206d87204728e5488d1842c2bb7aa1a1f220ee7918585cd7354`  
		Last Modified: Fri, 16 Jun 2023 04:08:55 GMT  
		Size: 2.4 KB (2405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9083010f25afa882d316ac8c410ca3dc4b74217062605e9d8013032f4dad4d20`  
		Last Modified: Fri, 16 Jun 2023 04:08:59 GMT  
		Size: 23.7 MB (23706079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b11258a0ffaa211656df523f4bfdcc63731fb659bc3f504287135be537ad0d`  
		Last Modified: Fri, 16 Jun 2023 04:10:44 GMT  
		Size: 689.8 MB (689770163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:21f61e7c7791edddb2349ca5155187919a5732f7027d369f26887b6e6e11667b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.6 MB (919615081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3604a059bf89b93332fd8869af4feba6203a290b8c6d340d41d2ef8f43101a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:22:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:22:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:22:20 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Jun 2023 01:22:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 16 Jun 2023 01:22:21 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jun 2023 01:22:21 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Jun 2023 01:39:25 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Jun 2023 01:40:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:40:08 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Jun 2023 01:40:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Jun 2023 01:40:08 GMT
CMD ["bash"]
# Fri, 16 Jun 2023 01:40:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:40:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Jun 2023 01:40:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Jun 2023 01:40:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:42:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254e648ecdfc867db0b42c6dbd4640c3f7f9b6ba3a884f30c88384561d38d6ee`  
		Last Modified: Fri, 16 Jun 2023 01:47:02 GMT  
		Size: 1.2 MB (1213527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f811aafc45c062b5c1d9c3c624d4bff1dedfdc438dd8870309e1dc91901d96`  
		Last Modified: Fri, 16 Jun 2023 01:47:00 GMT  
		Size: 3.8 MB (3801066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7ed4d8208fedb864dbcc1837f588b07dc9126ba57c6f8902e82adb80853b7e`  
		Last Modified: Fri, 16 Jun 2023 01:46:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6454f40413af60c629e3a0ba0acaa7a2a321a8bdf245ab80623052b37f0052d8`  
		Last Modified: Fri, 16 Jun 2023 01:46:59 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7681b598e87b602bd3949a3eee83c75b9389326287e67fb4ebddffee4803501b`  
		Last Modified: Fri, 16 Jun 2023 01:52:06 GMT  
		Size: 121.6 MB (121622225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7263fa8c020c1c3a7ec3dbfe871c520c497b02eb4e41e9c902faca840f7463c4`  
		Last Modified: Fri, 16 Jun 2023 01:51:41 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f079c2928d31a9d9aadbba7319d84caaec10ef28b5b361956af0f8b4442f1747`  
		Last Modified: Fri, 16 Jun 2023 01:52:23 GMT  
		Size: 82.7 MB (82736302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67183db26ea86b357090e2f539378fbadc07d4018e4664be54ff17a4e204f43`  
		Last Modified: Fri, 16 Jun 2023 01:52:14 GMT  
		Size: 288.4 KB (288368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42b58b1c944ab4dbdf7a9517731ae92f60c0b52ffc38ce2b84830cf3eb7c320`  
		Last Modified: Fri, 16 Jun 2023 01:52:14 GMT  
		Size: 2.4 KB (2421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850a5dcaad9eadb53879cc755bfcb0822a3ee0ae43e624742da2c4d26af362b0`  
		Last Modified: Fri, 16 Jun 2023 01:52:18 GMT  
		Size: 23.1 MB (23096329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b961f8f30d2ba754db8817a228ab0b459093408fc2bb2d090f57c90ea9a464fe`  
		Last Modified: Fri, 16 Jun 2023 01:53:55 GMT  
		Size: 658.5 MB (658463222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

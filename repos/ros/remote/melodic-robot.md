## `ros:melodic-robot`

```console
$ docker pull ros@sha256:fc9bf9da7a2dcd356aa0691b4cea8ab091a78cc2a61439162ae0364d4b0e61b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:968a88eed31ed3ec7d9100a3cf2a5f6be9950407ff64d7a4da335a72114ad0cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448462883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ded8d9ec1534c5d39f1875bc9f885a4d7517108c842bfc02e1cbbbcbe812a50`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:05:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:12:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:12:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 04:13:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 04:13:14 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 04:13:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 04:13:14 GMT
ENV ROS_DISTRO=melodic
# Wed, 02 Feb 2022 04:17:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:17:47 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 04:17:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 04:17:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:20:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:20:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 04:22:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:22:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a04d20dede38fb80c5555e5e471ed360ab6d41bc011f0af2d6ec62357562b8d`  
		Last Modified: Wed, 02 Feb 2022 03:36:03 GMT  
		Size: 838.9 KB (838901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5b5354d47a43af88f4ea9a9f017a7d4184f73efe1cea678e67fec853d5c754`  
		Last Modified: Wed, 02 Feb 2022 05:15:10 GMT  
		Size: 4.9 MB (4872126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60dd5fa157690c748c883a16f708f5d376f5dbea45b76a4119fe8c2029d89517`  
		Last Modified: Wed, 02 Feb 2022 05:15:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0013fb67bc5d263ac313f6ea69f033e17ed0b497a62c5d14a5612019a339118e`  
		Last Modified: Wed, 02 Feb 2022 05:15:09 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b1d8d016ef01f792805f9906d7f4938e32fc4bc612399b86b78dca3128b6b9`  
		Last Modified: Wed, 02 Feb 2022 05:15:50 GMT  
		Size: 259.5 MB (259452760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b77b2b9e52a7904da1c4ffa2daae2ab18d7cd49aaefe422485f14ae36914311`  
		Last Modified: Wed, 02 Feb 2022 05:15:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce741898b69ca3781dfc2fd985a85a108cf456debf8b6dd22bcbcd0b0c386526`  
		Last Modified: Wed, 02 Feb 2022 05:16:15 GMT  
		Size: 70.2 MB (70235469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caabde9838107e81a854965dd22e9f0fd9366eea38ecb7966d4ba68af6c783ce`  
		Last Modified: Wed, 02 Feb 2022 05:16:04 GMT  
		Size: 276.5 KB (276509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7484c2a248f9ea84bb9c49527f42e77cdc6d29786f42de8fae78b951fdac5a42`  
		Last Modified: Wed, 02 Feb 2022 05:16:19 GMT  
		Size: 75.0 MB (74994406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4709b1ca6dd0301c5c393c80d86b06c9dcbbcccd07ed73fc52394c22ec09cacd`  
		Last Modified: Wed, 02 Feb 2022 05:16:34 GMT  
		Size: 11.1 MB (11082230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:80356ffe0b31b1ce87d70e3ef62ade22cc00dc6d400060e0e8de30d9775d83d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 MB (396013110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80c1fa5010e397d2fb24ce8d8818df5556f09ea81dceec5fdf91c02b7248881`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:24:47 GMT
ADD file:f5678be7a8216c2848b16665194b944ad8bdf7696d2925a432437feb730cf587 in / 
# Wed, 02 Feb 2022 02:24:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:00:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:00:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:01:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:01:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:01:19 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV ROS_DISTRO=melodic
# Wed, 02 Feb 2022 03:05:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:05:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:05:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:05:15 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:06:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:06:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:08:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ddd1f986797e6622f6e3810028291b19248347b52709a52a74e6dea7ccee961`  
		Last Modified: Wed, 02 Feb 2022 02:29:12 GMT  
		Size: 22.3 MB (22306998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a13c5f3e0b3838377e14a11d204289624c042d330876e3c31326720c4d7633`  
		Last Modified: Wed, 02 Feb 2022 03:31:11 GMT  
		Size: 840.0 KB (839965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6068e70d21b899600a53c2d674310c256ac800a719d3fcfdd734cf60e92d3eb`  
		Last Modified: Wed, 02 Feb 2022 03:31:10 GMT  
		Size: 4.1 MB (4085945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34531b8ea861d18f8d51dc03b87850d8d18b299f2d6b1ebe0b8ebf8a15b3ed3`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579acbc591d9acea07aa3dbff7ade00b16cb57796ad701bc27624222b7af656f`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac0551ba705e2667e48f840f79e3b176a553e1f36cf08900716bd4c33e4b67`  
		Last Modified: Wed, 02 Feb 2022 03:33:38 GMT  
		Size: 238.9 MB (238928288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e30721392aaa57a123c9a6042528a6f2a9d540d03191232f5b206ac1890cf`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1251fbe6e11e670fa2c22ca7555185a87af09b7a00a1ab304466e2f6df89d8`  
		Last Modified: Wed, 02 Feb 2022 03:34:21 GMT  
		Size: 54.7 MB (54704691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e091dbbcdc27d08f83c858d8ab9782a9333716a03aa27d4d1eff19be1c461a0`  
		Last Modified: Wed, 02 Feb 2022 03:33:51 GMT  
		Size: 276.5 KB (276457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a28d93bdcdace9abbf308c29b5a74316a08464be2c22d0734623443d57ae2f`  
		Last Modified: Wed, 02 Feb 2022 03:34:36 GMT  
		Size: 64.7 MB (64746010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d4d1894d4d4734259ce4328e795671cde30e59717a29ccce3e64de9197c6bc`  
		Last Modified: Wed, 02 Feb 2022 03:35:00 GMT  
		Size: 10.1 MB (10122343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e07ad5390b4f1adc8d5324e379cdfff749c1da54687133668c4ab538c597b7cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.1 MB (422061560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee36540cbb50079cb80e0795986ce07d80b135749f19ce5fd6ee7abde42f816`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:10:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:10:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 05:11:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 05:11:09 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 05:11:10 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 05:11:11 GMT
ENV ROS_DISTRO=melodic
# Wed, 02 Feb 2022 05:12:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:12:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 05:12:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 05:12:37 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:13:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:13:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 05:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:14:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5948c01bc8c6d84421fa740c3bf4469bdea2118ab1cfbd547d0c3b0dc36d173c`  
		Last Modified: Wed, 02 Feb 2022 05:36:12 GMT  
		Size: 839.7 KB (839668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b129c4d1619fdde9a8a9d4fb6ffd859db40fbdf64d29e44f6f1b83927de62041`  
		Last Modified: Wed, 02 Feb 2022 05:36:10 GMT  
		Size: 4.3 MB (4263932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff0284082c4469688953fd5218610fca2a288dc6ce4fa57b2e502fb12cfaa88`  
		Last Modified: Wed, 02 Feb 2022 05:36:09 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7485fc64058b8f687ec7b6dbd53858ae6d39c94a0218bf0bebcfbb924bcb9fd`  
		Last Modified: Wed, 02 Feb 2022 05:36:09 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae476dcd446fc6643f69e8813b347b0feb75aac146d0be1404f6fd1e4747ff1`  
		Last Modified: Wed, 02 Feb 2022 05:36:45 GMT  
		Size: 252.4 MB (252361909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea9a2fb634a6f7662904932585bec97089e745e6d61b93477513702a3356160`  
		Last Modified: Wed, 02 Feb 2022 05:36:10 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa6c11ec085c84cce8825ae035e06c25b84688931f6b5e110665f34cf48c06c`  
		Last Modified: Wed, 02 Feb 2022 05:37:05 GMT  
		Size: 63.1 MB (63067349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8cec6c45859e357f169881c823ed032033c84562d449270ad0c5f33abb41a0`  
		Last Modified: Wed, 02 Feb 2022 05:36:56 GMT  
		Size: 276.5 KB (276456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a38e47840795f734f6c3844bcdd77f37eb1731a090b51efb748cd4ec99cde7a`  
		Last Modified: Wed, 02 Feb 2022 05:37:07 GMT  
		Size: 67.0 MB (67002022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5210560f92cfb1e8a6ec5a98a15e75b457d6b56af0f89e53df2b0b2bf3c2b4c`  
		Last Modified: Wed, 02 Feb 2022 05:37:27 GMT  
		Size: 10.5 MB (10518118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

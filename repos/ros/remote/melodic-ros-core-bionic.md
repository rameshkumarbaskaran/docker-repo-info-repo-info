## `ros:melodic-ros-core-bionic`

```console
$ docker pull ros@sha256:e74ac730a084011e1dcf6294e26207e98c9077c076665605cf8e8658b55dfb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:af679a237fa12883249dddc3cb6651c81fff8a02c9d2126c8ed7d8cba4366c29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291874269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fc43379f0ef6ab636d8cc7af3f8eb3c65c7046d051b559db46d9ac8c5e8e51`
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

### `ros:melodic-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:81574e74b25c691033866489463a92fe540be285a2dc77ddef68f6b50d6c1fa7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266163609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03b18dfca19d1eeac5ca2370489745ae376ca1702e84146914f5fa69f5759b5`
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

### `ros:melodic-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d2e788898450a73cde929eaeea33d2bb44225cc3d1ab16534fb2afe8a9bdd5e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281197615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16eb62a8cfb5769f73ffbe89c79727cb37b7b21830eaa14ce0c9fbadb0d7f85`
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

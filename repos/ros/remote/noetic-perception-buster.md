## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:8abadae98bba78dd9625bccd1030e8305e7920b8010787a4148efce7fea1c327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:08e06ab6cf9e9bc92ce20c5db639653a5ccc4a39f0a644ca0be8ba9a8eae2c74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **951.4 MB (951411608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0965503cf726ff4ce7ebfb99527bd04f50700b3d7f5552dd3346d4b8461cc9d0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:50 GMT
ADD file:1fb366429a5df94c7ba642735d6aa77e201f90e0843de03721a6ad19f80ee4e0 in / 
# Tue, 04 Oct 2022 23:26:50 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 10:15:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:15:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 10:15:10 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 10:15:10 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 10:15:10 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 10:15:10 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 10:16:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:16:49 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 10:16:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 10:16:49 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 10:17:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:17:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 10:17:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:21:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b6d6a76ebdbe1e858fec4564af6c6c3fe9e9bf1c502c8c8a51afd0fcf3374d44`  
		Last Modified: Tue, 04 Oct 2022 23:31:15 GMT  
		Size: 50.4 MB (50441102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2341aa83c173ccc7896ed46aadb5f8da7ef58882bd50ab70db04adad01c7dd54`  
		Last Modified: Wed, 05 Oct 2022 10:52:43 GMT  
		Size: 10.9 MB (10893675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4707ffddc54db884ea0f0b8d3dcb59efecf4b23f05ca9678cdb9093afeb503ed`  
		Last Modified: Wed, 05 Oct 2022 10:52:42 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189ff615727a275e72ab0b25ee32ab5bbaf9038ec984ac9590b05ec0bd699420`  
		Last Modified: Wed, 05 Oct 2022 10:52:42 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02002ab3d47e892389b5c1698d3762ba599087c17a75d1c89b38eba2d10e9e73`  
		Last Modified: Wed, 05 Oct 2022 10:53:15 GMT  
		Size: 239.2 MB (239205312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b538c244b3c01ac7f43cbbe81f3828c21d135d04e3f09c2be3cbd996f74e2d`  
		Last Modified: Wed, 05 Oct 2022 10:52:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df699501c681c16e834b1d4c6a0020da7a337123f2599fa0138c7a689abe2c00`  
		Last Modified: Wed, 05 Oct 2022 10:53:34 GMT  
		Size: 86.6 MB (86571557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c877ef0ff6f06ed582cc68bf1bb2a9f3febf8e8d6812c86c77fa110bf09fe22`  
		Last Modified: Wed, 05 Oct 2022 10:53:22 GMT  
		Size: 324.6 KB (324645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6360754d0398a4f26fe2e6909f0d860b818f474a42c16d8f1fb6232def5a53d`  
		Last Modified: Wed, 05 Oct 2022 10:53:33 GMT  
		Size: 76.0 MB (75976232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829343866cdb6d39fe9e6d8009e2e081875e38ce8f48936b829813b8b77dcf1`  
		Last Modified: Wed, 05 Oct 2022 10:55:04 GMT  
		Size: 488.0 MB (487996673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0be734205fcd3bb5d8d7b494b2480ee3c501e8e7bc80a22086c5fae168d0ff18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 MB (867691466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0407a6c31b234440c08346172e561c78fdef9da60394cfc61d02ee81616aff43`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:54 GMT
ADD file:ef2ee78fb3eda698ebec33ff4b6dea672e03908b0f8630a28acb33ec9a7c3e13 in / 
# Tue, 04 Oct 2022 23:44:55 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:42:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:42:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:42:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:42:22 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:42:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:42:24 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:43:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:43:35 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:43:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:43:38 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:44:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:44:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:45:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:504dcdd9b4a0035dba7a55a5312cf594c3d22fb99b7bf676d397c464db919009`  
		Last Modified: Tue, 04 Oct 2022 23:50:47 GMT  
		Size: 49.2 MB (49228885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c286841822dd708cc8ec03c64947552384e955fad5e3df9a73a5acab4aaaed`  
		Last Modified: Wed, 05 Oct 2022 14:11:38 GMT  
		Size: 10.7 MB (10689488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b51b46470fae12ab22dbf0e0f68d92e335b5d2aec01faf4694f688dcff7ed7e`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01f93551ac4426be901cafe628cfa60e541d98154404fcba3cb02cde1d85358`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a850fdf218d14508c13532bd2745504750003968ec91b47bbc2a16d38af0791f`  
		Last Modified: Wed, 05 Oct 2022 14:12:09 GMT  
		Size: 184.4 MB (184402359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46befb9f0b1823e66932ff7e6bd3b3f7ef17e0115617e47457b2e68aa6db3103`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70142cef45c79ed6c16def65c939723b912688d777616cd8f0394a0a9bed62b`  
		Last Modified: Wed, 05 Oct 2022 14:12:28 GMT  
		Size: 84.4 MB (84371054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec293e0c6336ccbd0d0986af98ef8fd2f6e8caebfc5454d01a8d50bf39f3310`  
		Last Modified: Wed, 05 Oct 2022 14:12:17 GMT  
		Size: 324.6 KB (324579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdd5b15718815c6b2b180f7ba28bb586c4071861d49a281db790d1263561842`  
		Last Modified: Wed, 05 Oct 2022 14:12:26 GMT  
		Size: 73.9 MB (73865277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce03a7da0d66f047902e88c4c2a4af4a8a6d8ab4e8e457debc9fbdebb20bfc3e`  
		Last Modified: Wed, 05 Oct 2022 14:13:53 GMT  
		Size: 464.8 MB (464807456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

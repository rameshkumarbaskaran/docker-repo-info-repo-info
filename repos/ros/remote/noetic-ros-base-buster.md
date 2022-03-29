## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:942908bd5b2e42dab678772afa938e3e357c25a1f5e5d1c28c0885326437a659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:e96e34d4dbcd475ca6cf853d057fb8570bf32fc53bcd4435d06411b728d0c121
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.3 MB (463345704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ae4dfb48508ccf4b9cc436b97de0230175db74153eb3b6a7c0b94e10f1afe1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 18:38:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 18:38:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 29 Mar 2022 18:38:10 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 29 Mar 2022 18:38:10 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 18:38:10 GMT
ENV LC_ALL=C.UTF-8
# Tue, 29 Mar 2022 18:38:10 GMT
ENV ROS_DISTRO=noetic
# Tue, 29 Mar 2022 18:39:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 18:39:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 29 Mar 2022 18:39:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 29 Mar 2022 18:39:14 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 18:39:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 18:39:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 29 Mar 2022 18:40:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd41fb40810985980555ad4f3e5c98a2d1fb6aba5406dfb13c3a5751591bb3e4`  
		Last Modified: Tue, 29 Mar 2022 18:43:53 GMT  
		Size: 10.9 MB (10892020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd07b963a0a4666adbf672efe29068ca41a393dbe4e8857520f10bbf6567fbe`  
		Last Modified: Tue, 29 Mar 2022 18:43:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15a903c4ecdd8129ebf93bbb6558cae4631b7c8cbdb52f7b8aabed4da3ec9d8`  
		Last Modified: Tue, 29 Mar 2022 18:43:52 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff0aa132a5f18476525f41162559ac29a36d8d7fae933dc20478fd1e1cdce0e`  
		Last Modified: Tue, 29 Mar 2022 18:44:24 GMT  
		Size: 239.2 MB (239165595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04437849c9723fd4c815474f1c9148d9917c601f413fd74c7f39a9de06b02e7b`  
		Last Modified: Tue, 29 Mar 2022 18:43:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4312d90907c6e468e1d0d5dca383651b811b150e9b6e169af56a5650d492fe38`  
		Last Modified: Tue, 29 Mar 2022 18:44:45 GMT  
		Size: 86.6 MB (86566668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b306a49cda07cd17bf29d90b1b872d94dfefcec3a9a19e13770ae6b052165d7`  
		Last Modified: Tue, 29 Mar 2022 18:44:32 GMT  
		Size: 305.0 KB (304968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e60e6f9eb483ac56169058a0ad6cd0a9f4d5438c948eeb61f5d931c47b346fd`  
		Last Modified: Tue, 29 Mar 2022 18:44:43 GMT  
		Size: 76.0 MB (75976127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ff7e1406a32bc45301b53e2aab3872761b47c6e166aec405a774ec28fb909c79
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402759447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cd741a31d43b56b8d729a4371b343794125e9e692bf9b96d1e0f56811f680d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:08 GMT
ADD file:37cabd1fec04269c22fc158f62ce5bc655934f2e58fb1ff3a1e366a33ba9bc18 in / 
# Thu, 17 Mar 2022 03:22:09 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 00:57:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:57:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Mar 2022 00:58:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Mar 2022 00:58:40 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 00:58:41 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Mar 2022 00:58:42 GMT
ENV ROS_DISTRO=noetic
# Fri, 18 Mar 2022 01:00:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:00:08 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 18 Mar 2022 01:00:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Mar 2022 01:00:10 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 01:00:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:00:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Mar 2022 01:01:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3996f04b7c6c17d8b25c04c7287353b896b4a0b10ab440f47d00573a7d5c3e17`  
		Last Modified: Thu, 17 Mar 2022 03:28:59 GMT  
		Size: 49.2 MB (49222993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cb989cba7dc1d50cf620a207810dfda41194cf7c3488cada787f5828ee2090`  
		Last Modified: Fri, 18 Mar 2022 01:24:22 GMT  
		Size: 10.7 MB (10688147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dc0d7ec12bfae1925877797eaff4b9a4ba48083fd8920a4ccff5b5dd0bb07e`  
		Last Modified: Fri, 18 Mar 2022 01:24:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eae995b77a571bfa585e4b04eb18f60b0cec5688a13afb5be92ba9e38eefe23`  
		Last Modified: Fri, 18 Mar 2022 01:24:21 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743fda29b26873c08cbc5f7efdb9b3a02f08b87dcfc7a69a0f8f684a88c92237`  
		Last Modified: Fri, 18 Mar 2022 01:24:53 GMT  
		Size: 184.3 MB (184325939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d63919ef43f47b1ff0002843cb0ab133ab048f94d0241d53d989f63971f26a`  
		Last Modified: Fri, 18 Mar 2022 01:24:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5617ca4faf4158afbdca7a157ff503b9946d6c29f88eb4c4f3ffa169c50b23f`  
		Last Modified: Fri, 18 Mar 2022 01:25:13 GMT  
		Size: 84.4 MB (84350617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac233a43af2e3ccd2100b8d8bba599ab0599daf41d3991647e2ba9cb5abfb028`  
		Last Modified: Fri, 18 Mar 2022 01:25:02 GMT  
		Size: 304.3 KB (304262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acef00249fd85131df6b4130a40a2480a309cf90d004df97bfc77393581f601`  
		Last Modified: Fri, 18 Mar 2022 01:25:12 GMT  
		Size: 73.9 MB (73865119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

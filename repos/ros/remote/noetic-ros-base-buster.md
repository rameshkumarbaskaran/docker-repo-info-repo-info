## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:39f11ef560ee89ed1b8ac8a6287d9d2702c76d240e3a32c69638204a0fae94bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:07523e427c14d76a7d15e21798929ffb493972f805cefe9896afff381e7cddc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.5 MB (463484686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccde5ae61127d05aafa73f6914f1169741148e92ac0f3f87ecbe22ce394c6a15`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:19 GMT
ADD file:54838b3dbf7839dadd0b29835bbe53ecbfdfde657ef8671ec5ac3cf5867ea069 in / 
# Mon, 12 Jun 2023 23:21:19 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 17:08:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jun 2023 01:20:49 GMT
RUN echo "deb http://snapshots.ros.org/noetic/final/debian buster main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Tue, 27 Jun 2023 01:20:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Tue, 27 Jun 2023 01:20:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jun 2023 01:20:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jun 2023 01:20:51 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jun 2023 01:22:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jun 2023 01:22:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 27 Jun 2023 01:22:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jun 2023 01:22:53 GMT
CMD ["bash"]
# Tue, 27 Jun 2023 01:23:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jun 2023 01:23:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jun 2023 01:24:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac8bb7e1a32398e26c129ce64e2ddc3e7ec6c34d93424b247f16049f5a91cff4`  
		Last Modified: Mon, 12 Jun 2023 23:26:48 GMT  
		Size: 50.4 MB (50448512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9622cf5c15547519baec38e96827f04dc5f08cfb702fc8765dfa47ba9b8eb2bd`  
		Last Modified: Tue, 13 Jun 2023 17:17:32 GMT  
		Size: 10.9 MB (10897084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ca51b4c58c0584ed69a618914b0b2c4f50f9d813aa45705d26d84487111652`  
		Last Modified: Tue, 27 Jun 2023 01:36:31 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed4c52cac8a0cefc5f1c09a110eceba6c8c2dd67b0794fac78a8a76c6eab152`  
		Last Modified: Tue, 27 Jun 2023 01:36:31 GMT  
		Size: 3.2 KB (3221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06558bc538997bfde288afa7ad8dc75a26bf86a173687d8ecb4835c1604a1ed`  
		Last Modified: Tue, 27 Jun 2023 01:37:02 GMT  
		Size: 239.2 MB (239247831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac4de4055bb55cdced21af8b9bd8d7208db93781433edb09ec77f762f66a4a7`  
		Last Modified: Tue, 27 Jun 2023 01:36:32 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9714d55b15206374694f43dbc5e14012e3d3958561691cc600618b51c602a38`  
		Last Modified: Tue, 27 Jun 2023 01:37:21 GMT  
		Size: 86.6 MB (86625286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de079f7ac705565208992d4833c64a6afee5a1f34a9b2438b3008590ad5b22df`  
		Last Modified: Tue, 27 Jun 2023 01:37:10 GMT  
		Size: 296.7 KB (296668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d719d1ece58de5bc6fe76401e990484678c5b27587fae7ba29c19fc41c074`  
		Last Modified: Tue, 27 Jun 2023 01:37:20 GMT  
		Size: 76.0 MB (75965659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ffc821fb32b52c051e4f5a97b2c305ed7ad31914d8de0e2d0c5e277d1cfccfce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.4 MB (403441320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dcf995f7ea60f4ac780a9dfc4d76512664ac690050e8eba87195f1717be7ed`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:41 GMT
ADD file:bb3cb9e6abc423742d7c1b6bc006a7cef70038c5621c71a90a2ae7c1ea29ec63 in / 
# Mon, 12 Jun 2023 23:40:42 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 13:42:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 13:43:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 13 Jun 2023 13:43:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 13 Jun 2023 13:43:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 13:43:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 13 Jun 2023 13:43:02 GMT
ENV ROS_DISTRO=noetic
# Tue, 13 Jun 2023 13:44:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 13:44:28 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 13 Jun 2023 13:44:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 13 Jun 2023 13:44:29 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 13:45:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 13:45:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 13 Jun 2023 13:45:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e8371d57f7426517aead21bff5af0cf321625cac166c86214c439fb67db84243`  
		Last Modified: Mon, 12 Jun 2023 23:45:01 GMT  
		Size: 49.2 MB (49238409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03375f4355e227cafbfa908999c3ddc516dfece8850f794cbfee3d98a3b0e4d`  
		Last Modified: Tue, 13 Jun 2023 13:51:27 GMT  
		Size: 10.9 MB (10902698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87455fe1f6c14ca646af35900faf90365ac3f7e81bed4b81b88e3abb574a4402`  
		Last Modified: Tue, 13 Jun 2023 13:51:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc3c46e762a7441e9f9691783ed4686cefafc163ebd2a456bdf433c89287d8`  
		Last Modified: Tue, 13 Jun 2023 13:51:26 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55db42145f6caf7e455205c09a9a1d3663adc3f0db751eeb654008b42dca4736`  
		Last Modified: Tue, 13 Jun 2023 13:51:48 GMT  
		Size: 184.5 MB (184469619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095f9b9f16405a7957c5409754d18a64bbe1f89878c0017a77fdde5fb330d868`  
		Last Modified: Tue, 13 Jun 2023 13:51:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beeab7876fa087145597e605094b6a924f8619de8caf0255491fc4fa0f2948fd`  
		Last Modified: Tue, 13 Jun 2023 13:52:02 GMT  
		Size: 84.4 MB (84396970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78aec8582d4f1b67ba097e7f015d6d6ad0dce469e56472570a9c1f44adfb35a4`  
		Last Modified: Tue, 13 Jun 2023 13:51:54 GMT  
		Size: 295.2 KB (295178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa121382b620e16c5f9ecbd7272677d1b17895ebb4f1143c54a743fbcd589ed`  
		Last Modified: Tue, 13 Jun 2023 13:52:01 GMT  
		Size: 74.1 MB (74136032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

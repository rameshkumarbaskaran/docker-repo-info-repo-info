## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:3b7a6fc0f08b821468705bb08c44167ac9a8b8c4ec438b747df16f71b9333ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:01b186e3cb098181d56105de494565c91befca6fdb9a0cd0a0a413db5f305be9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300597073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229d3208f89cfcab4653948befc7fc0a1c11f082a4d7db1fc1990c8b8fdd648d`
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

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0c3c1931c6d60e14fb8b0d02bbd8aed5a7c90c5a98f3735c24bcdf966a0377fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244613140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b25b5a7db1983f22e23093166f48474a1a14775201f776944efa2c611324786`
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

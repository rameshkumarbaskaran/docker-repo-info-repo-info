## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:d3989fd09f9eabfedb97ab0cda7f4f00b6f83c9e8214b99e978dd7e926d41aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:9f698f43bd0b2e89db3336119da5fdc8496ffd517ad170b2d7a87f0828db2e51
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.0 MB (462990626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faacc2beaa6996d4edc2f4a5495fdb921f87cff2dc06bc3776a9dcd6d0ffb452`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:52 GMT
ADD file:6014cd9d7466825f80d4a3345847efd6fd7ef600b8135811cab4f0e304f66cd7 in / 
# Fri, 11 Dec 2020 02:05:52 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 19:38:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:38:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 11 Dec 2020 19:38:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 11 Dec 2020 19:38:33 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 19:38:33 GMT
ENV LC_ALL=C.UTF-8
# Fri, 11 Dec 2020 19:38:33 GMT
ENV ROS_DISTRO=noetic
# Fri, 11 Dec 2020 19:39:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:39:40 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 11 Dec 2020 19:39:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 11 Dec 2020 19:39:40 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 19:40:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:40:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 11 Dec 2020 19:40:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6c33745f49b41daad28b7b192c447938452ea4de9fe8c7cc3edf1433b1366946`  
		Last Modified: Fri, 11 Dec 2020 02:12:07 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8976c0b6dafba8e29d428307d1a731a8cf6b1ebef7280ec00f1582e30d70e9bd`  
		Last Modified: Fri, 11 Dec 2020 19:48:43 GMT  
		Size: 10.9 MB (10890369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03728db810730c356cc4e6d117dbb856990d83d8b424404820b83e60d1c0a62f`  
		Last Modified: Fri, 11 Dec 2020 19:48:42 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c01b817549038fd01886fb541048dc802d51175b3d0280699ef1b4a2ce5826`  
		Last Modified: Fri, 11 Dec 2020 19:48:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a229b50b83602782324ede7d94e323985fd1bb2769db16f2cbf549387fd7fe41`  
		Last Modified: Fri, 11 Dec 2020 19:49:31 GMT  
		Size: 238.9 MB (238919867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86cd2429c18dcfca36b2d9dc7c45899f54bd706f389805d0ad288196ec67a94`  
		Last Modified: Fri, 11 Dec 2020 19:48:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6b8eed608456204202cb4ff3bbee64ca412693690552fa5f5c389225dfc1c1`  
		Last Modified: Fri, 11 Dec 2020 19:49:52 GMT  
		Size: 86.6 MB (86563916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be07eeed30e464c010628d1e6d911b526df006276dbdbf8f69dde3e7ccdb7caa`  
		Last Modified: Fri, 11 Dec 2020 19:49:36 GMT  
		Size: 250.6 KB (250559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabc6b683f6cf363ad2eb70b5f9c9cc9fc04f1f5cd6670cd7de3cdefc7783ab3`  
		Last Modified: Fri, 11 Dec 2020 19:49:50 GMT  
		Size: 76.0 MB (75966349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cef481426f8fa3dd47a0c78d99f50afaff15856de3de05bfa6e797de1531284d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402908732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba18fd69c82ad44132b31ca2dcf7cbc85fbc123991583b10169b4dda37c49960`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:23 GMT
ADD file:b08f373022952dba7d08b7fc02909d9e369c9727e0e4f62d6110e41e70e668cc in / 
# Fri, 11 Dec 2020 02:45:25 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 23:25:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 23:25:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 11 Dec 2020 23:25:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 11 Dec 2020 23:25:11 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 23:25:13 GMT
ENV LC_ALL=C.UTF-8
# Fri, 11 Dec 2020 23:25:14 GMT
ENV ROS_DISTRO=noetic
# Fri, 11 Dec 2020 23:27:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 23:27:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 11 Dec 2020 23:27:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 11 Dec 2020 23:27:36 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 23:28:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 23:28:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 11 Dec 2020 23:29:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99e5136f81cd2a8cc226c42435d6f4f30584d168cc51f4d4afd2d5611e4d2215`  
		Last Modified: Fri, 11 Dec 2020 02:52:45 GMT  
		Size: 49.2 MB (49180317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6802a596e847ecc40fc64a4020bce9c6b7ec241a9a0adff6a2f4b93c30b2144`  
		Last Modified: Fri, 11 Dec 2020 23:41:10 GMT  
		Size: 10.9 MB (10882958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d048a0e9c93d12fc2502ef2bd5aff74d265481bfe6a09ed85acc1b9d28d689`  
		Last Modified: Fri, 11 Dec 2020 23:41:07 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89503d24c7d28733c7447800ad677d2131c8d16d0a168ebb554b2b3daaf1a1f1`  
		Last Modified: Fri, 11 Dec 2020 23:41:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215ec51670c89e647b8382b61d566bad5238b2661b6575cae78036b6dbc1da44`  
		Last Modified: Fri, 11 Dec 2020 23:42:01 GMT  
		Size: 184.1 MB (184145865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f19aa0624291920427cd6503ba38ebd048f0d00f4e6f303a9893c73a1d212a`  
		Last Modified: Fri, 11 Dec 2020 23:41:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1e404c27ce42d1a86ea2b5f569c72e14662afd6311cc8246e7404d572a91b3`  
		Last Modified: Fri, 11 Dec 2020 23:42:31 GMT  
		Size: 84.4 MB (84354929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fcf8820144a3531ad73680a7bcfce89b628b8f63a4633f46f390320c0a5778`  
		Last Modified: Fri, 11 Dec 2020 23:42:10 GMT  
		Size: 254.6 KB (254605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e4418084bd7fe7d75ffae62f54e83367b6952bf4674aa4cd51cc4d27d10b96`  
		Last Modified: Fri, 11 Dec 2020 23:42:29 GMT  
		Size: 74.1 MB (74088219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

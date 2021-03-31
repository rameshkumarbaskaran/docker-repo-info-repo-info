## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:49fb42ac6d3074820af2d20498ef644c0dcaf63ba74fc37fea815e53983498f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:23a2aca09e9bd2b0cb4dac86206bfb5805a930470e4f44c7582879688ce44410
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **967.9 MB (967901520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6b537f7859fba695b0fccc1682a13f2e12b806e9651f3afe5d04539c5b3708`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:16 GMT
ADD file:c254898ceb4172f05cd40460f8d0b1ca2d39d5178bdddd4e794c7d3fc5a60a03 in / 
# Tue, 30 Mar 2021 21:49:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:37:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:37:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 31 Mar 2021 14:37:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 31 Mar 2021 14:37:11 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 14:37:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 Mar 2021 14:37:12 GMT
ENV ROS_DISTRO=noetic
# Wed, 31 Mar 2021 14:38:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:38:46 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 31 Mar 2021 14:38:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 Mar 2021 14:38:47 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:39:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:39:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 31 Mar 2021 14:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:42:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:004f1eed87df3f75f5e2a1a649fa7edd7f713d1300532fd0909bb39cd48437d7`  
		Last Modified: Tue, 30 Mar 2021 21:53:41 GMT  
		Size: 50.4 MB (50432842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f283255a7d12fe7da3a43af5ad6efeff536a63cc1a145c14a6c6d400c2322d`  
		Last Modified: Wed, 31 Mar 2021 14:47:40 GMT  
		Size: 10.9 MB (10891959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdde152c73cfc8ca8aac1e9be5a519d900b16728ee48f68186feaef4d3518a9b`  
		Last Modified: Wed, 31 Mar 2021 14:47:38 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1012d5124e2f8e67807fe22a0ab099b073842635953efaad784b05c96bd4623`  
		Last Modified: Wed, 31 Mar 2021 14:47:38 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edb3da76ce6e2975c4054550bdc6e71895240b4c70f6ef4c5b4b959a981a299`  
		Last Modified: Wed, 31 Mar 2021 14:48:23 GMT  
		Size: 239.0 MB (239025852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e286d90affa35dc52952451721ce94d45a6d9716c333a029c34b5a419b6d05`  
		Last Modified: Wed, 31 Mar 2021 14:47:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fae458da7d673a0bc217a7e6f68bbebca2e7dd1c5d166eb48cdedc955f52650`  
		Last Modified: Wed, 31 Mar 2021 14:48:54 GMT  
		Size: 86.6 MB (86566252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fc5b7be04d74b55b5cc95b27a235ba10befdc1beb374f12440e2fc7aa86f67`  
		Last Modified: Wed, 31 Mar 2021 14:48:34 GMT  
		Size: 274.8 KB (274824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4f1ef32145e42cec358a573e74144c8c97f376a16e0bb507aac47c7c70ccdd`  
		Last Modified: Wed, 31 Mar 2021 14:48:47 GMT  
		Size: 76.0 MB (75975096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3194b760bb26437618b19cfc6b095a81db7786788a012bc59dda54e89a03f358`  
		Last Modified: Wed, 31 Mar 2021 14:50:41 GMT  
		Size: 504.7 MB (504732855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:73e5c9268bdcf46ac7113342225b358029486bf84eaa89f92166352ef668a5ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **884.7 MB (884655379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f1289979a68dd15a6428fe3a8bc6b319d26c6e3a67e0be3d0c855c052d634f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:46:50 GMT
ADD file:6a5cce92f1039ef2cb7ac6dd999c9f84289a9f6e1c0891d1edf791ea73b7e125 in / 
# Tue, 30 Mar 2021 21:46:53 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 13:49:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 13:49:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 31 Mar 2021 13:49:20 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 31 Mar 2021 13:49:21 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 13:49:22 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 Mar 2021 13:49:23 GMT
ENV ROS_DISTRO=noetic
# Wed, 31 Mar 2021 13:52:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 13:52:35 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 31 Mar 2021 13:52:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 Mar 2021 13:52:37 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 13:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 13:53:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 31 Mar 2021 13:54:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:00:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef28e7e77ecbd3b3b426832bc12e8f5e629959683767466e9bac149c3286e126`  
		Last Modified: Tue, 30 Mar 2021 21:54:03 GMT  
		Size: 49.2 MB (49225808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b10597693b224937ce4d457543a06dce5f11624a25fa61e62534b154013a92a`  
		Last Modified: Wed, 31 Mar 2021 14:08:28 GMT  
		Size: 10.9 MB (10883525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c008f3dddbf040a2e694f39105725834300ae8f8477c9dbbd5c79b5cb23199a`  
		Last Modified: Wed, 31 Mar 2021 14:08:26 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add46ffbec133da5c01b9a88e9e3989183c864f9619f612cde268cb3c36438bd`  
		Last Modified: Wed, 31 Mar 2021 14:08:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574e6d0cf1ff497632a742787107585220c26cabe302cb5bd891ab5baa174f94`  
		Last Modified: Wed, 31 Mar 2021 14:09:49 GMT  
		Size: 184.2 MB (184204230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b94776c6c910590000e226121d2215ae485328207fdde890c502a6534b73c`  
		Last Modified: Wed, 31 Mar 2021 14:08:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9630b0c397b1e57dd750dbb39bf40b5b90c14f4d033e3f5d8eff5a454038643f`  
		Last Modified: Wed, 31 Mar 2021 14:10:17 GMT  
		Size: 84.4 MB (84358908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c435ce95597dbc5279339cade8cd740061c12cca6b61e3be9d4bdeb5d84e625`  
		Last Modified: Wed, 31 Mar 2021 14:09:57 GMT  
		Size: 274.8 KB (274834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e702c0310f7256e54459711a324685c55275c8471b1138e525692b2aa5c9bd`  
		Last Modified: Wed, 31 Mar 2021 14:10:14 GMT  
		Size: 74.1 MB (74089164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2baa98ee54570149903dfde957b905737f138d1297b0361e945f3fd51468639d`  
		Last Modified: Wed, 31 Mar 2021 14:13:01 GMT  
		Size: 481.6 MB (481617071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

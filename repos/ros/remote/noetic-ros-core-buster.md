## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:b2fde036f3de5422f91918ec5eabbbc8b8d2774234d91b5b00f6df0374c2b48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:90c56753aedf355cba83f0d20c64c0102366f21eb990ad7fd3ae0cfa98ea2685
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300352493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd3b30a45de7fe8727448bd992d227677855cc97d657cbf3498e5de784fbbd0`
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

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c581d3fa1d63bc526ff812e98aa17c6c95015530b8181a230cb7a57f13806ad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244315402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7e91512e3c57818690c056b8d49b5f401f751484d1e179d2cd5ad04b54d223`
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

## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:fd9e03a878cadcb365ccb236cd47c36dc1a19ce4105becedd4e9418dc8d1ca1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:8fc740c4c663c10544f1c6fcbe0d9ed232d15725bc41d4b4ee256a5cc193f534
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.5 MB (484451700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca0c9f7c246ad81ee27739eb65046725966c9334246e9e1571884a8cf33cdf6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:54:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:54:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 17 Aug 2021 14:54:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 17 Aug 2021 14:54:12 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 14:54:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Aug 2021 14:54:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Aug 2021 14:55:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:55:18 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 17 Aug 2021 14:55:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Aug 2021 14:55:18 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:55:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:56:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 17 Aug 2021 14:56:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6a25b8c075beb4891f7c9088956d2a452f32036d8126e37217b5b62fd7024c`  
		Last Modified: Tue, 17 Aug 2021 15:02:09 GMT  
		Size: 10.9 MB (10891952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e00b43ac20734a706cb03369661415e15f6856a48275dcd4fe7744b0bde5d23`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b19825ce46253a4664a6e606382250ba22ec8d0e1d13516be7d225efcca57f`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034eef40d3fabaea23b5d4473263a3a6ab8cd3545504c1ba16818b3b90152d1f`  
		Last Modified: Tue, 17 Aug 2021 15:02:50 GMT  
		Size: 239.1 MB (239050839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ae7d371ba1fee4f46bf91b9a18289de1dd3472eb2c3b8458f8ff2df5825c78`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b4384fc4992e164b0946674e8bf7905f6037fbe56d20552b0a9f981e0b23df`  
		Last Modified: Tue, 17 Aug 2021 15:03:21 GMT  
		Size: 86.6 MB (86566411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6466d96361536da7163da2fbe6e4e5267a768c30f1f04480d818c767e0ef32`  
		Last Modified: Tue, 17 Aug 2021 15:02:59 GMT  
		Size: 310.1 KB (310086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da0dad1381eb1948df8e9a05518d305a6b3a7df20eb1f0b82edb2a00bee76b`  
		Last Modified: Tue, 17 Aug 2021 15:03:19 GMT  
		Size: 76.0 MB (75975146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb420023d0d4981e7e1c712cf7670854d7160f6cd251076d6fa94d822b18cef2`  
		Last Modified: Tue, 17 Aug 2021 15:03:35 GMT  
		Size: 21.2 MB (21218651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a71321e849437464740dadf3a7d92ba33aa9cd325313096b2092348fc5582503
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423996486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1339d6e7c2ba9eca967117d5d0a6a8b425002eb4c8f7803111013392eb2e9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:16 GMT
ADD file:9e7d801ba29c50f7388cf80395faef75e0b4db056e16d1117293539bda895467 in / 
# Tue, 17 Aug 2021 01:46:16 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:48:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 17 Aug 2021 11:48:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 17 Aug 2021 11:48:59 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 11:48:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Aug 2021 11:49:00 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Aug 2021 11:49:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:49:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 17 Aug 2021 11:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Aug 2021 11:49:54 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:50:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:50:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 17 Aug 2021 11:50:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:51:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b721438f56fc7c4bf10a9f9ac58d22b52d97c50353a44f531fb5b7a70314e642`  
		Last Modified: Tue, 17 Aug 2021 01:53:52 GMT  
		Size: 49.2 MB (49222362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21602f601a18ce34c8a479ae1d7bac4442282478925664d6f67ad1d2b34e020`  
		Last Modified: Tue, 17 Aug 2021 11:56:11 GMT  
		Size: 10.9 MB (10883354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630d4e557cfdbdf3a855acc0ae4cb3c204ac63ae1dd071cd42e608dcb0645c2d`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f24119c6422825783e8ee727d9b12a12c7cb5605e9b6e883b5101a388b450a`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd82c4517707ac42892fd33d02b10b53c8eb41cf05683d381df617056c035fd`  
		Last Modified: Tue, 17 Aug 2021 11:56:42 GMT  
		Size: 184.2 MB (184236324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5bbd42e097110d8576baa6d6d16c7a91e608fad20f3b7978c7e0e99f4ee7df`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf124f136abb277ab2e63f14af6802ccc288e34cc0c43a7d62f7c42717f23e3`  
		Last Modified: Tue, 17 Aug 2021 11:57:03 GMT  
		Size: 84.4 MB (84358116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6515efab5054193f9a8defd851ec9536c17950ae722b38778b4bd6aef481e9`  
		Last Modified: Tue, 17 Aug 2021 11:56:51 GMT  
		Size: 310.1 KB (310090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa915bc3d0bc2ea62806da8704257a5df824c41fa8997831b5de9ac482cca14`  
		Last Modified: Tue, 17 Aug 2021 11:57:03 GMT  
		Size: 74.1 MB (74087852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f1b5f110e2990823b69a716c68ef7506a92319e4d3c59c1991db59244653d1`  
		Last Modified: Tue, 17 Aug 2021 11:57:14 GMT  
		Size: 20.9 MB (20895975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

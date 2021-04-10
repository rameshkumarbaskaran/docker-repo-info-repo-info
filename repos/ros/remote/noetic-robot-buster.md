## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:899dadb4fb96b064178f27c191b27bfe0079f441d282e53a750ff7a4f8cbbd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:feec5f25ab7ba32e93553549c6e1d50a76e26cb4c22e3c57ec934f0c3ecedcba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.4 MB (484383620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3caa47b772dc895fcb4468d85ce67be6a92f83f9a75a9bf0c58bfe5d912c1341`
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
# Wed, 31 Mar 2021 14:40:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:36363f8141f157b9cce67d4b23de20dc0fe74dc071392d15d4471b48a1ba0d7e`  
		Last Modified: Wed, 31 Mar 2021 14:49:08 GMT  
		Size: 21.2 MB (21214955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:aa51bb6360e7bac0da5813c7e375b6b285b410f751f7ac387a99275a39a1d56c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.9 MB (423903217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3346eb67997304b948f0b8ece9a4611ea3f122d9e2effe10c89b4af3624e807b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 15:37:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 15:37:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 10 Apr 2021 15:37:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 10 Apr 2021 15:37:16 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 15:37:17 GMT
ENV LC_ALL=C.UTF-8
# Sat, 10 Apr 2021 15:37:18 GMT
ENV ROS_DISTRO=noetic
# Sat, 10 Apr 2021 15:40:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 15:40:17 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 10 Apr 2021 15:40:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 10 Apr 2021 15:40:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 15:41:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 15:41:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 10 Apr 2021 15:42:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 15:43:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36a3b7dee476a7c21f147f8ba83dfd7c574332ae1351bab531f996d1f40d252`  
		Last Modified: Sat, 10 Apr 2021 15:56:28 GMT  
		Size: 10.9 MB (10883505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d476645129f490eb4af61264fcab0cb2bd9eb9af56e8c2a84a027e733bbb7a`  
		Last Modified: Sat, 10 Apr 2021 15:56:26 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed05dd4c3440f5d1ca1c0b4deec634cee528af76b508e0909d0d75d0f0ac896b`  
		Last Modified: Sat, 10 Apr 2021 15:56:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbd4e4275f95551283e9dade9816ebd70b2885ef7d355b9c6bad63be31d7863`  
		Last Modified: Sat, 10 Apr 2021 15:57:30 GMT  
		Size: 184.2 MB (184202626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147fa70d954f9519fefbf0d8866f60d576cf506dc64a41f60f017b8ef416f838`  
		Last Modified: Sat, 10 Apr 2021 15:56:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a473f227cf740e3c139957b5ddf02997e137c602d3be3a576ce51dd91696eb0`  
		Last Modified: Sat, 10 Apr 2021 15:57:57 GMT  
		Size: 84.4 MB (84355758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37993ff61eb58e3fbe83d66af5f42aa709c1bdec6617606cee9423557fcd8fa`  
		Last Modified: Sat, 10 Apr 2021 15:57:36 GMT  
		Size: 276.4 KB (276397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51720a1eccbe930e8c3ca42e1259593fb1e914af8375becab8e6436e929bdab`  
		Last Modified: Sat, 10 Apr 2021 15:57:56 GMT  
		Size: 74.1 MB (74089062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3dc8e191354812f0a2afb846422ce84fb08e1373ea1036bd45e9fe48756795`  
		Last Modified: Sat, 10 Apr 2021 15:58:10 GMT  
		Size: 20.9 MB (20868250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

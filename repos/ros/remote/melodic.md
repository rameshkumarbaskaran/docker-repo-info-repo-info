## `ros:melodic`

```console
$ docker pull ros@sha256:7855b75a1db59649a3667c2114bf9a8fac96e90dc28a87656955d5f95b51eddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic` - linux; amd64

```console
$ docker pull ros@sha256:96705e5651a424f55c89221f8dc76f79b55250584b6f953a220c8b1c31ba78bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.8 MB (437775055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b924cfe48d0df443d8c4c1693973e973ab20545c4bc875ca1f38e2c8820150`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:55:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:51:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 19:22:20 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Mon, 03 Jul 2023 19:22:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Mon, 03 Jul 2023 19:22:22 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jul 2023 19:22:22 GMT
ENV LC_ALL=C.UTF-8
# Mon, 03 Jul 2023 19:22:22 GMT
ENV ROS_DISTRO=melodic
# Mon, 03 Jul 2023 19:26:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 19:26:18 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 03 Jul 2023 19:26:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 03 Jul 2023 19:26:18 GMT
CMD ["bash"]
# Mon, 03 Jul 2023 19:27:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 19:27:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 03 Jul 2023 19:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27456075680427d55e79ddce0ccec278d1f81ab5181d13386de5ac3f085b90`  
		Last Modified: Fri, 02 Jun 2023 01:02:13 GMT  
		Size: 818.9 KB (818915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8c91ad7650f55a57d952458067fa5d43fc42f60aa1300eac0321468efd7f1d`  
		Last Modified: Fri, 02 Jun 2023 02:17:44 GMT  
		Size: 4.9 MB (4878354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0683d606786339b4368e89c6aaf1c72169b6aa7e6630aefddaeac503bc6552bc`  
		Last Modified: Mon, 03 Jul 2023 19:35:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66495e509f4c45b21e332a761ce4b1d4f207417e3e0b51b3c71dad8e9697cce`  
		Last Modified: Mon, 03 Jul 2023 19:35:21 GMT  
		Size: 2.4 KB (2406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c731a0490674b377c6cd43c7d5012868bf98a22b30417a9bbbc9f016d73d07c`  
		Last Modified: Mon, 03 Jul 2023 19:35:53 GMT  
		Size: 259.6 MB (259612161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f9d35f26e100c81e0e5c8ceecdf6a25d7beb14187fb876d869b81530cf831a`  
		Last Modified: Mon, 03 Jul 2023 19:35:21 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417956853271dd45a847801f29dc2a06fe7d594a677a67abef90a7d63b95806`  
		Last Modified: Mon, 03 Jul 2023 19:36:11 GMT  
		Size: 70.5 MB (70460187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a12ca12306ba5f87d1bba2dcd5e4f882dff48c2cae9e526cd23657a941d829`  
		Last Modified: Mon, 03 Jul 2023 19:36:01 GMT  
		Size: 284.8 KB (284821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fc4b75f8dc61a781d06a268987b8cbac8c0df0fc2e30457cfc6f0a23d9e032`  
		Last Modified: Mon, 03 Jul 2023 19:36:12 GMT  
		Size: 75.0 MB (75000427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm variant v7

```console
$ docker pull ros@sha256:e190b65b72c48b0cc22ab5fb3f4980fb7a6802c3f47b9e20ade5a13658ff7e5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.4 MB (386370980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4121174d917958759b30991c500040c93792e9a9eb1116f5c20cc28d56fbb6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:52:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:52:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:52:20 GMT
ADD file:d570ab6bd7d664cc6547b6ae228cf825333d9d841969911c7d62afe3ed440803 in / 
# Tue, 30 May 2023 09:52:21 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:03:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:03:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 19:35:29 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Mon, 03 Jul 2023 19:35:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Mon, 03 Jul 2023 19:35:30 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jul 2023 19:35:31 GMT
ENV LC_ALL=C.UTF-8
# Mon, 03 Jul 2023 19:35:31 GMT
ENV ROS_DISTRO=melodic
# Mon, 03 Jul 2023 19:40:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 19:40:04 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 03 Jul 2023 19:40:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 03 Jul 2023 19:40:04 GMT
CMD ["bash"]
# Mon, 03 Jul 2023 19:40:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 19:40:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 03 Jul 2023 19:42:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76bc0c6b06fc92c1f911be6147b55b6430301b80e4062178329c4fa8a0f79f51`  
		Last Modified: Thu, 01 Jun 2023 23:54:31 GMT  
		Size: 22.3 MB (22312178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296f87f37d6a7831a2d27cf9ba67dbb404857632b477ce335ecbe521cd84db2d`  
		Last Modified: Fri, 02 Jun 2023 00:15:23 GMT  
		Size: 820.3 KB (820335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a424966fc7947ef55ca4db8ed69abeb762dbe613d82cb7b6c248b55d4a76fe8d`  
		Last Modified: Fri, 02 Jun 2023 00:15:22 GMT  
		Size: 4.1 MB (4090754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ab58b432ab762c3e066cf1bbb2cf2cb6e184f7ba4d5eccebe3002f9e0d7f25`  
		Last Modified: Mon, 03 Jul 2023 19:49:13 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31905fc086a9d671f7d3e78111401be4f09982743b2729cab2cedb7226b57932`  
		Last Modified: Mon, 03 Jul 2023 19:49:13 GMT  
		Size: 2.4 KB (2406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac92b51d2d7d1dac38b1cc25ba69f7d4e96a35293a72149ba318d3cf92376ffd`  
		Last Modified: Mon, 03 Jul 2023 19:49:46 GMT  
		Size: 239.1 MB (239075082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e085617659d8479bc89c2ae48b56fbeac53b0f2a62edaceb1393bca8ae6dbb1`  
		Last Modified: Mon, 03 Jul 2023 19:49:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc471e0ec79b120efa3e3231e93a6472f7fad09fc16c69b2fa66b8b7ea485658`  
		Last Modified: Mon, 03 Jul 2023 19:50:02 GMT  
		Size: 55.0 MB (55034056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415295eab38f1ccb1544603febc3cf15e980ca1fcc51d9d01410616fd691866b`  
		Last Modified: Mon, 03 Jul 2023 19:49:55 GMT  
		Size: 284.9 KB (284862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccc4909a878ecd5f89a2673ccb55e2a8adae0884350b325c8addd6cb1769b20`  
		Last Modified: Mon, 03 Jul 2023 19:50:05 GMT  
		Size: 64.8 MB (64750877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:016c8d65cd94acf72f71f1cccb07f5ccc7b37cd06a15e4ae8797ca9049393ba0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.3 MB (412347515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78be2a7f6c6d7ca30d92068bbcae735ea8a2e62719c7a58882a5bc433307434a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:07:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 18:54:30 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Mon, 03 Jul 2023 18:54:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Mon, 03 Jul 2023 18:54:31 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jul 2023 18:54:31 GMT
ENV LC_ALL=C.UTF-8
# Mon, 03 Jul 2023 18:54:32 GMT
ENV ROS_DISTRO=melodic
# Mon, 03 Jul 2023 18:58:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 18:59:00 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 03 Jul 2023 18:59:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 03 Jul 2023 18:59:00 GMT
CMD ["bash"]
# Mon, 03 Jul 2023 18:59:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 18:59:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 03 Jul 2023 19:01:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f5d58f6c858f92b45f1d3e366bcabef3c6821ccaa9ee17c59beb643029cb4d`  
		Last Modified: Fri, 02 Jun 2023 00:41:19 GMT  
		Size: 819.0 KB (818994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9e738cf9edf30ed3cf9686d84733d2d3d3ee28a85c58ada09fabd9660ed336`  
		Last Modified: Fri, 02 Jun 2023 00:41:18 GMT  
		Size: 4.5 MB (4461671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb15c91065685951357c563d50225475bf62ccf00e185b08b5d5aa0d828f9e9`  
		Last Modified: Mon, 03 Jul 2023 19:08:53 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaf40387f745b8b6c023a4647f5ce4a9f784107d4ba1d4356d41f6ccd21a5d9`  
		Last Modified: Mon, 03 Jul 2023 19:08:53 GMT  
		Size: 2.4 KB (2404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d28df4590da4d1b3e217e5b8b28fed95ce13c54228ee8335465c1b72839ef3c`  
		Last Modified: Mon, 03 Jul 2023 19:09:17 GMT  
		Size: 252.5 MB (252524042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffda3f020806b222794eaaa7b5f1cf412f7ebf13aad2e650fd36980f6649787`  
		Last Modified: Mon, 03 Jul 2023 19:08:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce65a51b0331e8a1ff1c5bd34f6cf61bb21789c246ed43c0465eecddf10e14`  
		Last Modified: Mon, 03 Jul 2023 19:09:32 GMT  
		Size: 63.3 MB (63279594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b5c3f121b18d97b4bd63e2476c9c60549acd8148c5c11fd04bd08f5c70d877`  
		Last Modified: Mon, 03 Jul 2023 19:09:26 GMT  
		Size: 284.8 KB (284817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529a658836e677ca17fd290d1d7bb810935536e4e53a459435294c426cad64b3`  
		Last Modified: Mon, 03 Jul 2023 19:09:34 GMT  
		Size: 67.2 MB (67234662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

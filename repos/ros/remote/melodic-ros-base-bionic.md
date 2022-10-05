## `ros:melodic-ros-base-bionic`

```console
$ docker pull ros@sha256:3fb81f5456c132b4dfc3084ffd723dc16b4b2b665ddaf9c2213a1fff8ef3262f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:8e83dbb13e46ad46ade95f14a41d9cb1f52b0ded3671ec0ca47da2a75405caa2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437522644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19100de5b02016f5969462e71fb3370efde59d2bb6f50e78a774079ca02d19d6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:04 GMT
ADD file:ed601c56cf74241eeb1971b24ed969fb855cd2b9330276d3c5779ecdb0b28364 in / 
# Tue, 04 Oct 2022 23:35:04 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 09:49:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 09:49:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 09:49:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 09:49:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 09:49:44 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 09:49:44 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 09:49:44 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Oct 2022 09:53:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 09:53:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 09:53:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 09:53:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 09:54:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 09:54:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 09:56:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e706e0a9f42365312b366bf4caa22f3cdd8fc7fd8f6f49b4dd3782711f66aca7`  
		Last Modified: Tue, 04 Oct 2022 11:37:26 GMT  
		Size: 26.7 MB (26711852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ec163f2e73ca4c7df5142df330fb9169325367e235b65c457afcc3bf320f35`  
		Last Modified: Wed, 05 Oct 2022 10:47:14 GMT  
		Size: 831.0 KB (831002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc154e3f17c6b6f2816c50c8a5bdf831cd4d8813015cacf86568d64746596b6`  
		Last Modified: Wed, 05 Oct 2022 10:47:12 GMT  
		Size: 4.9 MB (4873641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfe6435278fe5856644c183f90cfb982b207bddda62c63a94d6a938acffaa85`  
		Last Modified: Wed, 05 Oct 2022 10:47:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d8283d791cae1e7c3329c4a1d8f4bc0476769b04e9ce92d6a97fe84026c059`  
		Last Modified: Wed, 05 Oct 2022 10:47:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab60f51f309df710bd88888532e7f25291a9e1d1f54e49a7af43e0771994831f`  
		Last Modified: Wed, 05 Oct 2022 10:48:02 GMT  
		Size: 259.6 MB (259558625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b4b730c4ae1b037fe75c6ca063e9c629e1ed238654786a73fabd60b4ed9719`  
		Last Modified: Wed, 05 Oct 2022 10:47:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291c878123af7c6629193bffe3aef7b2e41bc7e5b6d8d6c195e41a0afa072a2e`  
		Last Modified: Wed, 05 Oct 2022 10:48:23 GMT  
		Size: 70.3 MB (70259758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233ad80e5d2bd29146fac7ab104b0a8959214abd2c1e6381db3da5f889ec798c`  
		Last Modified: Wed, 05 Oct 2022 10:48:12 GMT  
		Size: 287.6 KB (287643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13911ccd58f2742aeb456bf670156ec35a6d1bb3670c9ba7d5a709b0201e2388`  
		Last Modified: Wed, 05 Oct 2022 10:48:28 GMT  
		Size: 75.0 MB (74998281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:df938dbfce72ec195200566eb00a046505a08bd0468c8d38f6853705b651be2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385999606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df02f2bbc53d38e90f00067ea8a4879191d1479c4dc6c613203aed1c27cc4e85`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 19:33:23 GMT
ADD file:45c82fca220161f3905a06e276f12ec0cb3be5c099cca70bb6d495da10088f7d in / 
# Tue, 06 Sep 2022 19:33:24 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 20:02:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:02:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:02:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 06 Sep 2022 20:02:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 06 Sep 2022 20:02:33 GMT
ENV LANG=C.UTF-8
# Tue, 06 Sep 2022 20:02:33 GMT
ENV LC_ALL=C.UTF-8
# Tue, 06 Sep 2022 20:02:33 GMT
ENV ROS_DISTRO=melodic
# Tue, 06 Sep 2022 20:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:04:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 06 Sep 2022 20:04:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 06 Sep 2022 20:04:42 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 20:05:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:05:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 06 Sep 2022 20:05:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:074d633b5bde02245e333b110dde5850e06ea4ebefe4283af6e4dfd8d462b170`  
		Last Modified: Tue, 06 Sep 2022 19:35:07 GMT  
		Size: 22.3 MB (22305954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0da4089b68bf46009d284fa16ca1d621c7049f3db1038f87fdc58aa3e52059`  
		Last Modified: Tue, 06 Sep 2022 20:09:19 GMT  
		Size: 832.1 KB (832054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb5783e1925df093ff571a9432fe1c845b3ece17f25ceaf82d5608e22b05bd1`  
		Last Modified: Tue, 06 Sep 2022 20:09:17 GMT  
		Size: 4.1 MB (4088159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292f716a6e78a03f97c202a01a3e1e98cf10bed5364c7c32c839c867d13681a6`  
		Last Modified: Tue, 06 Sep 2022 20:09:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ca0dfda7d5b871d65a21978a3eb27b0e0df4356a07344a412a47884c99fa97`  
		Last Modified: Tue, 06 Sep 2022 20:09:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f2026bdd33971a08db14214c57a9844a8b07c0419dd4f91cdb452cc945d2da`  
		Last Modified: Tue, 06 Sep 2022 20:10:01 GMT  
		Size: 239.0 MB (239016534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409e6ba5da3e6f8d9bfe01490e9a5fdbc6c46106af86015aa53de972cf17fb92`  
		Last Modified: Tue, 06 Sep 2022 20:09:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18156240d002de6754c981e2a6b01263d8e5b2ed7533d540aed2523a440b8969`  
		Last Modified: Tue, 06 Sep 2022 20:10:24 GMT  
		Size: 54.7 MB (54720950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe655b5f5872d42a2aa6dc285aee77585f2b351d69bf0fa7e469e55e08d5b4d`  
		Last Modified: Tue, 06 Sep 2022 20:10:14 GMT  
		Size: 285.5 KB (285538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056747a254333c4839465266c56c71c9917689606230324d5718be769198ebce`  
		Last Modified: Tue, 06 Sep 2022 20:10:29 GMT  
		Size: 64.7 MB (64748572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:aa69b5ba8c09387ac30a0a61a0915bcd1f531fe8cdb6ddf06653e24ea840e3ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411708652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58250c8a80c58321b727945b00fdd1165730914bd9abdd446325c8c22ed25710`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:49:02 GMT
ADD file:26cb5ace98a4462b36211bf28f1e73781dd6d8984350d9bd53243dbe50ae180c in / 
# Tue, 06 Sep 2022 18:49:02 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:39:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:39:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:39:34 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 06 Sep 2022 19:39:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 06 Sep 2022 19:39:37 GMT
ENV LANG=C.UTF-8
# Tue, 06 Sep 2022 19:39:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 06 Sep 2022 19:39:39 GMT
ENV ROS_DISTRO=melodic
# Tue, 06 Sep 2022 19:41:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:41:03 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 06 Sep 2022 19:41:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 06 Sep 2022 19:41:06 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:41:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:41:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 06 Sep 2022 19:42:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d30cf2a6a25aea48a115837d149468c8de7df7fb51f210b9fa1173c065f7b34c`  
		Last Modified: Tue, 06 Sep 2022 18:50:34 GMT  
		Size: 23.7 MB (23734076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c4f657f16f312fa6dcdfe1497bf20b105de50db3390adc504f994c2e9f5b26`  
		Last Modified: Tue, 06 Sep 2022 19:47:40 GMT  
		Size: 831.3 KB (831309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0409a4a76860508a3bb6248ebf7f6c0e2710dcd922c36a4959dd70bc0bd27e`  
		Last Modified: Tue, 06 Sep 2022 19:47:38 GMT  
		Size: 4.3 MB (4265677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8c9b1355942f3d60e38808189d3e6d165d5be537fefc37fa08042bc39b874b`  
		Last Modified: Tue, 06 Sep 2022 19:47:37 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890877cc8e4438ec9389664d9d410292ebcaed1e9f7bb0790d11083308930c25`  
		Last Modified: Tue, 06 Sep 2022 19:47:37 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d08560eb8db9469de77a96e0f07ccc2d8735796b72d3360b34d33ea2ea3e9e`  
		Last Modified: Tue, 06 Sep 2022 19:48:12 GMT  
		Size: 252.5 MB (252503601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7dfbfc923a78aa6af356834ddc818505716f9ed414c5c15cd9563f4df2d3a4`  
		Last Modified: Tue, 06 Sep 2022 19:47:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e737e5219269563197c5a1752c0204a040cbf1b5392ed477a228b2aad8429087`  
		Last Modified: Tue, 06 Sep 2022 19:48:33 GMT  
		Size: 63.1 MB (63088672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcec473689040d5e1f94c9b1369ff622507a6679936505c84d0d2928fc5dcc0`  
		Last Modified: Tue, 06 Sep 2022 19:48:24 GMT  
		Size: 285.4 KB (285399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c063648ef6b170ec80363adfdf39d3c9585b60a8ec03510bc5872de9a351f87`  
		Last Modified: Tue, 06 Sep 2022 19:48:35 GMT  
		Size: 67.0 MB (66998115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

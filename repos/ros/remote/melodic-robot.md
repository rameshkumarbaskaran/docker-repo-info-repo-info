## `ros:melodic-robot`

```console
$ docker pull ros@sha256:392b36d1645180f99de9b697c5fadc5cefe412308be89d7a532c4d1fbe88c222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:35d1cf663f1a54a281580c2635a49b9c6d6a88c05d0d274a388119967f5cf002
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.6 MB (448608427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c691edf515ea30216d1741a1934d63e937bf0f449327f950b79fb9b8a7b74a15`
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
# Wed, 05 Oct 2022 09:56:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:10d82b23298ae87a9d9bc3caf9b4a446fb35de0b2b379eab7db9d03b17e29c17`  
		Last Modified: Wed, 05 Oct 2022 10:48:42 GMT  
		Size: 11.1 MB (11085783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:9d1bfcc3ab99d0a7ea08798214b449ab3e8f6d0d6206950e4f3e9cd6ed454bf3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 MB (396123532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0175165ca9399f5a1ca1c0d297d41135f01c1ca51a56dffc96e86c2e4e6f62`
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
# Tue, 06 Sep 2022 20:06:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1065de2998b586f61746026e5c3c33ef30e1eaff6dc5b28ad1ca62c912d41255`  
		Last Modified: Tue, 06 Sep 2022 20:10:47 GMT  
		Size: 10.1 MB (10123926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6af49c17eb45365833a3015658f71db8cb1496edd7c4196ca5d44baf8cc6bae9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422447622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21b2b650b73f497fe2b2d6860d64416bf68f4185a20ce627275830641d309d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:02 GMT
ADD file:4beae13e1fd7bb92776c08a5cd95feb81b8b3c80522ed8513f2441adfb1661ac in / 
# Wed, 05 Oct 2022 00:02:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:31:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:31:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:31:40 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:31:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:31:42 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Oct 2022 13:33:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:33:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:33:08 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:33:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:34:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e9b69cf8198dafe5b7db1eee7b96b96238f8346ec641dd44f961f7996c2c152`  
		Last Modified: Wed, 05 Oct 2022 00:03:33 GMT  
		Size: 23.7 MB (23734594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe90d911d5615b705080d27fba0823b4f14f420d2d26ab56026456d57781d53`  
		Last Modified: Wed, 05 Oct 2022 14:06:42 GMT  
		Size: 831.4 KB (831396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31110fc43a4ce01227dd0a0453f904b221bd482dc4c0301b8ffa501b18ea30e`  
		Last Modified: Wed, 05 Oct 2022 14:06:40 GMT  
		Size: 4.3 MB (4265721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7365507dba87454ad0733144061a0542a771b554c28c0b8ebec0b48db8f8678c`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13820d6a8f15395e7f0229f1db78a33b5cab7627627dcf05a9f5aa25cc4c88a`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3e83df9803da355f686ea14320ce21fd16f2d1d493aa0c23027119f31892e`  
		Last Modified: Wed, 05 Oct 2022 14:07:15 GMT  
		Size: 252.5 MB (252503449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13927152bbda1f9e5e4da3f8f076eeb25177cb22e6347a12dbb859a375a5dfaa`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb232301a9cb5bd90e93d2d742551234aab484877099d191004e68fd52c2939`  
		Last Modified: Wed, 05 Oct 2022 14:07:35 GMT  
		Size: 63.1 MB (63088887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e697dcc64c80657eb9b8cd7f3245242a6c1aa2c256512e00dc7a0b01c50e004`  
		Last Modified: Wed, 05 Oct 2022 14:07:26 GMT  
		Size: 287.6 KB (287598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0588145aba131c45bb37457b2bce2eb15ff97b20dc08c8706f0073a5940b0a37`  
		Last Modified: Wed, 05 Oct 2022 14:07:37 GMT  
		Size: 67.0 MB (66998442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b70eebce05e703acd0e9cd6a52e2061058ce5b16d05bde10bafa746e1109bd5`  
		Last Modified: Wed, 05 Oct 2022 14:07:54 GMT  
		Size: 10.7 MB (10735735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

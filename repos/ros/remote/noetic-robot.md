## `ros:noetic-robot`

```console
$ docker pull ros@sha256:dec52d670aead774ba5906310da12fd28a68080c44578e6062762b7ce7cb76ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:f2cb64c09356a71a17270f40ae8e9d42d242509547d47b395d46e04fbfaa5c93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359041151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aae48c851939de656e19f202234d0491e2bf82aa82870ab8070c404b34a0bda`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:10:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a67e64bc6cfc11803ed4fdb948911a3d1d22b6f40e7ed61cd815d62c050a4fc`  
		Last Modified: Tue, 25 Oct 2022 07:54:17 GMT  
		Size: 15.9 MB (15861161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:3f776a6cc9ad8ec3c64b0118d5d2b8918e544fbf1b757849998c2abfd5fd2a2a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303318474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe35d649eccf626ca98db067e0a14b9e1db741b83c309d322c069d6ea628019`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:07:00 GMT
ADD file:0e30b9fd980776c745b113ac234367069202f461c4d888acb3225ccc0aa75385 in / 
# Tue, 25 Oct 2022 03:07:02 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:09:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:10:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:10:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Nov 2022 19:10:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Nov 2022 19:10:12 GMT
ENV LANG=C.UTF-8
# Wed, 02 Nov 2022 19:10:12 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Nov 2022 19:10:12 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Nov 2022 19:13:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:13:08 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 02 Nov 2022 19:13:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Nov 2022 19:13:08 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:13:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:14:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Nov 2022 19:15:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:16:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88411d40226eb74e038e5d2cbedefbd7555c34298ed687d1073cf87740fab694`  
		Last Modified: Tue, 25 Oct 2022 03:09:28 GMT  
		Size: 24.6 MB (24588786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4980d48be3296f50c2eb7a1ed914910fd03228f6827e76761e4f91e855c274`  
		Last Modified: Wed, 02 Nov 2022 19:28:01 GMT  
		Size: 1.2 MB (1162277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46df80e53990143d250cd2cfc257128e21ad7900fea8655f90dc73db497ee70d`  
		Last Modified: Wed, 02 Nov 2022 19:27:59 GMT  
		Size: 4.7 MB (4678939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5c8d46e4b38edb3ed3b546e70c15759ea848a90835313ff76420f5f6236f4d`  
		Last Modified: Wed, 02 Nov 2022 19:27:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a631c1eea769a3bb413e8b9acee2ba43d03ca28ba9f352402a1f438929797bf8`  
		Last Modified: Wed, 02 Nov 2022 19:27:58 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0f2b9e1046c08b089ef7de2e729e4fe4a931f878eb337e38e38b21f05d7466`  
		Last Modified: Wed, 02 Nov 2022 19:28:32 GMT  
		Size: 157.5 MB (157499042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723fb85ab5877cb1c8a4c5404244e3ae35339f14585e9fc0cf6ea7edbd98e744`  
		Last Modified: Wed, 02 Nov 2022 19:27:58 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d36e628b562012ce5558f6c1874f3d6cd0986636f5fed29a2a12443ff5843e`  
		Last Modified: Wed, 02 Nov 2022 19:28:51 GMT  
		Size: 40.5 MB (40506752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bb6ea983ee09f27ab55355b62ddd57de03cc019997304ca3c7557a61368083`  
		Last Modified: Wed, 02 Nov 2022 19:28:45 GMT  
		Size: 332.8 KB (332813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f5efd84d9c10fd339e85aeef8d785c40cc233d921959b11cd7b991b49b6e3c`  
		Last Modified: Wed, 02 Nov 2022 19:28:56 GMT  
		Size: 60.5 MB (60481135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb0840c62f958906360caf24fcd6f69712d87d2c678c220aedb409e746faa24`  
		Last Modified: Wed, 02 Nov 2022 19:29:15 GMT  
		Size: 14.1 MB (14066319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:35c0807c3a9674796b7ff7b819fbd159fc13f69dc3034a817a170c98c29ebee6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338307578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb6fdbc1a68f4521e7fb3e4b2a4c8d83f26b47cd5b4233095f12c3dd95ec6a1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:11:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:14:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:14:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:14:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:14:39 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:15:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:15:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:17:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:17:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7354b266abeda9b5bfbca97ad1c6887d2a277d69ff8c607591a279459548ac7`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614279c49f19055c903676e10afd41c8a3cd40f35d8b708fb499f7b5eeb965f`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c1b3c16d04da075eb127cecb646f3fbb43b07575ac781c7f670ca3f1885796`  
		Last Modified: Tue, 25 Oct 2022 22:01:55 GMT  
		Size: 171.4 MB (171447425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac303ffe5e80a8c48e68fb479034e19261f5b6990dd5100bc6ddb1c7cd38ff`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4148c35466d56fca5bdd1144c7cc49f7c57ff22d51ce5c197995f215040f68d6`  
		Last Modified: Tue, 25 Oct 2022 22:02:11 GMT  
		Size: 45.2 MB (45204375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b385026becc2dcce049f0ab39c7d58c6459f28965efe78e7ee77336f82328a45`  
		Last Modified: Tue, 25 Oct 2022 22:02:05 GMT  
		Size: 332.1 KB (332102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d152eaa0a13418a883f576ea85d8893f1cdcafe87fc965ff14ee47fd4e076e7`  
		Last Modified: Tue, 25 Oct 2022 22:02:14 GMT  
		Size: 72.0 MB (71974237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1ae12efe38c9f33d969d096b063141edbfda6df668fbb72467712d72e825b5`  
		Last Modified: Tue, 25 Oct 2022 22:02:29 GMT  
		Size: 15.5 MB (15453818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

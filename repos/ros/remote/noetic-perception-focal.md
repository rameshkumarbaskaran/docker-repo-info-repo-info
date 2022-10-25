## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:c53667dc915e56abe3ef22f5db7b5adfaf30e3cc966bbeb1713cb54457a3e771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:cbbb6aa7e54b07b867ea1c6fefab9c1bd83f795f6e3a30a499c0a1f595db15c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.1 MB (835147503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d806f6ce0fd63436af5228a1d9a4209bb5f7f8de53205864e5319df8784e227`
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
# Tue, 25 Oct 2022 07:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:96304f40d98ec3ee8f481818e18af495a0d8da05d780423f6da8294be3c5fcc1`  
		Last Modified: Tue, 25 Oct 2022 07:55:56 GMT  
		Size: 492.0 MB (491967513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:d3a05ef88d081e15785fcfe16ff2c65f1202d8e5ec15369b110b406ff066c6bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726177866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2302d2ee97aca1cc80e68f815cc9e06f1b146c7567089608a5feb883d948ea4a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:57:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed30924832b5259516fe54fa5708a8ae36898b16de1c94f0898baa3d5d3b84a`  
		Last Modified: Thu, 06 Oct 2022 07:03:20 GMT  
		Size: 436.9 MB (436879892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c9ad66b6b36c2b6ca4ecc31c4f8f1f19bccceb47cf271dd5441c9dbac84ee8ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.8 MB (784795707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d38a613da5f472621d5e0844eafee839f3f0dd60170e73750a822cba8e910cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:36:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:36:52 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:36:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:36:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:37:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:37:54 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:37:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:37:57 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:38:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:38:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:38:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:42:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f0727eb08e94e95fafae4d8d0079ee1413dc8ff544022ff06d844f4a53bf3c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf931507240c54649243355c092bd81e83eae6916ab26a7620f410132c2d47c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991837517e4c0d5001d2caa2a90cf5e70018524cf2ad724b9cf736dc76eb1d05`  
		Last Modified: Wed, 05 Oct 2022 14:09:29 GMT  
		Size: 171.5 MB (171504736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d4fe51a6dd429e99d46144fc5ddd118e6c466b37ffb21e3942c6fb1bcb67ac`  
		Last Modified: Wed, 05 Oct 2022 14:08:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a814635c2ec9fc6aa1c79542be862549465c5ec04cef8ec399952b79e14fe736`  
		Last Modified: Wed, 05 Oct 2022 14:09:46 GMT  
		Size: 45.0 MB (44987961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f762c4f58b5522b0b2e4a82a4b02573353cdb815242b32b47ea696270c4f74f0`  
		Last Modified: Wed, 05 Oct 2022 14:09:40 GMT  
		Size: 329.8 KB (329844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7389f48d507d2a20ca2a184d421e98d9717ff8bd42ce2a9e76b6b153dfc2ee27`  
		Last Modified: Wed, 05 Oct 2022 14:09:50 GMT  
		Size: 71.8 MB (71753417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74469c08d264edcc5ee135c5451f9ae9f9636a408d721ae64bb3afcbf69ee13b`  
		Last Modified: Wed, 05 Oct 2022 14:11:25 GMT  
		Size: 462.5 MB (462539292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

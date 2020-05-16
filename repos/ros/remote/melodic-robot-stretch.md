## `ros:melodic-robot-stretch`

```console
$ docker pull ros@sha256:e8006d69b1711a994da2291e46651e6c9b9fcc2e9ab604f8c6daa65993d57594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-robot-stretch` - linux; amd64

```console
$ docker pull ros@sha256:b1704c8ca03d4e703213ace2713c3297f453c5ea1febb468ed971cf801837406
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.1 MB (522113757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b16dd60fbb6e92942d9d16dd706b4ea44ced173b33ed04bf9b8aac10d4d68be`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 06:33:25 GMT
ADD file:13031623172f5c5857e27de93553adedf17d955fa370882f850bb6ed6fb8cee7 in / 
# Fri, 15 May 2020 06:33:25 GMT
CMD ["bash"]
# Sat, 16 May 2020 03:59:11 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 03:59:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 May 2020 03:59:18 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 16 May 2020 04:00:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 04:00:07 GMT
ENV LANG=C.UTF-8
# Sat, 16 May 2020 04:00:07 GMT
ENV LC_ALL=C.UTF-8
# Sat, 16 May 2020 04:00:08 GMT
ENV ROS_DISTRO=melodic
# Sat, 16 May 2020 04:00:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 16 May 2020 04:01:52 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 04:01:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 16 May 2020 04:01:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 16 May 2020 04:01:54 GMT
CMD ["bash"]
# Sat, 16 May 2020 04:02:57 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 04:03:23 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c6172af85ee14a8db5a3a51d406b768dfa94d196c06d0d06d591507cf8199f0`  
		Last Modified: Fri, 15 May 2020 06:40:31 GMT  
		Size: 45.4 MB (45375207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fda4a46c1d10f88aabb05da22ec1b0b29e36528fa63d6ad5d315eef32b04d0`  
		Last Modified: Sat, 16 May 2020 04:06:33 GMT  
		Size: 10.5 MB (10476838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74529292be06ac11f652a0185d3b8a8e7c8e6318f78145c9fc6a1f62ab665d83`  
		Last Modified: Sat, 16 May 2020 04:06:32 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9068d1ad5bb66c7ce4974550fa3d9bd1a50ddd06b3aff537cf8ac34edf7dbc7b`  
		Last Modified: Sat, 16 May 2020 04:06:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a7091997ccf0c3afb96ac38925f448e86129e61725cd384d216b8db2da380`  
		Last Modified: Sat, 16 May 2020 04:06:47 GMT  
		Size: 64.8 MB (64797298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3728aa494cb44476d46affef19ab460b7bc376333944a5db9eee751da17d8981`  
		Last Modified: Sat, 16 May 2020 04:06:30 GMT  
		Size: 247.7 KB (247672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3892457fe31ca1f052dc113ae893fb097c7f869363701bc2762a648f9547db9e`  
		Last Modified: Sat, 16 May 2020 04:07:20 GMT  
		Size: 276.2 MB (276209403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39976de06deee43924e049833042e4781f041b7fbf3f42687e6e26ae32a2e98d`  
		Last Modified: Sat, 16 May 2020 04:06:29 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec696c745f89d6b37ff9dec480e2f40cf8471a1cbcc62e5cf79f607183ddd46`  
		Last Modified: Sat, 16 May 2020 04:07:44 GMT  
		Size: 108.5 MB (108477140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0994586a749a4364a66789c73d9fb05ab961f42f5daacf5f16180ecc7a756740`  
		Last Modified: Sat, 16 May 2020 04:07:50 GMT  
		Size: 16.5 MB (16528376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f2c96cf75b7d5b4724b273239ef66a8b36c9df49a7da4021db4a5a9c44c8f8be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.7 MB (464718138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f676e65839210a7ee1222e2253d6fb5e3b9ca5b6da1eb9de1456c60ad16a8b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 12:48:07 GMT
ADD file:251053dbd1ce0b3744de3eecf53a3ef8ccf92ea509678e59800952c3dbd1b32c in / 
# Fri, 15 May 2020 12:48:09 GMT
CMD ["bash"]
# Sat, 16 May 2020 09:08:28 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 09:08:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 May 2020 09:08:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 16 May 2020 09:09:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 09:09:45 GMT
ENV LANG=C.UTF-8
# Sat, 16 May 2020 09:09:46 GMT
ENV LC_ALL=C.UTF-8
# Sat, 16 May 2020 09:09:46 GMT
ENV ROS_DISTRO=melodic
# Sat, 16 May 2020 09:09:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 16 May 2020 09:12:45 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 09:12:52 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 16 May 2020 09:12:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 16 May 2020 09:12:53 GMT
CMD ["bash"]
# Sat, 16 May 2020 09:14:15 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 May 2020 09:14:55 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e144e997aec62ed9c3bb1ff83ae2a62cbea252858abfb48ac60bb2078817a6c`  
		Last Modified: Fri, 15 May 2020 12:55:43 GMT  
		Size: 43.2 MB (43163052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adcea988ace3277be71b815d98bafecfbc3b947df828bbd494e7085e5fb1585`  
		Last Modified: Sat, 16 May 2020 09:21:42 GMT  
		Size: 9.8 MB (9775014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feaa5401dfe7ddb95dcb6de0a4eb7283aa6a2def14cf3340f8e7b9b4730148d2`  
		Last Modified: Sat, 16 May 2020 09:21:39 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23dc23b7b13d543ecc54f90d6b010b53fa3db276c2f8c57217adf1d89a97c5e`  
		Last Modified: Sat, 16 May 2020 09:21:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27290dc07596e678a0735240b71e41a14953d50db4af85a8992c5db289dedf7f`  
		Last Modified: Sat, 16 May 2020 09:21:58 GMT  
		Size: 62.1 MB (62097672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a844380c84bf9a25745c28fd3bac50cf3e8215b708559843d527e3402d87f624`  
		Last Modified: Sat, 16 May 2020 09:21:38 GMT  
		Size: 247.7 KB (247737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81ded023357ea030fbb8a3b72370c16c6d6b20e664b1074159b1d0b05f37850`  
		Last Modified: Sat, 16 May 2020 09:22:46 GMT  
		Size: 230.4 MB (230401736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f15673969bdf41754d0b000c9eb2d6a97266d1c63ef171c362c822d9e86b5b`  
		Last Modified: Sat, 16 May 2020 09:21:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bc732aa84f09e693b067588e92f67f2bba46a359f79c293a79acb6cb0c6331`  
		Last Modified: Sat, 16 May 2020 09:23:18 GMT  
		Size: 103.0 MB (102958305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cc0e17e7b4b401e097202ab6b3e58094292346805f92ae85be2ffc44398725`  
		Last Modified: Sat, 16 May 2020 09:23:27 GMT  
		Size: 16.1 MB (16072800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

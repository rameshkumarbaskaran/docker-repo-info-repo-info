## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:d9c650446853b88cad284419263a9d56bc62d3c98dd8e01cdbb848bae8ec9bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:eb9cb9d2843ef50aa96edfc64d29690882633227d956698d9b99643ff211ff89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **951.5 MB (951527328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb871071aeb60fde83497f6af89ca97c419468b44cbdd3bbc6f97b33140c1a98`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:36 GMT
ADD file:2f32dd3ef1e51a4d2d6dcf55fbf766434df5b3ada802b087d5761f2fa0cdebf5 in / 
# Thu, 23 Jun 2022 00:20:36 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 12:48:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 12:48:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 23 Jun 2022 12:48:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 23 Jun 2022 12:48:09 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 12:48:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 Jun 2022 12:48:09 GMT
ENV ROS_DISTRO=noetic
# Thu, 23 Jun 2022 12:49:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:38:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 23:38:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 23:38:10 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 23:38:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:38:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:39:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:41:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea267e4631a981caf2841a7e9a1faf29cef9d020c4378fc64845802d17586531`  
		Last Modified: Thu, 23 Jun 2022 00:25:38 GMT  
		Size: 50.4 MB (50440811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d614310471c61e4200046b8f7adea9e8513871ad4fde9b669e49cafd656bde2`  
		Last Modified: Thu, 23 Jun 2022 12:53:58 GMT  
		Size: 10.9 MB (10892280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c90706f4c8a053c5c76e44d43756ced985189146b36ac63497e25ceceefc5c5`  
		Last Modified: Thu, 23 Jun 2022 12:53:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832307bf10c44d39b4524638f32d96d980cbea1925cc229df4ca7c97c3d08e81`  
		Last Modified: Thu, 23 Jun 2022 12:53:57 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09580d323567b8cc4622a787e2540c618939571a6ba340dd72e42597029cbba5`  
		Last Modified: Thu, 23 Jun 2022 12:54:29 GMT  
		Size: 239.2 MB (239166199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39dada285349dd73a05a5efcc9f7a78ece2b4d3f8af94032d497caeef5a9f16`  
		Last Modified: Tue, 12 Jul 2022 00:04:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4c45b18027d32f13d3a3054125f1bc02100af05c5625dcaffaeb925a75d49d`  
		Last Modified: Tue, 12 Jul 2022 00:05:12 GMT  
		Size: 86.7 MB (86716172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425afd918406f89360e651fe6438c7d56e07c3373139984762889c163123ca25`  
		Last Modified: Tue, 12 Jul 2022 00:04:59 GMT  
		Size: 316.4 KB (316435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04828242e79a3ae204a877e305d8dcdce6cdbd7e2f94d828405673f5c3c860ed`  
		Last Modified: Tue, 12 Jul 2022 00:05:10 GMT  
		Size: 76.0 MB (75977435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267a37db93cbe4ea7c084703d2d858f8589905137999a3aa638cacab21060fc1`  
		Last Modified: Tue, 12 Jul 2022 00:06:45 GMT  
		Size: 488.0 MB (488015586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2e1d939d0d39d36d113dc6065fb0ae71f9207949f46f31e8a87a1cd7c51ea6cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 MB (867664380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7a08645d17a3dda8e51a470fda30f3a96065c29cfdd1bec886137546446cf0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:46 GMT
ADD file:ea39534c5e9a548d7938f6b0e2459383caaf3906f3cc5eafe8bf66053b19f2d5 in / 
# Tue, 12 Jul 2022 00:40:47 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 13:00:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 13:00:48 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 12 Jul 2022 13:00:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 12 Jul 2022 13:00:51 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 13:00:52 GMT
ENV LC_ALL=C.UTF-8
# Tue, 12 Jul 2022 13:00:53 GMT
ENV ROS_DISTRO=noetic
# Tue, 12 Jul 2022 13:02:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 13:02:13 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 12 Jul 2022 13:02:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 12 Jul 2022 13:02:16 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 13:02:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 13:02:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 12 Jul 2022 13:03:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 13:06:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:891a1587d3644a8b4b6dab3726ef380a725a0e19bfbf0eac02a275f711985862`  
		Last Modified: Tue, 12 Jul 2022 00:46:46 GMT  
		Size: 49.2 MB (49228928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9d4034dfbab9d3d5107231bf79f7e9128aa4489cba93d97578d760166fe3e6`  
		Last Modified: Tue, 12 Jul 2022 13:09:17 GMT  
		Size: 10.7 MB (10689263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0120a667e47e68ebbd4a03de6b0932ea25a0078d49f8ee71a75c9ebc31fbeef`  
		Last Modified: Tue, 12 Jul 2022 13:09:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c0820f1a42597e95311859510855953092a4ac35c4d590417693b084968c31`  
		Last Modified: Tue, 12 Jul 2022 13:09:16 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66081e680fda062b62d547ed9e29d0766f71a29d7a5fafb291a118efb1d184b`  
		Last Modified: Tue, 12 Jul 2022 13:09:46 GMT  
		Size: 184.4 MB (184372986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b195084a0c638927568ddb99e45b6b5b0c4d9994a11d7938842a8d3a60a9a1c`  
		Last Modified: Tue, 12 Jul 2022 13:09:16 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3d20692b99e02b1c6458a922737fcdd3c2672cdd5f388abec6574b69ba70a8`  
		Last Modified: Tue, 12 Jul 2022 13:10:06 GMT  
		Size: 84.4 MB (84370574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51c1b09402b429b070ef67b190db669048246a5a35cd21c29746c5765ab8eca`  
		Last Modified: Tue, 12 Jul 2022 13:09:55 GMT  
		Size: 316.4 KB (316388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02cb0af4b91439692d2e60c520d13a9ba0ab45163ac7803dc675c1d54006746`  
		Last Modified: Tue, 12 Jul 2022 13:10:05 GMT  
		Size: 73.9 MB (73865065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2296917a8ccce27517c4119004e34bdbeac749fe6693ee3f50568b941dc30b`  
		Last Modified: Tue, 12 Jul 2022 13:11:31 GMT  
		Size: 464.8 MB (464818808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

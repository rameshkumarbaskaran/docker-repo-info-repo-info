## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:d1a7a206464c1e036697e5efea0b19fe714a59225d13329ed0e97b8b3710237c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:f7ef48f81f85002b43232085036aec373a85ad61598dd54377b6da36001225f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141821695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9711169d734ddeb793a10d6a574a3684c654ac287e0326028f8ab175ff018fd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 03:41:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:41:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:41:43 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Jun 2023 03:41:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 16 Jun 2023 03:41:44 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jun 2023 03:41:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Jun 2023 03:41:45 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Jun 2023 03:43:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:43:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Jun 2023 03:43:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Jun 2023 03:43:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b169f458fb68eaad31436347ddfc7e25dd97c37d8cb63f22e84e7f95d4fa19b`  
		Last Modified: Fri, 16 Jun 2023 04:03:37 GMT  
		Size: 1.2 MB (1212828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bf80c9011de772b9b9ef6bbfe82a4f648cba6a09b044082641c5a232558d5a`  
		Last Modified: Fri, 16 Jun 2023 04:03:35 GMT  
		Size: 3.8 MB (3828743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa9834c66b60b85dc4ddfef495ea84f47531b25092c93ce7cea642ccf57ef2b`  
		Last Modified: Fri, 16 Jun 2023 04:03:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11d2a49f11b048e53a72852bd937876370b9ba2c2448fff57054b14f67466f0`  
		Last Modified: Fri, 16 Jun 2023 04:03:34 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbaaf0d07ce9923344bb5649335dc9cb1d9d75b9072a4184813e3b6e96cb98c`  
		Last Modified: Fri, 16 Jun 2023 04:03:50 GMT  
		Size: 106.3 MB (106346667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40d88d0af61448739222d5fd5bd85608277cce56a574273ff20a89fafee8515`  
		Last Modified: Fri, 16 Jun 2023 04:03:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:268f0f924e3f57a839868e589d0872539266d91048c7eed6f6f17592bf768bb3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137501451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf4c9a915dd9277d29c5bb2fddd8d79eb15e3a6d9a7befef47f3ce5219f4e24`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 14:39:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:39:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:39:32 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 04 Jul 2023 14:39:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 14:39:33 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 14:39:33 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 14:39:33 GMT
ENV ROS_DISTRO=humble
# Tue, 04 Jul 2023 14:41:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:41:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 14:41:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 14:41:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00229127f6e92c07e3d74389e863ed6853d2d18643b36b4305c0618bd0dde009`  
		Last Modified: Tue, 04 Jul 2023 15:02:02 GMT  
		Size: 1.2 MB (1214643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b203d955e7643d1bb7ec9891155ddb1401e9f8ef11e41eff2ea80a7477a1e4a2`  
		Last Modified: Tue, 04 Jul 2023 15:02:00 GMT  
		Size: 3.8 MB (3802027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c278f102957a8f2e4cef72c46fb72240db242ec7800b4e9f3660cdd59adb5d`  
		Last Modified: Tue, 04 Jul 2023 15:01:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b369fa41d7f7a70ee18742f04da6ab36f01e9331cd686a3fc0d10f2a61df1ee`  
		Last Modified: Tue, 04 Jul 2023 15:01:59 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc99b708e63ea51d08155711080144b68401240806daf3d55ff31da8ce2e6e8`  
		Last Modified: Tue, 04 Jul 2023 15:02:14 GMT  
		Size: 104.1 MB (104091352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4587e83797ba402344f156014188711bc267dad06b4fc07b9b76d84206961887`  
		Last Modified: Tue, 04 Jul 2023 15:01:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

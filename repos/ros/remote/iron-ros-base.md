## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:ca1916d2c292d2f57b40573bdb3c9937b8ceb3837f9b2b4d5faceb0e9fdd9b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:61eb3c9f56d43eb810b2d192d604c692a9305f1f71ed56de06fa3fe1d4fbe142
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268906475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e095263ce4cd11daf04a3b7de88bd0d602d325c77a22fd9734ece4ce1e7892`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:29:07 GMT
ENV ROS_DISTRO=iron
# Tue, 03 Oct 2023 06:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:15 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:30:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:30:15 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:30:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:30:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:31:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23a4f8abcdb7d54b1be57c8c5a7b900175491bf0a6c728ec1ff988721eeb650`  
		Last Modified: Tue, 03 Oct 2023 06:39:58 GMT  
		Size: 124.2 MB (124214286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e5bde6e62e3000d8b94ad515014497a6fa4a570dad9498a8ae2f1237452198`  
		Last Modified: Tue, 03 Oct 2023 06:39:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e24fe421e5b439046c262749796b2f9d58ebc40de204cfadb5c956943845717`  
		Last Modified: Tue, 03 Oct 2023 06:40:19 GMT  
		Size: 85.2 MB (85169141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22179de2db23d58e3be85b024d47ba5a2380e9ee2d8da5dc834879354909c521`  
		Last Modified: Tue, 03 Oct 2023 06:40:09 GMT  
		Size: 304.7 KB (304715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74e90661265c45926e24a78f9376fa9773c906d6a6e0858990bab9abc0534c4`  
		Last Modified: Tue, 03 Oct 2023 06:40:08 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6d02fed5e2a9b1964ba837a59e99999255fd8e141dc0a29a079ef8bef0201e`  
		Last Modified: Tue, 03 Oct 2023 06:40:14 GMT  
		Size: 23.7 MB (23730531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5a813a8e3985628fe6982d47598e20dc739668aa3dfc7ba751cf65b0a5de4fd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261352622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63dbcd822b0ded6f61ded207258977796f50e596d7bcad3a7499a441251165a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:50:42 GMT
ENV ROS_DISTRO=iron
# Fri, 13 Oct 2023 04:51:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:31 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:51:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:51:31 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:51:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:52:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:52:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe7e5397da56a4ded96341848bbe099efaf06181bb8a09f3720aeb98cd49c69`  
		Last Modified: Fri, 13 Oct 2023 05:03:18 GMT  
		Size: 121.7 MB (121671888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b628474c464bf47e0464b172ff209e5e12441f2570b8a83504c6ef68bc1f77`  
		Last Modified: Fri, 13 Oct 2023 05:02:55 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82511f0dabbf715d554877bab0fec36b1418a40aa932175ad0816f595105f435`  
		Last Modified: Fri, 13 Oct 2023 05:03:35 GMT  
		Size: 82.8 MB (82845322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a7517588a907a56e240f9131473fa8f9e8f3453f23e00a962242a46ea01bc9`  
		Last Modified: Fri, 13 Oct 2023 05:03:27 GMT  
		Size: 304.9 KB (304924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7110d57994728ed7d08117f21b0158ae78a4cb11c5efb4b68db0626e995e099`  
		Last Modified: Fri, 13 Oct 2023 05:03:27 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e9dc421947da7f84fb4df824e59128c51449f0220cbfa2ee41ee150798241d`  
		Last Modified: Fri, 13 Oct 2023 05:03:31 GMT  
		Size: 23.1 MB (23117319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

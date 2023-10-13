## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:d3ffa0686d76a1846ecf4ed1ecaf3d5ec042cc22ca0a7d621489a02679f30592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:53c74e56feec06d6ce92013a2bba03f5adb30b8b378fa03300f7f3c61a3660b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141905855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e4795326da29494c410c38313f6db9ccb8342b7210bcfa8b2932e7c35246c0`
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
# Tue, 03 Oct 2023 06:09:08 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Oct 2023 06:11:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:11:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:11:49 GMT
CMD ["bash"]
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
	-	`sha256:f63af57a291ea0d8bef7998336bff74edc42cd8c81f6d753a2f5d4f2c809a2b1`  
		Last Modified: Tue, 03 Oct 2023 06:37:27 GMT  
		Size: 106.4 MB (106420533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e044e4a00a19b3e05de479e3a9337d89b05d2bb4bbb253140e06f1354096ac90`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cbc7e852624d2c318fc4a363e4ea2a4f36d20ee00c54dd6728cbf70d6cf729ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137562649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11217ed4a7b2efff89f4f5baaa1d07042502c240978402ce00e384881fcbdea`
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
# Fri, 13 Oct 2023 04:38:07 GMT
ENV ROS_DISTRO=humble
# Fri, 13 Oct 2023 04:39:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:39:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:39:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:39:35 GMT
CMD ["bash"]
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
	-	`sha256:c023537795c860c51cdc51a826448aa3f98423714b84b95dea685761f8e013d6`  
		Last Modified: Fri, 13 Oct 2023 05:00:48 GMT  
		Size: 104.2 MB (104151928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfda3e7987bf657d0a886fc085e34ebecaca449450d6b705392eb5c3170fe318`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

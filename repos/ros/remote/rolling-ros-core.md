## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:1a1da3f393a7e216a6a27b701122d0fc81852467d9515f323077170000434a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:82e943d3795de3208b880176e44ef3c1fe938e2a645cd4324cee9176e37a63ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159674366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1a375fa361d6d2dbb1b8150b27a0610a6a3683ebdc6d364167c63b1671cc34`
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
# Tue, 03 Oct 2023 06:33:13 GMT
ENV ROS_DISTRO=rolling
# Tue, 03 Oct 2023 06:33:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:33:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:34:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:34:00 GMT
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
	-	`sha256:b293927275b81c0d4e6656435654ec293113bba612b31ca59e3aa388e1135f95`  
		Last Modified: Tue, 03 Oct 2023 06:42:33 GMT  
		Size: 124.2 MB (124189046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223180173aa5341b495187f6e300564465cda4640e1b148b6ca8ed0cc899c68e`  
		Last Modified: Tue, 03 Oct 2023 06:42:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ab2505deb5f42c48cb360b80157d2be11857c4382a68dd09bc6939e111899d76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155061635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a97697aa23f24fc57efab234b9550dcd9ba538bf56ab64ed516f8575b6cec8`
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
# Fri, 13 Oct 2023 04:54:13 GMT
ENV ROS_DISTRO=rolling
# Fri, 13 Oct 2023 04:54:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:54:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:54:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:54:53 GMT
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
	-	`sha256:c76919e69d9bf2e3d2ca8ae0d65ff46ad78ea4ad6cb40564909d2ab3ca2cb1dd`  
		Last Modified: Fri, 13 Oct 2023 05:05:47 GMT  
		Size: 121.7 MB (121650914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78ad5922e8a4b2b9b64791f4eb98c6ce309e5d8ff2ff1a652ce79787364cf87`  
		Last Modified: Fri, 13 Oct 2023 05:05:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

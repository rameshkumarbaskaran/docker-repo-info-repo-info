## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:664420f4b16c030307935c36bc23ff18d0b0bce7d391ebec298ff3819bf05d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:d6f26345b7c67531b3db01c3179b4a3c8a3c88f88e3955902506a6a19907d001
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155735340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49a55ecc793bce5191924818e0c663a7c313154699b61cca4030ed47a947dd1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:57 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:58 GMT
ADD file:655d373cb551d0dd5d7867f88a4f98908dc3f16190986f693e88c423e6f21b8d in / 
# Mon, 05 Jun 2023 17:08:58 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:26:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:30:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:38:43 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Jun 2023 03:38:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 16 Jun 2023 03:38:44 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jun 2023 03:38:44 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Jun 2023 03:38:44 GMT
ENV ROS_DISTRO=foxy
# Fri, 16 Jun 2023 03:39:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:39:44 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Jun 2023 03:39:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Jun 2023 03:39:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f0412dfb1aaea4892c13dab6f771bcd79641a4bdcb521ce881f5dcfc0df9a7a5`  
		Last Modified: Tue, 06 Jun 2023 09:20:27 GMT  
		Size: 28.6 MB (28580519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733ac94a680e3659eb88af9a60aa46eabe11de358d05cb19cf9d535083358650`  
		Last Modified: Fri, 16 Jun 2023 02:35:08 GMT  
		Size: 1.2 MB (1198722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c1fc3d4979a8cbea7949ab14296db71b51de166f987d5b8427b73ada3f02c0`  
		Last Modified: Fri, 16 Jun 2023 03:59:52 GMT  
		Size: 5.6 MB (5553799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3eff5a20cb49beeb08300ad92aa92769ff55b41f28ffa912b7629fc9508a40`  
		Last Modified: Fri, 16 Jun 2023 04:02:22 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654c3018234b0bd67a2e90bcf0f12b25a7181a9e32ea10b02709553e0adbb4b0`  
		Last Modified: Fri, 16 Jun 2023 04:02:22 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bcc91e8004fdeae5d2bab3940341e63b96c2766ef5f2f45d6a7b5ffe821366`  
		Last Modified: Fri, 16 Jun 2023 04:02:40 GMT  
		Size: 120.4 MB (120399883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744aeb09540670851e8f96bcacb101e8090a2534fbd1bb18eb684a89d58fc91d`  
		Last Modified: Fri, 16 Jun 2023 04:02:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c7cb2c154a42cb579603e09a71ae9b4105ce19045e189731601a535a8a5c0d65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138547424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4727f94550c533146adb474bb9017a768426c4ad68619929891cdbae657e2ba1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:07:59 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:07:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:02 GMT
ADD file:6c0661b94e27ede70ca2a8842bdab5bc26b9ae4760b17870eda9d595672795ff in / 
# Mon, 05 Jun 2023 17:08:02 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:04:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:05:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:19:22 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Jun 2023 01:19:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 16 Jun 2023 01:19:23 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jun 2023 01:19:24 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Jun 2023 01:19:24 GMT
ENV ROS_DISTRO=foxy
# Fri, 16 Jun 2023 01:20:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:20:17 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Jun 2023 01:20:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Jun 2023 01:20:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:29c851dfb906fc3c51d9a9d53a0cfa8ea88e10040baaf47155e04bf87ce3f3a5`  
		Last Modified: Fri, 09 Jun 2023 02:40:24 GMT  
		Size: 27.2 MB (27200436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8ce101c5379362c5d849146976146cdb15940589c3378f71530e726706b160`  
		Last Modified: Fri, 16 Jun 2023 01:43:18 GMT  
		Size: 1.2 MB (1199977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde7326ceba9de7061d919892605fd699e778fbaf87d16a5e3c3506e23a475fa`  
		Last Modified: Fri, 16 Jun 2023 01:43:16 GMT  
		Size: 5.5 MB (5533346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff005d43de0495d08ba8fab702b5a0b2a17e5fda87b3b29b8b6c2aa466af36e6`  
		Last Modified: Fri, 16 Jun 2023 01:45:39 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e623381dd590f881b6d778aae3d52a60123d53a9d321c5e4806f0d9b3a4ef39`  
		Last Modified: Fri, 16 Jun 2023 01:45:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28553edd6cdcf5cf14ecbcdcf441c24b01fee7ddb5cb43531838155aab41dccc`  
		Last Modified: Fri, 16 Jun 2023 01:46:01 GMT  
		Size: 104.6 MB (104611250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74fe9fb151c0863ea44c9c53bb94ecc0123ba796a5ee8bc7184f6a972941641`  
		Last Modified: Fri, 16 Jun 2023 01:45:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

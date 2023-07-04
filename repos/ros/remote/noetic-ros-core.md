## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:c758a55dc996bb123d3760747ed9ae4fd486a358a1d47fb3c7403d7d61326a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:37084b9972c0fd2ef118eec80c749551cfad67ca88c8de4a900e5bdf749b5f68
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212381108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06cdf08f23aa4d698b7d5377017f796cdcb9c701b8e7e5e8d3a6953bb4924b09`
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
# Fri, 16 Jun 2023 03:30:04 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 16 Jun 2023 03:30:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 16 Jun 2023 03:30:05 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jun 2023 03:30:05 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Jun 2023 03:30:05 GMT
ENV ROS_DISTRO=noetic
# Fri, 16 Jun 2023 03:31:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:31:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 16 Jun 2023 03:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Jun 2023 03:31:29 GMT
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
	-	`sha256:e0c84d683cefaf172b68dda67c6436651b8b1563cbf6581f6d107056879bd8dd`  
		Last Modified: Fri, 16 Jun 2023 03:59:51 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7b26995f6b2a9cf9efe6abea26c654753ad281e510d846acd0a50df8ecc32`  
		Last Modified: Fri, 16 Jun 2023 03:59:51 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f480dd10200e3a3923db8466a2f0ace22c6a438b1fcce66e58aff7277e61ab`  
		Last Modified: Fri, 16 Jun 2023 04:00:18 GMT  
		Size: 177.0 MB (177045651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4245827a1732fa0f267df2f15bcade007d9f966ca6b66aff8674eb1f2c65ff8d`  
		Last Modified: Fri, 16 Jun 2023 03:59:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:fedd732d5c2543cd83cca86cdc9c4d5c5ed67e3b35a5e30feb6ee17f52acd53c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188013798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19ebdc1715edcc59196c6c3efbaf12c01535fffb2e80808368c76f8898cea37`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:19:26 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:19:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:19:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:19:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:19:31 GMT
ADD file:114d6f55f8c1c4ec7f7d2ba3c803116a188eece1d1b6dbb3bb40c11082194234 in / 
# Mon, 05 Jun 2023 17:19:31 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:09:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 16 Jun 2023 01:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 16 Jun 2023 01:09:08 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jun 2023 01:09:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Jun 2023 01:09:08 GMT
ENV ROS_DISTRO=noetic
# Fri, 16 Jun 2023 01:11:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:11:22 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 16 Jun 2023 01:11:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Jun 2023 01:11:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2d97abfcf215d35e8a846b390350fea9f455676b41221360fe8782163a1c46bb`  
		Last Modified: Thu, 15 Jun 2023 03:47:54 GMT  
		Size: 24.6 MB (24589116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067db60a914b1db17390d08b8bd7e865dee500a51f35b6cc416f2f439f353955`  
		Last Modified: Fri, 16 Jun 2023 01:22:14 GMT  
		Size: 1.2 MB (1198730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0881c824748bc118255bd7e676957b191f4d1fc5d9312139c1c52620c3cd2e`  
		Last Modified: Fri, 16 Jun 2023 01:22:12 GMT  
		Size: 4.7 MB (4679255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897d12de37bd26c3e5b7c318c866dbb1b2da51ef7fcaf919748173b86af8be76`  
		Last Modified: Fri, 16 Jun 2023 01:22:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca60445b0a24d3a271c0344aada562719e7fb4093cd08e1c827d0f3cbe06c14a`  
		Last Modified: Fri, 16 Jun 2023 01:22:11 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fd28f326a43c2f4336c4d7942bad0b2e7c7c66948c45b89e2c444d11da9334`  
		Last Modified: Fri, 16 Jun 2023 01:22:40 GMT  
		Size: 157.5 MB (157544285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054ab69607baa56a10b8698b59afe82be893274534a3bfca0e72b462dc40e149`  
		Last Modified: Fri, 16 Jun 2023 01:22:11 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7ff2832f5f3e621f73dbcd5a6e456fff5357b32bf2fd4b34b4e787a916a64699
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205444512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bbc889db53a10a59ced385cf734a2ce98caaddc375c3a77706af3c76283cf8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 14:25:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:25:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:25:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 14:25:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 14:25:42 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 14:25:42 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 14:25:42 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 14:28:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:28:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 14:28:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 14:28:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28cdd39b6ea2b9a0ce173cf2e1f26322497d5a9c7710030e37439ad5d4b2523`  
		Last Modified: Tue, 04 Jul 2023 14:59:38 GMT  
		Size: 1.2 MB (1199222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb204de59b70d94654e7760fc586c55bcd195218315dbf7589d66289510f275`  
		Last Modified: Tue, 04 Jul 2023 14:59:36 GMT  
		Size: 5.5 MB (5532648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b74969841e6f58cb9e0f0a3c29463b5877ac9e57c3ce30bfcf3c1a6f5d74b6e`  
		Last Modified: Tue, 04 Jul 2023 14:59:35 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed7a86bfb6803f03f9f877eab39ae2496795feb327436a44d9450ce2781b071`  
		Last Modified: Tue, 04 Jul 2023 14:59:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d91c98424c5722a91cb12e54ca5c7af9f12c034b801df540e013a52df8e938`  
		Last Modified: Tue, 04 Jul 2023 15:00:09 GMT  
		Size: 171.5 MB (171511899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493841186da8cc28dcd3542f3c5e48f6853b465d5389b8a2e595292fe4acfa57`  
		Last Modified: Tue, 04 Jul 2023 14:59:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

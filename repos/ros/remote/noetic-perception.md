## `ros:noetic-perception`

```console
$ docker pull ros@sha256:f26739ec9d163557c72e3561d5f7b21c6baa36650e29a0e630fc54c552029285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:6fe3eeb0a6c79f2c9fed542d0949d758f5023d19f2b21e4cbf19429045e0bb70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.5 MB (835546300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a04683087cbd99125d821c04802461d90d0820274819cb79387718ae4969be`
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
# Fri, 16 Jun 2023 03:31:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:31:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Jun 2023 03:32:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:38:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:eb4b92cb1be2be4c3303b48ae3153b399a674ba5205267a8f230094b09f4ead9`  
		Last Modified: Fri, 16 Jun 2023 04:00:35 GMT  
		Size: 50.9 MB (50939959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85074d427c0ad42d999081cdae5264fcbc3612d8f6f050416f85fe68af3ff5aa`  
		Last Modified: Fri, 16 Jun 2023 04:00:28 GMT  
		Size: 300.9 KB (300905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f55740d8cb9ba6388e9f43d993eb6efead35161d874bfdc0fab522b741534dc`  
		Last Modified: Fri, 16 Jun 2023 04:00:39 GMT  
		Size: 79.6 MB (79605074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acc02334f74bcb721a785ee4b4876c2179768930144af5368ca9ae294e1ae6b`  
		Last Modified: Fri, 16 Jun 2023 04:02:09 GMT  
		Size: 492.3 MB (492319254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:550b08de7d4654499a028a0c76e0f617b0924843176f9bd78deb83f943efdb19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.5 MB (726511769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21ccaa1a6f6253d41e5a3a1d3cda0c100fd9c1aa95187718b464b7c78664716`
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
# Fri, 16 Jun 2023 01:11:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:11:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Jun 2023 01:13:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:21:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c737eaceaa561ec3829766a4f983d37b1a8025bb5a684dbc6943a7bbb893cf92`  
		Last Modified: Fri, 16 Jun 2023 01:22:55 GMT  
		Size: 40.5 MB (40503879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca81c90a8a3c1dd33072bbaaad0ec5513a44ec458e3c6cdeb7f56a9db0d526ad`  
		Last Modified: Fri, 16 Jun 2023 01:22:50 GMT  
		Size: 300.9 KB (300910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634e8abbac2de0a96b0e64208fce0b241335c3727fae9cd287fd4703feee414a`  
		Last Modified: Fri, 16 Jun 2023 01:22:59 GMT  
		Size: 60.5 MB (60493810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf34daf709d5030ce3ecce404fb19c763e8035e85a55252f3d1899e0da1718c5`  
		Last Modified: Fri, 16 Jun 2023 01:24:21 GMT  
		Size: 437.2 MB (437199372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1d0487cdc96ec575cc7508097c8d8e1b0b0fc14d70e3478e43d04d0c4ef88130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.8 MB (785846180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff2ba19a83eca63cca34a699af128f82405633e67c43dfc99c5ed633ecc329f`
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
# Fri, 16 Jun 2023 01:05:24 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 16 Jun 2023 01:05:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 16 Jun 2023 01:05:25 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jun 2023 01:05:25 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Jun 2023 01:05:25 GMT
ENV ROS_DISTRO=noetic
# Fri, 16 Jun 2023 01:08:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:08:23 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 16 Jun 2023 01:08:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Jun 2023 01:08:23 GMT
CMD ["bash"]
# Fri, 16 Jun 2023 01:09:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:09:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Jun 2023 01:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:19:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:8660fa6a9889b47b0cdedcd38551c4c097b74330bc7a35fd279ee17d32d7d67e`  
		Last Modified: Fri, 16 Jun 2023 01:43:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5097712cf91a87b7360886785f2a964a56ce10c8e4f3a77000f83523967fa20a`  
		Last Modified: Fri, 16 Jun 2023 01:43:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ff70657adfd24e02a562b4b09fdd26c26299a6001899ed61f0a8d56fb4e6f7`  
		Last Modified: Fri, 16 Jun 2023 01:43:49 GMT  
		Size: 171.5 MB (171538574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a43a9a62bd1e51770b576e70e4a54589303e48ac0c92cd9b8e010d58561397`  
		Last Modified: Fri, 16 Jun 2023 01:43:16 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b2416bfb26d974c3da81f7eee6b7acfdb4eccae5aa2c72651e419946abed85`  
		Last Modified: Fri, 16 Jun 2023 01:44:03 GMT  
		Size: 45.2 MB (45205161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1bfa67a8583b7c003a10dc5da1e0a39d70b559bb0ef4854efb785d8a227d1e`  
		Last Modified: Fri, 16 Jun 2023 01:43:58 GMT  
		Size: 300.9 KB (300915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4152459f508eaf13deb06ac7708780ad620739b8cd3b7719a65bc728be19dd88`  
		Last Modified: Fri, 16 Jun 2023 01:44:06 GMT  
		Size: 72.0 MB (71971225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e30f904686801514f906f4b10630900fa5c7551ceb8e71256813143c09bdc64`  
		Last Modified: Fri, 16 Jun 2023 01:45:29 GMT  
		Size: 462.9 MB (462894133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:b46e25218684dde0f8fdc4ee64e95d5b48742d5a9b75032881e93e8c80565384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:e494f7045c604c02e24951e5fadac6970192d9750e74fed4dce6a84553a1bbe1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343227046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176ab51cd7218002277e110aa91f9a6ba9e07ea86a8b687079ecd5407dbe1ee4`
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

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:00362f93138beaccc2f24ca7603855ad9e5c4c1d0fb3276731ec5cd2c9e1a194
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289312397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb397f715f738fabd09fe73d93f3af1988aebe53ecd1c2e419665dd65abef97`
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

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9f131f36e81dbf42293146b1fa7d86be2ee41013c608e68efa1d355d1fc805f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322922029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f675169c509f89573c15272afd2e0826150be2d161f7dd7286baeab5042ef6`
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
# Tue, 04 Jul 2023 14:29:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:29:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 14:30:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:656ccdb00e6c88095176998c459e8fbff2585a38ed2a7781a7812e457b3abe9a`  
		Last Modified: Tue, 04 Jul 2023 15:00:26 GMT  
		Size: 45.2 MB (45204441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cbde3a0d7e6e385474cc8f84e37c7ddb2ac72700849e7e7a586690a0a29efb`  
		Last Modified: Tue, 04 Jul 2023 15:00:21 GMT  
		Size: 302.7 KB (302677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a52ffd06935d7fffa1923572f179f9d9aa8e0661022b715746f72ad0673679`  
		Last Modified: Tue, 04 Jul 2023 15:00:30 GMT  
		Size: 72.0 MB (71970399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

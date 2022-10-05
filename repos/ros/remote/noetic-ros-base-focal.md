## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:f6f8c1eb2cb8737226e3d9988ce935bcd7a73e8030a2352116e5b92d59da3246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:2bb6821186d86445b5f0b2da7a4ccc36dbc26707ae18b8c8b52184baf0c5fd11
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343232868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ce7cd5edc8f30ba6d15bc589632b6987b60d34f90dc2c31d103b0e700ac8eb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 10:02:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:02:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:02:51 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 10:02:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 10:02:52 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 10:02:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 10:02:52 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 10:05:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:05:28 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 10:05:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 10:05:29 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 10:06:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:06:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 10:07:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db398de1191a2231a78b6d5d54baa0f980aa763df67adb3394a7269111109671`  
		Last Modified: Wed, 05 Oct 2022 10:50:03 GMT  
		Size: 1.2 MB (1163849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d2c75c8d50e5aa3470df0fc55d0148e41867398126d721472b626f05229661`  
		Last Modified: Wed, 05 Oct 2022 10:50:01 GMT  
		Size: 5.5 MB (5546788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b903c62e1337e2dd7c72c1e20fc53356cb226565140bd53279940a0824dfd9fe`  
		Last Modified: Wed, 05 Oct 2022 10:50:00 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd68edbd1d0652c7c600df686df53d5de7acd8204dfdaa0021473d00b987edf1`  
		Last Modified: Wed, 05 Oct 2022 10:50:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009d57e521255204934b128030a0d4d356e8969e88e5db0e946889bffaae21ee`  
		Last Modified: Wed, 05 Oct 2022 10:50:30 GMT  
		Size: 177.1 MB (177071749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6428d2dd8bfe4fac9ded18b38507319ecee51621fdf191793d6687512c69d86`  
		Last Modified: Wed, 05 Oct 2022 10:50:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955c711ad2d8e864145c52c8810c7eaacae497a7a0eb81da4ede8668228e1674`  
		Last Modified: Wed, 05 Oct 2022 10:50:48 GMT  
		Size: 50.9 MB (50940474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738a6fe92784306c9f1453b6a855ad51a4ec6eed4ac1c90ea59048368531974f`  
		Last Modified: Wed, 05 Oct 2022 10:50:40 GMT  
		Size: 329.9 KB (329911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f45a8a3d4e2bf3f49eace9665b5b4fcb4dcf67a51bdfabd6a30c6a1e58420b9`  
		Last Modified: Wed, 05 Oct 2022 10:50:52 GMT  
		Size: 79.6 MB (79603231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:81555e4da758c7d82987d180eb4d2cdb21cd374c4fe586252027b54ffac71111
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289217405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2c752dd49937eaa632267c050cb24623692694032757dd8c745123ab3e4e3a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 06:08:22 GMT
ADD file:685f4b5f8c1f11b6389e9f929909e1a667abf29814a7ccfb859aae287dacd7e1 in / 
# Fri, 02 Sep 2022 06:08:22 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 10:18:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:18:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:18:18 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 10:18:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 10:18:20 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 10:18:20 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 10:18:20 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Sep 2022 10:19:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:19:19 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 10:19:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 10:19:19 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 10:19:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:19:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 10:20:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eff72fca8e1d166ddfda6ac6c409e888c95950da6c47d360a088219c0ad7ba05`  
		Last Modified: Fri, 02 Sep 2022 06:10:16 GMT  
		Size: 24.6 MB (24588743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2728e151d700852a4e3785ed979fbca05aebfa838997bbfb6208dac2baf0be`  
		Last Modified: Fri, 02 Sep 2022 10:26:41 GMT  
		Size: 1.2 MB (1164705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ea485604404c82ae7a2f2b9727554ea35d445dd4cbeeaccef029347c75a31a`  
		Last Modified: Fri, 02 Sep 2022 10:26:39 GMT  
		Size: 4.7 MB (4676623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eba218441b7bd8233673d1400fb8680f70b7ea7b544413e35a9b77721eaced8`  
		Last Modified: Fri, 02 Sep 2022 10:26:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a65ee78d700318acee75a82c045825dbc4fd919af3f26b2d49f42e2b179ed16`  
		Last Modified: Fri, 02 Sep 2022 10:26:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a6d872569136597e54453ae5b3342d12f39ab83c48427772b9955e842e21ef`  
		Last Modified: Fri, 02 Sep 2022 10:27:16 GMT  
		Size: 157.5 MB (157471800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431d2220c1d4633ae54c0ff2313b6c33ac62a1fc987657632054d763e35c2ab`  
		Last Modified: Fri, 02 Sep 2022 10:26:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf70c92a20f52607c496f6d3dd3f9356018df2bbca47784b18fb4d39c72c3d9e`  
		Last Modified: Fri, 02 Sep 2022 10:27:36 GMT  
		Size: 40.5 MB (40506172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e2cd1304a712507b28aa65a90a2070fa7724b97f8094037a9b644f01384761`  
		Last Modified: Fri, 02 Sep 2022 10:27:28 GMT  
		Size: 325.7 KB (325746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233f46cc3767a0e7e87109e7864e973fb75be53a37135001058671518d0670ef`  
		Last Modified: Fri, 02 Sep 2022 10:27:40 GMT  
		Size: 60.5 MB (60481203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:986aa4972599a27a24d5fef240d4bbb3baa85e68212932eed5e984b1f6683628
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322166779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a94e2896051c439f0a9a4bb21c10b79700eb74d879d67d9ca855a477f7f94ca`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 06:04:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:04:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:04:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 06:04:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 06:04:14 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 06:04:15 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 06:04:16 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Sep 2022 06:05:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:05:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 06:05:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 06:05:17 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 06:05:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:05:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 06:06:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6679da592cfdf550fcdc4b85e065118bc5d71a57534760b4abedb490355889fa`  
		Last Modified: Fri, 02 Sep 2022 06:29:12 GMT  
		Size: 1.2 MB (1165138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5eb560b76837a662c9463136466570590371e820399defb1c9bc087709ea18`  
		Last Modified: Fri, 02 Sep 2022 06:29:11 GMT  
		Size: 5.3 MB (5323438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e14c9b385a2e2a1aaf2e3e0e96bb0ab19b0ae4bd1ba4df6e04bd247b310d5c2`  
		Last Modified: Fri, 02 Sep 2022 06:29:10 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb230fc3fead8135d54463448100608dff8db563117ce648ff536d58028e043`  
		Last Modified: Fri, 02 Sep 2022 06:29:10 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a441fbb85ca0fc9351965d962c26631f0c0fdd0a80a5de4349d0a2fe39cdad`  
		Last Modified: Fri, 02 Sep 2022 06:29:39 GMT  
		Size: 171.4 MB (171414641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8cbf101495077c64a07b49123584c92c50e4eedbf37c6fe039a5c96c1a45fa`  
		Last Modified: Fri, 02 Sep 2022 06:29:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351e164058f5f6b26f33ca86e472799ca95df650c8044c529338423424b38ea4`  
		Last Modified: Fri, 02 Sep 2022 06:29:56 GMT  
		Size: 45.0 MB (44988847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fcd9c3e7122e87ef29f417d198e443a1892d621f1fe005f9cbf9072b5d3b9`  
		Last Modified: Fri, 02 Sep 2022 06:29:50 GMT  
		Size: 325.7 KB (325657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65599a689993fa62149f8b2028498730ddd14125298b858124751013f37cdba4`  
		Last Modified: Fri, 02 Sep 2022 06:30:00 GMT  
		Size: 71.8 MB (71754873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

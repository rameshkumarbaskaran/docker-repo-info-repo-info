## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:baa43b9b599444bff925df05e70a49cdb0a17aeaf7f9cfd8e86796ef545f38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:82adffa092e98d53cac94a9ecb55ba7569efc8f0f5d22fa619f93ce70eb50a80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358880748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e0ca8e38ae15069727b4c1507435dfe3fb53c865c6ab323f807fd32afdec7f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:26:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:26:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:26:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 22 Apr 2022 03:28:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:28 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:28:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:28:28 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:28:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:28:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:29:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a113e5bfc6a41a0f6d9401ad372ec451407fd55bff2862a2023976889322604`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c65e0abed62803e4b89b3aa305b9b4f0262f25940675f4b8fa7ad7bb9f01a9`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90362b1253ae0b3ad24a095a66a71c2437d714ea43529f9af6cf1f9ee26e7d6`  
		Last Modified: Fri, 22 Apr 2022 03:50:08 GMT  
		Size: 176.9 MB (176875279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424da76ce8b30c3127dada4dbec6e2374d087e7e2b0951038c14545d05b87cc7`  
		Last Modified: Fri, 22 Apr 2022 03:49:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fb42a12f184b9b6ad2c9b99a06bdfba4eb6b8c9d97cb8eb224a20386496a4a`  
		Last Modified: Fri, 22 Apr 2022 03:50:26 GMT  
		Size: 50.9 MB (50933515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9199749d47db40394c6f583da9bf1786de2f23b56c00534df5ab66d5e7ff7`  
		Last Modified: Fri, 22 Apr 2022 03:50:18 GMT  
		Size: 314.8 KB (314824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647f59c451e50b55164b1df4f395c7658e7583fbee1cb10ac1d0c4231a7abf39`  
		Last Modified: Fri, 22 Apr 2022 03:50:30 GMT  
		Size: 79.6 MB (79602400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f093d22dbe5877606fa8a0bb7ab4ff9f764a797720db05f3891f492ba89135`  
		Last Modified: Fri, 22 Apr 2022 03:50:46 GMT  
		Size: 15.9 MB (15858801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:925e6735d0b0a8bd360ae8b6f9bb3430e72444f8460bc6bd09c456b484b52f57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302722275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd50d304cce6369dd44fe927243dae8e7814cc4f7542f0689e49734ffc263139`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:39:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:39:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:39:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:39:26 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:39:27 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:41:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:41:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:41:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:41:54 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:42:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:42:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:43:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:44:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788bc5672cc0168109c03624bd9c0486dc436058f2ef6bd58aa20183c16330dc`  
		Last Modified: Sat, 30 Apr 2022 00:58:13 GMT  
		Size: 1.2 MB (1182235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f050457c70471d51e645d9056bf76421874818d4dcb3c2d9167cc4c7c59f1`  
		Last Modified: Sat, 30 Apr 2022 00:58:12 GMT  
		Size: 4.7 MB (4676780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf102ed76521e041cbd91514e5b37b5e35694a768c899009f51ba52983b3d4d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b493804b771bd37872f55298ac60b41ddb64199e41c6cbd02a5bd78b13f2e17`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf0953c9382836b5d5e61b0e28e2f23c2431ef644d2ddc2d4a5bffbadff9b15`  
		Last Modified: Sat, 30 Apr 2022 01:00:16 GMT  
		Size: 157.4 MB (157423830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5012cfe0e5842d29eb696b50431a424ba513d5c1554715f456713b05532596d`  
		Last Modified: Sat, 30 Apr 2022 00:58:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faae41d6b1935d771645ed3646ee3838471dd083a2f92d29b121834b2a712fab`  
		Last Modified: Sat, 30 Apr 2022 01:00:51 GMT  
		Size: 40.5 MB (40501299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dea40ff78bf9cdbb2384fb35a4bb7127dac17db236f078dcc3d9de59148a06`  
		Last Modified: Sat, 30 Apr 2022 01:00:28 GMT  
		Size: 315.7 KB (315673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d375b84b753999e87a8ed0b405d15fd34c522a1f831031dad0599a36d2f84491`  
		Last Modified: Sat, 30 Apr 2022 01:01:07 GMT  
		Size: 60.5 MB (60481908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b5b7095191acb5cd8a7361427292819dc1bc964f10e4ebb99aea3a00e113c1`  
		Last Modified: Sat, 30 Apr 2022 01:01:32 GMT  
		Size: 14.1 MB (14064485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7b254652b1ff037527cc04a7dfc60d2ff4f28dfb3fea29a192499a2b48019a17
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337474799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452f9a01749cd1dd57fda1c22ab16becc392c6f85837a65638348968970665f0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:20:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:20:44 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:20:45 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:20:46 GMT
ENV ROS_DISTRO=noetic
# Sat, 30 Apr 2022 00:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:21:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:21:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:21:47 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:22:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:22:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:22:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:23:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1a842c5f450bf757d4efae2d77d0b3637b2f76a02794282656ef03f45e1f1`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e026a627567dcb9c599ab69248d8c084364d4df165bc5257f923c2709f493ab`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a527d513e9f97294799a5126bcf25e7f7b73ff93ceb27622f1b3838d580fcde9`  
		Last Modified: Sat, 30 Apr 2022 00:38:47 GMT  
		Size: 171.3 MB (171293442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc48433487f9d4e46329a07c1247899a65bab17103180e95e2da17c25f686d5`  
		Last Modified: Sat, 30 Apr 2022 00:38:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9776aee7c7d20a2a679ec671b31130800b8048248586171aa655e89df4b91f4a`  
		Last Modified: Sat, 30 Apr 2022 00:39:05 GMT  
		Size: 45.0 MB (44988594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890ccdeaa4aedd37f00917bbddd6365cd5dc7f1746a97c5520462003cccd6b3a`  
		Last Modified: Sat, 30 Apr 2022 00:38:58 GMT  
		Size: 315.6 KB (315611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8b7144add68575402586085ccee53c0002fd54ef7e2813f589098a7cce933e`  
		Last Modified: Sat, 30 Apr 2022 00:39:09 GMT  
		Size: 71.8 MB (71753617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877ece7883f291d281f7de9072fa07427d7bf0ac57e8394bcd57db019004f91e`  
		Last Modified: Sat, 30 Apr 2022 00:39:27 GMT  
		Size: 15.4 MB (15447701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

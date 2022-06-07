## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:9d8b0720dc12e05e2e6cb00193ea05013fcc8bc52a8e11efcd7d726011d8581f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:75b9e694d8bf831ceeeb7f839faef39718b756fe7fd6b147389b423e81e4deff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.0 MB (834975524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6f96daae1d6f221b7a1e3c317e0e1857ae4406c0cd798c7caea98c423afbcf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:10:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:11:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:11:01 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 01:11:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 01:11:03 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 01:11:03 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 01:11:03 GMT
ENV ROS_DISTRO=noetic
# Tue, 07 Jun 2022 01:13:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:13:21 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 07 Jun 2022 01:13:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jun 2022 01:13:21 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:13:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:13:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jun 2022 01:15:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:22:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1e38681d9b6d153af3be7e0550217dc0dfb994512346ebc7d9a7a602651e74`  
		Last Modified: Tue, 07 Jun 2022 01:47:20 GMT  
		Size: 1.2 MB (1181179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a44b59555aadd115e37e45f079fef0ca694c5888fcd16350e10a693138a6db4`  
		Last Modified: Tue, 07 Jun 2022 01:47:19 GMT  
		Size: 5.5 MB (5547097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cefae97638ee7cb88a42485677466aa5587fca9972953eaaea67058f3e6d72b`  
		Last Modified: Tue, 07 Jun 2022 01:47:17 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86209410ac0375ac01df476d1f843d17c9837f6c086953deeaf0c7941bb3c47e`  
		Last Modified: Tue, 07 Jun 2022 01:47:17 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abf3bc6872ece682381026a6f6f11c4d5545ea0332db254fd844cd04ba7ea30`  
		Last Modified: Tue, 07 Jun 2022 01:47:47 GMT  
		Size: 176.9 MB (176860236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d317e6d1d9fe1bfd2c0445d594e8536c4d7e97846da20d59866f3c735294eb`  
		Last Modified: Tue, 07 Jun 2022 01:47:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617909da5816fdd6725712597eee7c8f07b716d1adbd74100e4c2c6d8695e764`  
		Last Modified: Tue, 07 Jun 2022 01:48:05 GMT  
		Size: 50.9 MB (50934172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1d95b4adafcf47d6a3bcba767615da47a945bbee4229e97017601a6aae6487`  
		Last Modified: Tue, 07 Jun 2022 01:47:57 GMT  
		Size: 319.3 KB (319342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65210ff74d033bbbd26bd59530f4a4f3a6ef5932282476aa41b7ec7342ddc592`  
		Last Modified: Tue, 07 Jun 2022 01:48:09 GMT  
		Size: 79.6 MB (79603101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b507c79d7107ec363c6307707669011365415eaf3e2b57e092345795a891073`  
		Last Modified: Tue, 07 Jun 2022 01:49:48 GMT  
		Size: 492.0 MB (491955351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:732a9ce14f825cacefc32886651b9a23180a0f46ef47874a17d32205450628b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.6 MB (725587279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce21f86b3137fa28a954f09289263b797c9a14a186dc78e041997dbdbfbc4e5`
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
# Sat, 30 Apr 2022 00:49:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:b9dc52f71902d762b0a95cfa3c0abfc4606212d101bdb1102c56046907805949`  
		Last Modified: Sat, 30 Apr 2022 01:06:14 GMT  
		Size: 436.9 MB (436929489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:37cba6b7529f06b540518f6797f71750191abcc4d1839510c6b82cf8d9d314b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.5 MB (784517811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081f48272fe65c5d6151746f56f2f4d30a39cbbb9177a73868d875d2ca4e4533`
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
# Sat, 30 Apr 2022 00:25:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:3f15a8b59ed9e76d31ca016fba28201e39c0b6f21f48212025ce82ac5a9162a0`  
		Last Modified: Sat, 30 Apr 2022 00:40:47 GMT  
		Size: 462.5 MB (462490713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

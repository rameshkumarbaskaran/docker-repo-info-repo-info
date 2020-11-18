## `ros:rolling-ros1-bridge-focal`

```console
$ docker pull ros@sha256:5cdacb527e953f681fa4a11052cdf0e3cb4138c19e608d0c68f39de1b84c1b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:68f0c683c9a866c4caa1bf7238d220041afab533b55b07844d3064d5c3f3b0ee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.7 MB (333733820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dc118b59dba3909161df067318659b47e30104ea0f2b21fa6d18a2cdfcf09b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:34:27 GMT
ADD file:da80f59399481ffc32f84353830dcf598f31a97785222e75d643bfb8a9aa14e7 in / 
# Fri, 25 Sep 2020 22:34:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:34:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:34:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:34:30 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 00:13:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:46:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 26 Sep 2020 02:05:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 26 Sep 2020 02:05:51 GMT
ENV LANG=C.UTF-8
# Sat, 26 Sep 2020 02:05:51 GMT
ENV LC_ALL=C.UTF-8
# Sat, 26 Sep 2020 02:08:46 GMT
ENV ROS_DISTRO=rolling
# Sat, 26 Sep 2020 02:09:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.1-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 02:09:33 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 26 Sep 2020 02:09:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 26 Sep 2020 02:09:34 GMT
CMD ["bash"]
# Sat, 26 Sep 2020 02:10:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 02:10:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 26 Sep 2020 02:10:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 26 Sep 2020 02:10:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.1-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 02:10:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 26 Sep 2020 02:10:30 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 26 Sep 2020 02:10:30 GMT
ENV ROS1_DISTRO=noetic
# Sat, 26 Sep 2020 02:10:30 GMT
ENV ROS2_DISTRO=rolling
# Sat, 26 Sep 2020 02:10:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.8-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 02:11:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.9.2-2*     ros-rolling-demo-nodes-cpp=0.10.0-1*     ros-rolling-demo-nodes-py=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 02:11:11 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:d72e567cc804d0b637182ba23f8b9ffe101e753a39bf52cd4db6b89eb089f13b`  
		Last Modified: Fri, 25 Sep 2020 15:20:50 GMT  
		Size: 28.6 MB (28558050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3630e5ff08d73b6ec0e22736a5c8d2d666e7b568c16f6a4ffadf8c21b9b1ad`  
		Last Modified: Fri, 25 Sep 2020 22:36:58 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a83d81d1f4f942d37e1f17195d9c519969ed3040fc3e444740b884e44dec33`  
		Last Modified: Fri, 25 Sep 2020 22:36:58 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac7e7e50c4ec78d366977925188b5bcceefc778ad809bbacacfddc2494cf44d`  
		Last Modified: Sat, 26 Sep 2020 00:33:06 GMT  
		Size: 1.2 MB (1176627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fee3294cf809591a86eaf42ab53997f7449cba60d6811bbd5d634d5bb436241`  
		Last Modified: Sat, 26 Sep 2020 02:17:06 GMT  
		Size: 5.5 MB (5547147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86eb1d49055c694a2de0fb058693277298e8663cce6066ecbf8caddc195623d`  
		Last Modified: Sat, 26 Sep 2020 02:17:05 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a159fff5cd41fcb199ffc6f5d72a234ae211ab84a79244bd1f668555b418a`  
		Last Modified: Sat, 26 Sep 2020 02:23:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d365ace33ceb990381865fd03ed3b5ee5cf29c3cb64686d8cb476c2e75e00100`  
		Last Modified: Sat, 26 Sep 2020 02:25:09 GMT  
		Size: 119.3 MB (119294150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76361817d2ba9e695de331b76aeb9786ff1a974b950a05466d42dac9975bf39`  
		Last Modified: Sat, 26 Sep 2020 02:24:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dac10a242ba6c661fccd5c79b5d75b3d9ed54ac15b57e4f2de5a7bf5dcd074a`  
		Last Modified: Sat, 26 Sep 2020 02:25:26 GMT  
		Size: 66.6 MB (66580444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e1bd6d44e791c5e13b7c5275822096f635e1463291f514928eb8051d0d435f`  
		Last Modified: Sat, 26 Sep 2020 02:25:13 GMT  
		Size: 188.4 KB (188417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0655023823a2ba8844a36075ee735ee7a4fae41cbced0fdfa729cb9dca2b158a`  
		Last Modified: Sat, 26 Sep 2020 02:25:13 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a8b614b4f8763cf7c94118c3ce3926db47d692be5a0f4f4ba6377c0e8bb089`  
		Last Modified: Sat, 26 Sep 2020 02:25:16 GMT  
		Size: 10.3 MB (10283227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f29c55940b101019b1df47cd68f504d6ac73c72d8682c182a0bb9e45a13c48`  
		Last Modified: Sat, 26 Sep 2020 02:25:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72cbc908ec9e5fcbb91ba7ed128f4b4bf97d7237a14ba2fa61ba6a11ca68131`  
		Last Modified: Sat, 26 Sep 2020 02:25:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e3c6a6f5013fe15cd552610a4edf65e0d4305cf8b888fba3d87518d8fcb669`  
		Last Modified: Sat, 26 Sep 2020 02:25:54 GMT  
		Size: 76.1 MB (76093418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3b61022f15a352fb3f7239590c3380073bbdcbf2a6132d31d7e91c24e92285`  
		Last Modified: Sat, 26 Sep 2020 02:25:37 GMT  
		Size: 26.0 MB (26006871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513d1f74b7f1f57dbc846103abaa901595d42b1280d2b8b77e877be09943c67b`  
		Last Modified: Sat, 26 Sep 2020 02:25:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:79f44ef1a76774398d23d971eea0bd2e049735fac21376b757ca14d44a1fcda0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.9 MB (309884306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1794f97158443dfba6b78da6adc4d9ef1e803e3ede52b9799850def9b07b761c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 Oct 2020 18:19:38 GMT
ADD file:83fb716eb29f83f9e0ea0422f76e651689972d98764d3e19e4017bbd3fe9d6e4 in / 
# Fri, 23 Oct 2020 18:19:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 18:19:42 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 18:19:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 18:19:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Oct 2020 19:06:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 19:06:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 19:07:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 23 Oct 2020 19:17:09 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 23 Oct 2020 19:17:09 GMT
ENV LANG=C.UTF-8
# Fri, 23 Oct 2020 19:17:10 GMT
ENV LC_ALL=C.UTF-8
# Fri, 06 Nov 2020 03:18:44 GMT
ENV ROS_DISTRO=rolling
# Wed, 18 Nov 2020 09:43:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:43:10 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 18 Nov 2020 09:43:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 18 Nov 2020 09:43:13 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 09:44:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:44:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 18 Nov 2020 09:44:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 18 Nov 2020 09:44:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:45:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 18 Nov 2020 09:45:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 18 Nov 2020 09:45:08 GMT
ENV ROS1_DISTRO=noetic
# Wed, 18 Nov 2020 09:45:08 GMT
ENV ROS2_DISTRO=rolling
# Wed, 18 Nov 2020 09:46:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.8-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:47:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.9.4-2*     ros-rolling-demo-nodes-cpp=0.10.1-1*     ros-rolling-demo-nodes-py=0.10.1-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:47:05 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:00f57adb053c38c53d0655dee1ba47ed4cbd78cade062cf0e00f4b9790c7ed36`  
		Last Modified: Thu, 08 Oct 2020 08:25:26 GMT  
		Size: 27.2 MB (27163834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b235828e8d75b4f9129ec8b0a00d4e3f1c4d100eedb3f00696a2ec78862082f6`  
		Last Modified: Fri, 23 Oct 2020 18:20:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b606b1b8abdd386d8de6d1ce374b4dcdd4f7bcb4d68db64f09c03520fa5bf5`  
		Last Modified: Fri, 23 Oct 2020 18:20:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a57a33cfa330c14ee308343f9e2a73382a99ccf08c3c905dbb22831ec69c86`  
		Last Modified: Fri, 23 Oct 2020 19:24:02 GMT  
		Size: 1.2 MB (1178042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c463e5d0fb6cd5bb763e1856a0ca0db13a28b7a5ff531cf5ea2a2d778ab6e536`  
		Last Modified: Fri, 23 Oct 2020 19:24:00 GMT  
		Size: 5.5 MB (5513934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7a377b36c34d24c6e2a5c5a7f9cbcfad3511145bdf413951e31feedfadd819`  
		Last Modified: Fri, 23 Oct 2020 19:23:59 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad05750da6711171d9e6bc951deb25363c73387191387317035493b2dfb906db`  
		Last Modified: Fri, 23 Oct 2020 19:28:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363a137147330caddc78262b59531adf5daf224b968684437382e43c42691f1f`  
		Last Modified: Wed, 18 Nov 2020 09:56:23 GMT  
		Size: 106.0 MB (106010727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63831a3e6bb74b6c091e57a1bb098e8a73ef7ecf43315abe7ec4f89459334a1`  
		Last Modified: Wed, 18 Nov 2020 09:55:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae702efda7ea91b62114f5501d2efb968cd0bcf641bcffdf6cd2b59d0c54ad15`  
		Last Modified: Wed, 18 Nov 2020 09:56:46 GMT  
		Size: 61.0 MB (60961136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3c701278e3f37f7da058ff6dc058abe1b1bf5dacb2ba3515163143bf100a87`  
		Last Modified: Wed, 18 Nov 2020 09:56:32 GMT  
		Size: 191.1 KB (191099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7500fe0602a5abd53ab31e7f797326c5c584aea00f2110686ed7de3a82ff06a8`  
		Last Modified: Wed, 18 Nov 2020 09:56:31 GMT  
		Size: 2.1 KB (2065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bce88db8e48ccc56bb7097c996258fbf12ae77838708911a499749247727da`  
		Last Modified: Wed, 18 Nov 2020 09:56:42 GMT  
		Size: 9.5 MB (9488593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92cd11f5588669a3aea3e0a45d6340d740567db8d44bac55ecf23381cf2e643`  
		Last Modified: Wed, 18 Nov 2020 09:56:57 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe46c3deaac66dae70e1a54de26f49bb1e5ec2fa034e7d3d428b6e731de48e1`  
		Last Modified: Wed, 18 Nov 2020 09:56:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268687c36c5532ac19f8426a75213d7a795aecbd3f804a2e4660be0e3a89a8e6`  
		Last Modified: Wed, 18 Nov 2020 09:57:23 GMT  
		Size: 76.3 MB (76319304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68d95834ee9ca3542ea01d31273f70268b07d87cf71068016a0475d99beead4`  
		Last Modified: Wed, 18 Nov 2020 09:57:04 GMT  
		Size: 23.1 MB (23052064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d05bf267a6bc635794a858d0c13706c8e769e01f21566227d28dee7d225224`  
		Last Modified: Wed, 18 Nov 2020 09:56:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base-stretch`

```console
$ docker pull ros@sha256:ddbfb54f83a2d95785539d7622117f70e6a00ef11532a7e0a252691a654016e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-stretch` - linux; amd64

```console
$ docker pull ros@sha256:9932650464fd264cd1140a6a6fdfb417caf70d0fe2feae03f254f78d881575d8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.0 MB (499952080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4339daf9e0c55d5e06b9e97c1bfb03f2d859bdc8b54bc9f35b475d7f3d2c271f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 18:17:30 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:17:35 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 26 Feb 2020 18:17:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 26 Feb 2020 18:18:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:18:26 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 18:18:26 GMT
ENV LC_ALL=C.UTF-8
# Wed, 26 Feb 2020 18:18:26 GMT
ENV ROS_DISTRO=melodic
# Wed, 26 Feb 2020 18:18:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 26 Feb 2020 18:20:45 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:20:47 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 26 Feb 2020 18:20:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 26 Feb 2020 18:20:48 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 18:22:07 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7851b385b3454126f02da75d871c31cab343adb6252f96c606208321ebe5f424`  
		Last Modified: Wed, 26 Feb 2020 18:26:49 GMT  
		Size: 10.5 MB (10476682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0f3c809d5bd964fa9c99f4d533d31508fe61ced1652651935ec77d4fa693fe`  
		Last Modified: Wed, 26 Feb 2020 18:26:46 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d860519553be9002ec6cc168b986adc95e13723c9d114964b18cbea0e19c90`  
		Last Modified: Wed, 26 Feb 2020 18:26:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16b9d760787b93bb8c3f0c7872b401fb00d96f3fd2a870a6f83e531d20d85e`  
		Last Modified: Wed, 26 Feb 2020 18:27:07 GMT  
		Size: 64.8 MB (64770161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9baabdeab314d3737e662c388e0b2b03c57de9e21f1e9e6aad43c4f78764c81`  
		Last Modified: Wed, 26 Feb 2020 18:26:45 GMT  
		Size: 426.8 KB (426764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b928396e18c50dff7d8bbe31d6340783a3d4472fa5f16f33a49fab28739f228`  
		Last Modified: Wed, 26 Feb 2020 18:27:50 GMT  
		Size: 270.4 MB (270426039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647876d988155403f463b985cdcbf476c331e01ce9b2bfd71b391abd87b27540`  
		Last Modified: Wed, 26 Feb 2020 18:26:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ed7a7ca1ab232e4fbf2652a60bbcc29ea6fe09a6c4dabb1b2db4de08ae08e9`  
		Last Modified: Wed, 26 Feb 2020 18:28:21 GMT  
		Size: 108.5 MB (108474685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2faade4fe6adba2f9cca34336cbb2d155e8fe412c5153563cd9a55cea7147697
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.0 MB (443016659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9445d40e3b8f06c7cb6d2de0edbadeba82e5a7da4755733ec346c9dfa9d632`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:03 GMT
ADD file:c82c7dc82c2eb3b50218c35e1b848f707b134d2df957f57125408f69aaeb9b96 in / 
# Wed, 26 Feb 2020 00:50:15 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 14:31:39 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:31:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 26 Feb 2020 14:31:47 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 26 Feb 2020 14:33:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:33:23 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 14:33:24 GMT
ENV LC_ALL=C.UTF-8
# Wed, 26 Feb 2020 14:33:25 GMT
ENV ROS_DISTRO=melodic
# Wed, 26 Feb 2020 14:33:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 26 Feb 2020 14:36:54 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:37:10 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 26 Feb 2020 14:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 26 Feb 2020 14:37:12 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 14:38:50 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:668c278237ef972312df4979c8fb1a927b38db5da09f094ae4fcc84a061dedf8`  
		Last Modified: Wed, 26 Feb 2020 00:58:30 GMT  
		Size: 43.2 MB (43158146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec93ccfa7a93f6e8e92bfb6a4612d88201a991de0eeccbf0f0bf911e494b010`  
		Last Modified: Wed, 26 Feb 2020 14:46:38 GMT  
		Size: 9.8 MB (9774844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d47cc5c856874753256905adae1cafc7bbe555293057734a15adff043ad552`  
		Last Modified: Wed, 26 Feb 2020 14:46:36 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8904c2c29a9d325e34d20fc23a9bf0424e4011a33a408e44efc9d3a7afd762`  
		Last Modified: Wed, 26 Feb 2020 14:46:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd405032f54a80c542f1c495a333e79235726b6bc13a929b1cd5b8c1857cf4da`  
		Last Modified: Wed, 26 Feb 2020 14:47:00 GMT  
		Size: 62.1 MB (62091345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da22cef13f13ce297cd764e86e8e695631eb4f9bd35437f30cb2fb4121836e4f`  
		Last Modified: Wed, 26 Feb 2020 14:46:34 GMT  
		Size: 426.5 KB (426457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c556607af67c09197a3819a5d4186a8a16161d13034880bcfa9896a95453d8ee`  
		Last Modified: Wed, 26 Feb 2020 14:47:46 GMT  
		Size: 224.6 MB (224601602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61457eaec54891acb526a2385adff233378c15c155753857cab7397dfce078c`  
		Last Modified: Wed, 26 Feb 2020 14:46:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d522db6c8689265e2a824a336e54ef5e1d066934054d93dd8a56e3fb7098a9`  
		Last Modified: Wed, 26 Feb 2020 14:48:16 GMT  
		Size: 103.0 MB (102962444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

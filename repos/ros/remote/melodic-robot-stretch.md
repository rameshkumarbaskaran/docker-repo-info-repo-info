## `ros:melodic-robot-stretch`

```console
$ docker pull ros@sha256:48b3366e54ce7af06c1ee782edba4438e5c621d570d75f56d9f980ac172e78cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-robot-stretch` - linux; amd64

```console
$ docker pull ros@sha256:e4e35090adc43385e1a56a7bfbafefff14a368c52128333cb88c09236f48a354
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.9 MB (462898640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1404d8285c0e2ca180a8346045b75cacebf66f6d7407cdc73d594d81c9e289d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:23:05 GMT
ADD file:d9e4f6f4fc33703b766642a5642cabb2b01675bb55cf6050f2e91507577ff570 in / 
# Wed, 12 May 2021 01:23:06 GMT
CMD ["bash"]
# Wed, 12 May 2021 17:09:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:09:15 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 12 May 2021 17:09:16 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 12 May 2021 17:09:16 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 17:09:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 12 May 2021 17:09:17 GMT
ENV ROS_DISTRO=melodic
# Wed, 12 May 2021 17:10:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:10:50 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 12 May 2021 17:10:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 12 May 2021 17:10:50 GMT
CMD ["bash"]
# Wed, 12 May 2021 17:11:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:11:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 12 May 2021 17:11:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:12:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bfde2ec33fbca3c74c6e91bca3fbcb22ed2972671d49a1accb7089c9473cac12`  
		Last Modified: Wed, 12 May 2021 01:29:52 GMT  
		Size: 45.4 MB (45380083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a867e9d598a219f826e3b76f5280f3d106205d5fa6b8e1f2d421fd463d8fbc`  
		Last Modified: Wed, 12 May 2021 17:21:34 GMT  
		Size: 6.9 MB (6869206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302212f98ddaf07466a1b811fe425f01ff9f85b2778ce2d5b97611934d34240f`  
		Last Modified: Wed, 12 May 2021 17:21:33 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b35ff6673ef12169b553429937e2fe4a366a68e6eb03770829a0b95f3361ad`  
		Last Modified: Wed, 12 May 2021 17:21:34 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70bec3846c6a4887618d8cf19d2db025d8d2122df811164567153330bf2e1a8`  
		Last Modified: Wed, 12 May 2021 17:22:22 GMT  
		Size: 270.0 MB (270044121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faf0f68b02c8fbcd34133d9f9b4bc1413a3f0851320b60e97d7f30e2404b931`  
		Last Modified: Wed, 12 May 2021 17:21:33 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5542020de522c68695172342481ec3eb28e50500ff526fa7af67c329da7b7b2b`  
		Last Modified: Wed, 12 May 2021 17:22:45 GMT  
		Size: 70.2 MB (70153767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac6bff56dc550773ba81dc63cdc50b0a51f817a1c5d8a613db08f79e0484287`  
		Last Modified: Wed, 12 May 2021 17:22:32 GMT  
		Size: 264.0 KB (264024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cb4d3b0a8144bac01a9f75f0f783076bca2e1810e5651798155f967fd4ad95`  
		Last Modified: Wed, 12 May 2021 17:22:42 GMT  
		Size: 55.1 MB (55059368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6464c98abb06409cba8fc8ab19b8e946ef43b26beccc062a075a04dd60c3730`  
		Last Modified: Wed, 12 May 2021 17:22:58 GMT  
		Size: 15.1 MB (15126255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:133a47d9e740d61a42df65f4c277a9bf1b7340e7ae15297f3fc4c89ac046933b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.8 MB (407785848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d66ca456f115870443228c5f9da65ef199c62c7da3dced04614d192b0031f4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:56:12 GMT
ADD file:9582243afc9973a3708fda530270ae8f23796b20a532a9f07e4faaf245e2cdc0 in / 
# Wed, 12 May 2021 00:56:18 GMT
CMD ["bash"]
# Wed, 12 May 2021 16:45:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 16:45:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 12 May 2021 16:45:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 12 May 2021 16:45:14 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 16:45:15 GMT
ENV LC_ALL=C.UTF-8
# Wed, 12 May 2021 16:45:16 GMT
ENV ROS_DISTRO=melodic
# Wed, 12 May 2021 16:47:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 16:48:07 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 12 May 2021 16:48:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 12 May 2021 16:48:09 GMT
CMD ["bash"]
# Wed, 12 May 2021 16:48:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 16:49:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 12 May 2021 16:50:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 16:51:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:41f38ce3010a5142300d74e5e19db4dea7694f4771471c330fff27c633f8ba32`  
		Last Modified: Wed, 12 May 2021 01:04:15 GMT  
		Size: 43.2 MB (43177820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf89e0449041f43ec9cebbb329a0431405cbb9c2ecb93bdbd93e510ef948aca4`  
		Last Modified: Wed, 12 May 2021 17:11:00 GMT  
		Size: 6.4 MB (6442905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c79df076887a87df88c16818f8b6626b656a8f0c99819ec7e9f33d59e47b072`  
		Last Modified: Wed, 12 May 2021 17:10:55 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ca281ecc3cb7378d6f88f78194435d7bb2edc558d7a897f8eb8d01490e2864`  
		Last Modified: Wed, 12 May 2021 17:10:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1e2c03847e9dc3c54e77bce32bda9081216ebf4e6baea5cbccf5d18b1f4059`  
		Last Modified: Wed, 12 May 2021 17:13:26 GMT  
		Size: 225.1 MB (225139022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a450c9d643b923cd090f55be30004b47cb7357c136db751382cd5b32a7eacfb2`  
		Last Modified: Wed, 12 May 2021 17:10:55 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27218ab637a123da0eb97148c44479ddcf9d1e66ee90ae173079678e1008da64`  
		Last Modified: Wed, 12 May 2021 17:14:17 GMT  
		Size: 64.8 MB (64841756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0aa0fce91afd6f03c52305bc45b1ba992ba1cc13ded7ad00ba40f70c15786f3`  
		Last Modified: Wed, 12 May 2021 17:13:37 GMT  
		Size: 264.0 KB (264041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afe3ba3386ffe3a4413d76f3c617514c448cc470b7b8532a6103b64b576309f`  
		Last Modified: Wed, 12 May 2021 17:14:15 GMT  
		Size: 53.2 MB (53245430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4184f141fa4746f4d09002168ae6098a254db1ba8992cc6322674667d7191c9f`  
		Last Modified: Wed, 12 May 2021 17:14:35 GMT  
		Size: 14.7 MB (14673055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:4ae0a12a1aae388638b1c4135efc02b2b23765e67038055b2d7f96318ae92f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:a32a6256a565b1c873b9158dbc55370b21fbd1c6fa7aa7236e69c4076553d11c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.5 MB (463499043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302394eab505493b12ad8064dc19f9156ec7f16d387f013a534b089c907214e0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:54 GMT
ADD file:2f52161f98fff6a77f865fbd61397b76f3ad3391fa6d694a50a08ad43fd5c8c9 in / 
# Sat, 04 Feb 2023 06:51:54 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:15:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:15:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 04 Feb 2023 13:15:57 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 04 Feb 2023 13:15:57 GMT
ENV LANG=C.UTF-8
# Sat, 04 Feb 2023 13:15:58 GMT
ENV LC_ALL=C.UTF-8
# Sat, 04 Feb 2023 13:15:58 GMT
ENV ROS_DISTRO=noetic
# Sat, 04 Feb 2023 13:17:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:17:21 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 04 Feb 2023 13:17:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 04 Feb 2023 13:17:22 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:17:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:17:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 04 Feb 2023 13:18:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d42a0fb443d7323eac0a2073d5a229cf6871c4cbddd8e85bad4b0301b2dadedb`  
		Last Modified: Sat, 04 Feb 2023 06:56:36 GMT  
		Size: 50.4 MB (50449110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44bf9327e4b7a8bf848c3699b20510e32f95481ba13b8d9a946754f18342fa5`  
		Last Modified: Sat, 04 Feb 2023 13:24:05 GMT  
		Size: 10.9 MB (10897097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b8a10b01929717aa618dcd6f710b0e66ce6ab72f8843e73f630735c2a73aed`  
		Last Modified: Sat, 04 Feb 2023 13:24:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dede64640aa97c0401af7c42dfc94a82841ba4c553f1e18510827c72b00afa14`  
		Last Modified: Sat, 04 Feb 2023 13:24:04 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604ceb6b1629e4d9e26c32dc0a33f68646f3e612f944ca073bdae4a5e7669778`  
		Last Modified: Sat, 04 Feb 2023 13:24:37 GMT  
		Size: 239.2 MB (239213880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659253c15397780551648f4e45c5915f6c3755e130e90fab1863f70c0124c436`  
		Last Modified: Sat, 04 Feb 2023 13:24:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bab81f9da21051763a7465deae8adac30260328bb9c35d25d676bd16176d27`  
		Last Modified: Sat, 04 Feb 2023 13:24:55 GMT  
		Size: 86.6 MB (86621101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c106973deec2e91cee88be69bb3557ec1139dd8cf6e0acc3af22d0f75bd0f43`  
		Last Modified: Sat, 04 Feb 2023 13:24:43 GMT  
		Size: 337.3 KB (337308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893cc2ca9a9446635b02ba2e46a324d7c9106103c2fc2a52e182f357d8b38f87`  
		Last Modified: Sat, 04 Feb 2023 13:24:53 GMT  
		Size: 76.0 MB (75978133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:77a1a669b9e32e04f491e769db22195778fa02da45cbc2edb36c6674b010b4c6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.4 MB (403372751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0026e1e09f725c5677b087ea2f2084945da1e3c80a450c3f9d8ec7e130e2a92`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:45 GMT
ADD file:0241487c3fb43506be1511724644c00339c32361e6b4c21a224d7190e4e1063b in / 
# Sat, 04 Feb 2023 06:17:46 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:26:04 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:26:04 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 04 Feb 2023 17:26:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 04 Feb 2023 17:26:06 GMT
ENV LANG=C.UTF-8
# Sat, 04 Feb 2023 17:26:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 04 Feb 2023 17:26:06 GMT
ENV ROS_DISTRO=noetic
# Sat, 04 Feb 2023 17:27:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:27:25 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 04 Feb 2023 17:27:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 04 Feb 2023 17:27:26 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:27:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:28:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 04 Feb 2023 17:28:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e0a5a2afd38370f358c0a7154362a8d17faf709c206b40b1553a077f810c3b3`  
		Last Modified: Sat, 04 Feb 2023 06:21:43 GMT  
		Size: 49.2 MB (49239373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b265718197183247c812f6e77250082b3ad9a6563b418ee7eb1d9aa48e81d2`  
		Last Modified: Sat, 04 Feb 2023 17:34:03 GMT  
		Size: 10.9 MB (10902637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c398dcb16c154524c0eb8b27ca3127a7af3ce52892f4f3e1fbb6769b147242`  
		Last Modified: Sat, 04 Feb 2023 17:34:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8806fb750e9db8cf1f79371eb9ad9aba0b0cf3a9efc612c4ca346319d1f847`  
		Last Modified: Sat, 04 Feb 2023 17:34:02 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2435ce7d72ccf71a222c2c1686bf6878a366f1c1a7951b450e40bfb17b285070`  
		Last Modified: Sat, 04 Feb 2023 17:34:26 GMT  
		Size: 184.4 MB (184402890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdbfb1ecc2f66b4bbde1c3d1610bf6704cd849a833fbb4d42f8db9a7705bb3d`  
		Last Modified: Sat, 04 Feb 2023 17:34:02 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46c4d3e1b6c6355329a5fd3d1b3ec96c3954acd510e496e300865d260b9f4a8`  
		Last Modified: Sat, 04 Feb 2023 17:34:41 GMT  
		Size: 84.4 MB (84397528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f153467df2e0635b70db210221437a533f094f9db97172b46e54f934538001`  
		Last Modified: Sat, 04 Feb 2023 17:34:32 GMT  
		Size: 337.3 KB (337312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58e2a2f615bb1e77778923fa448498f501ddd1ee468ebe109e1c0f5e3ccd68`  
		Last Modified: Sat, 04 Feb 2023 17:34:40 GMT  
		Size: 74.1 MB (74090596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

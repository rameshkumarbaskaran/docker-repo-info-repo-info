## `ros:melodic-ros-base-stretch`

```console
$ docker pull ros@sha256:3b4f286d23a3627de33d9bfaa43381b9f38be5c3050fa59be02bc3ec0eca1227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-stretch` - linux; amd64

```console
$ docker pull ros@sha256:7235e2d2c64ad525c8f7efee284650a909b793d3c38c559f5c22ce1aa4ec633a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.8 MB (447779175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad88fe112ef954583459bc9376e879b2ae6ba28497e75efa9b2847c877d3aa89`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:30:04 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:30:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 31 Mar 2021 14:30:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 31 Mar 2021 14:30:09 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 14:30:10 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 Mar 2021 14:30:10 GMT
ENV ROS_DISTRO=melodic
# Wed, 31 Mar 2021 14:31:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:31:59 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 31 Mar 2021 14:31:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 Mar 2021 14:31:59 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:32:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:32:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 31 Mar 2021 14:33:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f734eb85b47bda51f2595c99d9429f89241d0ea4b5882eac9f352a8ee9591eca`  
		Last Modified: Wed, 31 Mar 2021 14:44:40 GMT  
		Size: 6.9 MB (6869232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd8cf4e482c701e93c615dcd7c3c840953a9a630b31c402674529810bdbbd56`  
		Last Modified: Wed, 31 Mar 2021 14:44:38 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d597486b45058ba2465ebade2fb8a1b02f26df2e25a83f4033bec989244bcde2`  
		Last Modified: Wed, 31 Mar 2021 14:44:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc68b2ecd4ede5ed9bbf9c3574540d2e6cc9c87c642275088cb5e8663ca371ac`  
		Last Modified: Wed, 31 Mar 2021 14:45:25 GMT  
		Size: 270.1 MB (270066130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a94b685ae3e48152c7e4ea1b92c8375d2e7a912c33595e1c9ccbb64d61289a`  
		Last Modified: Wed, 31 Mar 2021 14:44:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c84acda20e6c81b1e855545e8db6447c34e93f330dce80633d971cd52dd2a0b`  
		Last Modified: Wed, 31 Mar 2021 14:45:49 GMT  
		Size: 70.2 MB (70152366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e388c0568292babb2cd4301569b25937b1d59f8a2776f3d51d76ef3cd17e17`  
		Last Modified: Wed, 31 Mar 2021 14:45:36 GMT  
		Size: 250.5 KB (250541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1c899f95bf3dba72c68165a7b76cd6ffb41c16176d8b3a88afed45ca86a441`  
		Last Modified: Wed, 31 Mar 2021 14:45:47 GMT  
		Size: 55.1 MB (55059142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8d29f17800a0f3282123164d104ea92ac845bf9a3d68a602c7e36e857b6434c7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.1 MB (393074913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ee088da844c4e6680b553ddaa91692033b755b7195a3144230b2994e29bdde`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:45 GMT
ADD file:0546f28e5d1be54699d1e0756275203da731735b3212f2ff1a87cd7f8dcc9049 in / 
# Tue, 30 Mar 2021 21:49:50 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 13:38:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 13:38:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 31 Mar 2021 13:38:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 31 Mar 2021 13:38:12 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 13:38:13 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 Mar 2021 13:38:14 GMT
ENV ROS_DISTRO=melodic
# Wed, 31 Mar 2021 13:41:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 13:41:27 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 31 Mar 2021 13:41:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 Mar 2021 13:41:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 13:42:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 13:42:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 31 Mar 2021 13:43:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9317dc7ea567b49ade0ea730b5530d1363b065549e8b75a198e0b60bdde1f1d7`  
		Last Modified: Tue, 30 Mar 2021 21:56:46 GMT  
		Size: 43.2 MB (43177588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9bcb4567c53b5710817f63af7d0c14a3dad36b823f3cc9f142434d89dd7cea`  
		Last Modified: Wed, 31 Mar 2021 14:03:12 GMT  
		Size: 6.4 MB (6442935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84574c97c15ff3c495faceaf91ec7efac2d7735c4fe357cc256339c4fe93410a`  
		Last Modified: Wed, 31 Mar 2021 14:03:09 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefd0949cc578f2b84114a09843d05b951725916a271d79c9e803a14021734f8`  
		Last Modified: Wed, 31 Mar 2021 14:03:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fafb8ecac1b3a711771dfd44718d41e04b5dcf0e3545af1cc8fc71a84905bb3`  
		Last Modified: Wed, 31 Mar 2021 14:05:04 GMT  
		Size: 225.1 MB (225114741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e8c7efe0eb7db52b3a500557e94b2126eb204eaf0deb2cb3356cdd72b378f2`  
		Last Modified: Wed, 31 Mar 2021 14:03:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae8b9ae40586f1c7f4a31c6f954c7fc823f68d3a1ca653021947d6561a88274`  
		Last Modified: Wed, 31 Mar 2021 14:05:39 GMT  
		Size: 64.8 MB (64841811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2302c8cf265a1c9f49435bdb51988d9f6c72875806726beb107b029b0229c5b3`  
		Last Modified: Wed, 31 Mar 2021 14:05:15 GMT  
		Size: 250.5 KB (250541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bbb4913683784dfcd753468a71f92c352037f11cc8f978e91e1731b4591aba`  
		Last Modified: Wed, 31 Mar 2021 14:05:41 GMT  
		Size: 53.2 MB (53245478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

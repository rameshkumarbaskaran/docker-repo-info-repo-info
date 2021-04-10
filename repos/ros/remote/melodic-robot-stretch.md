## `ros:melodic-robot-stretch`

```console
$ docker pull ros@sha256:8a3110022f7b88c32e3d8b9446831b4858722041f24926a680e212f4d95a25b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-robot-stretch` - linux; amd64

```console
$ docker pull ros@sha256:ae2498699735833f49ea560f5ccd1a96b89b2d5985da87b45ad8c83c26490e80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.9 MB (462905522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d1c803c67897aac5cb86a11352f3e44b37ac8f6cf0567009360ca415989b1f`
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
# Wed, 31 Mar 2021 14:33:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e67cefb46299b5fbdd4bc96f10a0303a01effbc94dc5bda2abd1a7786de7e189`  
		Last Modified: Wed, 31 Mar 2021 14:46:01 GMT  
		Size: 15.1 MB (15126347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0f828873bd321b8e2a6dbbedd7cd13787f371ba667e94917b3b614bf9cff53ac
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407743712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6c6d056b315d1d888517c1b9ff27bc2a1f10562933ccc4f7cc976cbe12e91e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:43:48 GMT
ADD file:64990d14743657dbcbe885739e43ac964a0239a63e4693e6401b0884ab96e09b in / 
# Sat, 10 Apr 2021 00:43:50 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 15:24:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 15:25:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 10 Apr 2021 15:25:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 10 Apr 2021 15:25:10 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 15:25:11 GMT
ENV LC_ALL=C.UTF-8
# Sat, 10 Apr 2021 15:25:13 GMT
ENV ROS_DISTRO=melodic
# Sat, 10 Apr 2021 15:28:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 15:28:27 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 10 Apr 2021 15:28:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 10 Apr 2021 15:28:29 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 15:29:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 15:29:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 10 Apr 2021 15:30:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 15:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:30bd672115ff6f225cb98d2d7f1ed62feb72c2612297b2ac615e762e436c64ec`  
		Last Modified: Sat, 10 Apr 2021 00:49:51 GMT  
		Size: 43.2 MB (43177772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d267bb40382f265c3a2b17a40e3b0ac14aefec3241d3165a352fb9e8b3a3611`  
		Last Modified: Sat, 10 Apr 2021 15:51:31 GMT  
		Size: 6.4 MB (6442907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f409406543418e427fce300b8eb166b61fa11defc2b68267d6ffa9a507c77309`  
		Last Modified: Sat, 10 Apr 2021 15:51:28 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34172e3929e56eb4fba600b5c480baf8112d57abe120790cbe1befa7d3fb9e61`  
		Last Modified: Sat, 10 Apr 2021 15:51:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60954ec9568f6a7e2dbdddb363be902d336e96653dc84225e0e1fb5ba980ab66`  
		Last Modified: Sat, 10 Apr 2021 15:53:14 GMT  
		Size: 225.1 MB (225108617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95e19ab692b33c8148268009f1a7533000eb4b4c804fcdd8ce42321edce7d35`  
		Last Modified: Sat, 10 Apr 2021 15:51:28 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665759b1c2ca319d3fbc7fd1d3f169931874b128cd4fa7598871653363c2c545`  
		Last Modified: Sat, 10 Apr 2021 15:53:49 GMT  
		Size: 64.8 MB (64841566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa262508378f63ea709dfb9521e70536cb0fab5bf5d3e78bc5db723ef6978c9`  
		Last Modified: Sat, 10 Apr 2021 15:53:25 GMT  
		Size: 251.5 KB (251511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60f21cf4fb5904d41f84d88f936971f252ee4c968e4f87fc4259658884064e1`  
		Last Modified: Sat, 10 Apr 2021 15:53:53 GMT  
		Size: 53.2 MB (53246575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648f8269f77d5b8529f3ac2ffd3bf83af69046337c65e6d598a46cea428d356c`  
		Last Modified: Sat, 10 Apr 2021 15:54:04 GMT  
		Size: 14.7 MB (14672946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

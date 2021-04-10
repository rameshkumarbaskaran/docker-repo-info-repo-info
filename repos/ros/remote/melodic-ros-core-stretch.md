## `ros:melodic-ros-core-stretch`

```console
$ docker pull ros@sha256:333fbfc6c9976598efe0ee7092b8587bd19dda13b1f0fd7ff5fd8c5acb093094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-stretch` - linux; amd64

```console
$ docker pull ros@sha256:0137e8aaa9674f842a3ef1936d7f531d8b8e0daee9f418a864bca975af09a3d5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322317126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bfd1049c015496d17696faaa2fc77969ac2058f1e717da2115069d8073c789`
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

### `ros:melodic-ros-core-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9c7656aec543122a885e3d585794c287601f79d360f3f34e77d680b192863e33
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274731114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba461b1c7182bc79602fe5b404b31bd2d5eaeef9f296314848f097008318ad1d`
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

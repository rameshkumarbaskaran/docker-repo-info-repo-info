## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:347756299830cf7affa34689cfb8cdd12517cfb4d419c14b9eceb20b587abde4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:3b471ec795136f54b05fdf0fd0879caf27782dbf8b58a958b732739c4f49b568
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300285288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd335733f94278539b28dd40bbc2337ae3437ef043aff4c875f88f2734a3545`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:41 GMT
ADD file:89234bb2f86c7eb890235a48904d1c9898a8d287a525c4fe5698d4a04cdd8f12 in / 
# Fri, 26 Mar 2021 15:20:42 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:18:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:19:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 27 Mar 2021 09:19:01 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 27 Mar 2021 09:19:01 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 09:19:01 GMT
ENV LC_ALL=C.UTF-8
# Sat, 27 Mar 2021 09:19:02 GMT
ENV ROS_DISTRO=noetic
# Sat, 27 Mar 2021 09:20:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:20:07 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 27 Mar 2021 09:20:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 27 Mar 2021 09:20:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8bf9c589d5f9475f1fcc050e02308d6b4eeb86eab7752ef948a13693e81a6aaa`  
		Last Modified: Fri, 26 Mar 2021 15:27:11 GMT  
		Size: 50.4 MB (50400278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f449035c3af90c31ff21aac54677ddaa94af7b4199927b2f133e67e8595890b`  
		Last Modified: Sat, 27 Mar 2021 09:29:31 GMT  
		Size: 10.9 MB (10891856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456137ab974bca1d8f62d7d5680410744326ca834b1a0b28f08439320b0760e6`  
		Last Modified: Sat, 27 Mar 2021 09:29:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1385d40e15645e2c90531a6509af986cdf1443339297d7fe19d8279b932c5ca`  
		Last Modified: Sat, 27 Mar 2021 09:29:28 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb71cc1ea410520d668b783bdd3e0a1a5c7b5f781d4adc019127c0b6c76a3f1c`  
		Last Modified: Sat, 27 Mar 2021 09:30:24 GMT  
		Size: 239.0 MB (238991317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886c7fa5d1013621ff1cbf8d90848d0ccd58d5769abfb273e8a5760ea7cbdd10`  
		Last Modified: Sat, 27 Mar 2021 09:29:28 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bbcaa1b744a8702b9e5bfc3a6330944bb3acd34cc6ade67e3914462076761e72
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244275976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa6b59b299c7fa3fd1f165a0b39a0f75e87e50e1ee9141cfd9107cf4dbbb110`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:41:27 GMT
ADD file:536306ac674764a6a921b71adcbb4440797b916a0583b9270cd1565d62642e4d in / 
# Fri, 26 Mar 2021 15:41:30 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 08:44:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:44:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 27 Mar 2021 08:44:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 27 Mar 2021 08:44:56 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 08:44:57 GMT
ENV LC_ALL=C.UTF-8
# Sat, 27 Mar 2021 08:44:58 GMT
ENV ROS_DISTRO=noetic
# Sat, 27 Mar 2021 08:46:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:47:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 27 Mar 2021 08:47:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 27 Mar 2021 08:47:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:383261dafcc4f63ecae5f2d661d1ef8d0a5e1c9f4b1f12285115baca7d101d5a`  
		Last Modified: Fri, 26 Mar 2021 15:48:21 GMT  
		Size: 49.2 MB (49196215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5ff3f5d28c8af3f88665a2aa84284c359ed12aa33168c1a64a78f0ade71297`  
		Last Modified: Sat, 27 Mar 2021 09:00:29 GMT  
		Size: 10.9 MB (10883463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74fad49a464d1b87097bc055363ccb50dc8a92828ad693eb5e1ee949e41b56e`  
		Last Modified: Sat, 27 Mar 2021 09:00:27 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f561924c9d78e4a9873808f60fb46676818c58ab68fb4ecd8fcc00d3953f0e7`  
		Last Modified: Sat, 27 Mar 2021 09:00:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b4a7908a17a34219acf017102f05b6e2720d17bc539a55d3916795c4c949f1`  
		Last Modified: Sat, 27 Mar 2021 09:01:34 GMT  
		Size: 184.2 MB (184194463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c4e20a52ff1b28780dfe7a728e042eb5ba0421aaa6b2e917eb1a9588932ac4`  
		Last Modified: Sat, 27 Mar 2021 09:00:27 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

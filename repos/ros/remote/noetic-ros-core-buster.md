## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:825789e1394223ae6466124fe5120e485542bb93e8f5c071b2dc207a7613169c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:b22f3c646df1f2f5a59bafea4aa9ad5d0c6199d03c700c947a9edfaf8d145378
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300562501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e85c5f66d0bef351fa22c4200c46fe54c7b875ae5fad07bd91b577a0d3a54a`
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

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:debf08df675a5e5c543853fb37d521f93987f06e51453af8c6a7f90aa4388957
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244547315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b6a3110bb660a4f7859e56d0c9c7b8a1c6f77ea8103fe97016f3359b5e537b`
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

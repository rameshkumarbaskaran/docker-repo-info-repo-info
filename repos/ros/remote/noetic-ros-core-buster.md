## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:77cc16362762ec51b998f51a57c689b3fa4f1899b9bf8cb7602865c034ce9f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:2c50e8c3d36e29203b9f3c0f5cc5937b65702932c7af75b46e3297ea653c4e7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300550539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8233aa7bd2facad013538e003fdd08eb0c1e5ac30e030b2e519dc8c56858ce8c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:05 GMT
ADD file:00d8a84de32d523b936621886a10683664f38d8ec0846a60511fcf3a99d0e0c4 in / 
# Tue, 06 Dec 2022 01:21:06 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 06:55:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 06:55:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 06 Dec 2022 06:55:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 06 Dec 2022 06:55:41 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 06:55:41 GMT
ENV LC_ALL=C.UTF-8
# Tue, 06 Dec 2022 06:55:41 GMT
ENV ROS_DISTRO=noetic
# Tue, 06 Dec 2022 06:57:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 06:57:14 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 06 Dec 2022 06:57:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 06 Dec 2022 06:57:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:620af4e91dbf80032eee9f1ff66a8b04119d7a329b2a13e007d69c8a0b337bf0`  
		Last Modified: Tue, 06 Dec 2022 01:25:30 GMT  
		Size: 50.4 MB (50448865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821976fb70a1a949ce1e0f957ab373f10caff567977865f6e32aa1c8e0f0aa67`  
		Last Modified: Tue, 06 Dec 2022 07:03:56 GMT  
		Size: 10.9 MB (10896976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a368d393abce7be1308b98ad183e4e4e4b0ceab2dc5e6d66a4f270e3b60209`  
		Last Modified: Tue, 06 Dec 2022 07:03:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e639599375ee6d0b5e7ec7f657f4e583e08f7647519f83dd8816c2a514666d`  
		Last Modified: Tue, 06 Dec 2022 07:03:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27796b9579d3ee5904e92b8b0d48179d0f2079d8bda295f20ba361c7245a6fa`  
		Last Modified: Tue, 06 Dec 2022 07:04:27 GMT  
		Size: 239.2 MB (239202286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c9359756e3a8a665915f05eb2303d5b7cb66ee058e2ff79826c06765230dad`  
		Last Modified: Tue, 06 Dec 2022 07:03:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ea0e03de4581586ce6d534f9e6fc2c2bf8e50a50168b9b0afb57d3fbe4f7582d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244519823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65702135bd10e5f317ce9f171437335f2de36dbf8ab6a4ba4da9465bdefaaffa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:26 GMT
ADD file:2122642b8ad9a333f73cba41ff9cc829542740e0e3c88379a7c9511fbfc28991 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 11:01:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:01:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 15 Nov 2022 11:01:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 15 Nov 2022 11:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 11:01:16 GMT
ENV LC_ALL=C.UTF-8
# Tue, 15 Nov 2022 11:01:16 GMT
ENV ROS_DISTRO=noetic
# Tue, 15 Nov 2022 11:02:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:02:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 15 Nov 2022 11:02:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 15 Nov 2022 11:02:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:34983cc1fd1c67f0d8b7b8b4320539206a1c098388b3a671abe88b45f157978d`  
		Last Modified: Tue, 15 Nov 2022 01:44:52 GMT  
		Size: 49.2 MB (49233786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0d6aa77dc7e3e6cb404ca839ffe05429dc865c6f53f61d199627cddc197c0a`  
		Last Modified: Tue, 15 Nov 2022 11:09:47 GMT  
		Size: 10.9 MB (10902568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3955f704bc1936a82d8f59acffc7b268f5b37cb949b1eae1f51ddb2efb63f8c9`  
		Last Modified: Tue, 15 Nov 2022 11:09:46 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eb3e975face0a771cbbe4d7fcbaecd10a64dc2553cc0d0d405eabcd005d5a8`  
		Last Modified: Tue, 15 Nov 2022 11:09:46 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec0a529ecc45627e8b17f5c8845fa00a9cca8cd87cfa9629ee2b23196501416`  
		Last Modified: Tue, 15 Nov 2022 11:10:09 GMT  
		Size: 184.4 MB (184381056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b039cb484dc03fe448fd378fdeeb38fa7aed48361105571b0a99aa20163544cb`  
		Last Modified: Tue, 15 Nov 2022 11:09:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

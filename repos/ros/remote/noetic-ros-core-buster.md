## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:a4a811bb0506fd730247101c9095e391520714c7e163db4b78349aa63e9f7fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:953dfc6c66e60b0106ef4cbc304baef2155861ecbba69d13bd1db5433bdf5c7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300610530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43f4b3df3a420ffe44998a06fbcdfd1f2a73251645b24ba5dc015a0ef05158a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:07 GMT
ADD file:d176a72312205fc75b2950df98f4ed25abadd4b053b9d85bea67466a5b30220f in / 
# Tue, 02 May 2023 23:47:08 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:38:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:38:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 May 2023 21:38:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 May 2023 21:38:39 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 21:38:39 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 May 2023 21:38:39 GMT
ENV ROS_DISTRO=noetic
# Wed, 03 May 2023 21:39:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:39:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 May 2023 21:39:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 May 2023 21:40:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a94073ab46f8d565f5938cc345d32f7adda10a2585e39555079da9d4ee595974`  
		Last Modified: Tue, 02 May 2023 23:50:40 GMT  
		Size: 50.4 MB (50448697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6a520b96cab6be544c3de79dfbd2e79a43648778ff5ffc9cea03b9afea1a8a`  
		Last Modified: Wed, 03 May 2023 22:02:33 GMT  
		Size: 10.9 MB (10897025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b18fd569bd474fa851fd78f1d3bf2e9678d8423061fdd217c621a34a0e1a18`  
		Last Modified: Wed, 03 May 2023 22:02:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b96262d8a19c986620307e5e5f5bc87d241ebddd343a22e317096193e83ca7`  
		Last Modified: Wed, 03 May 2023 22:02:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba9b33e9316a950f2ca0db084e17331cca39064c3a3d10175a5732482915e1c`  
		Last Modified: Wed, 03 May 2023 22:03:02 GMT  
		Size: 239.3 MB (239262397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f679b704b1a974ebf77923991309e3935a8e4e5950043f8e8df9817cb566018`  
		Last Modified: Wed, 03 May 2023 22:02:32 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1e368f04c44fb0167ff47d43b10fd721c254e2e52f39cf02a2f8e1c9d20bc3ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244600123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0841f2fb87cc10cf6793954ab95d56fde855f4a16509c5a9e94ae9ed297fc522`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:32:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:32:30 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 May 2023 18:32:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 May 2023 18:32:32 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 18:32:32 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 May 2023 18:32:32 GMT
ENV ROS_DISTRO=noetic
# Wed, 03 May 2023 18:33:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:33:54 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 May 2023 18:33:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 May 2023 18:33:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f4b1b3aff79daeba459c24d6625912443a9c4b6e072fd443df8cf1fe609a3b`  
		Last Modified: Wed, 03 May 2023 18:59:14 GMT  
		Size: 10.9 MB (10902746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3bd0f1f3ef8032558026a60ca367a9d7b0a28a5d5656befe67922b145ce30bf`  
		Last Modified: Wed, 03 May 2023 18:59:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ffa192fc268fe17d966f4b3cea0d44a2889b03c6266a5d26e16c239241f65e`  
		Last Modified: Wed, 03 May 2023 18:59:13 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66412823f7f9778ca86e89b006f993392e02d4dcf6d72bececff2961ab62e97`  
		Last Modified: Wed, 03 May 2023 18:59:49 GMT  
		Size: 184.5 MB (184456335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2220fcae6736a0fef7e49e980a9743d78ac71f0793d181838e243ca8df2e17b7`  
		Last Modified: Wed, 03 May 2023 18:59:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

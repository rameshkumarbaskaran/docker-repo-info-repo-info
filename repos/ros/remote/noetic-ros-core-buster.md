## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:87327704e430994f17f27447fede890ed0037fc583faeaa2d6b3427f13d65bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:0dbe7d810340fe7fa6072129c78fd9d1a32386b19a1517df9ff01c8a0a2b1c91
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300501700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f03347c1adb7f729c36849dde2946d9eae4e9159a105815ced441101e07e02`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:36 GMT
ADD file:2f32dd3ef1e51a4d2d6dcf55fbf766434df5b3ada802b087d5761f2fa0cdebf5 in / 
# Thu, 23 Jun 2022 00:20:36 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 12:48:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 12:48:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 23 Jun 2022 12:48:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 23 Jun 2022 12:48:09 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 12:48:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 Jun 2022 12:48:09 GMT
ENV ROS_DISTRO=noetic
# Thu, 23 Jun 2022 12:49:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:38:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 23:38:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 23:38:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ea267e4631a981caf2841a7e9a1faf29cef9d020c4378fc64845802d17586531`  
		Last Modified: Thu, 23 Jun 2022 00:25:38 GMT  
		Size: 50.4 MB (50440811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d614310471c61e4200046b8f7adea9e8513871ad4fde9b669e49cafd656bde2`  
		Last Modified: Thu, 23 Jun 2022 12:53:58 GMT  
		Size: 10.9 MB (10892280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c90706f4c8a053c5c76e44d43756ced985189146b36ac63497e25ceceefc5c5`  
		Last Modified: Thu, 23 Jun 2022 12:53:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832307bf10c44d39b4524638f32d96d980cbea1925cc229df4ca7c97c3d08e81`  
		Last Modified: Thu, 23 Jun 2022 12:53:57 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09580d323567b8cc4622a787e2540c618939571a6ba340dd72e42597029cbba5`  
		Last Modified: Thu, 23 Jun 2022 12:54:29 GMT  
		Size: 239.2 MB (239166199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39dada285349dd73a05a5efcc9f7a78ece2b4d3f8af94032d497caeef5a9f16`  
		Last Modified: Tue, 12 Jul 2022 00:04:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:84f96828f39aee595f8614d70466b274a0ed49dab231f8804b068ede598aa4fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244293545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debf14ac309c743939181156899aa2cfbec1a71008241693dca29b060dd1a6ad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:46 GMT
ADD file:ea39534c5e9a548d7938f6b0e2459383caaf3906f3cc5eafe8bf66053b19f2d5 in / 
# Tue, 12 Jul 2022 00:40:47 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 13:00:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 13:00:48 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 12 Jul 2022 13:00:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 12 Jul 2022 13:00:51 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 13:00:52 GMT
ENV LC_ALL=C.UTF-8
# Tue, 12 Jul 2022 13:00:53 GMT
ENV ROS_DISTRO=noetic
# Tue, 12 Jul 2022 13:02:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 13:02:13 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 12 Jul 2022 13:02:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 12 Jul 2022 13:02:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:891a1587d3644a8b4b6dab3726ef380a725a0e19bfbf0eac02a275f711985862`  
		Last Modified: Tue, 12 Jul 2022 00:46:46 GMT  
		Size: 49.2 MB (49228928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9d4034dfbab9d3d5107231bf79f7e9128aa4489cba93d97578d760166fe3e6`  
		Last Modified: Tue, 12 Jul 2022 13:09:17 GMT  
		Size: 10.7 MB (10689263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0120a667e47e68ebbd4a03de6b0932ea25a0078d49f8ee71a75c9ebc31fbeef`  
		Last Modified: Tue, 12 Jul 2022 13:09:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c0820f1a42597e95311859510855953092a4ac35c4d590417693b084968c31`  
		Last Modified: Tue, 12 Jul 2022 13:09:16 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66081e680fda062b62d547ed9e29d0766f71a29d7a5fafb291a118efb1d184b`  
		Last Modified: Tue, 12 Jul 2022 13:09:46 GMT  
		Size: 184.4 MB (184372986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b195084a0c638927568ddb99e45b6b5b0c4d9994a11d7938842a8d3a60a9a1c`  
		Last Modified: Tue, 12 Jul 2022 13:09:16 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

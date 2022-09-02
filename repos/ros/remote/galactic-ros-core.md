## `ros:galactic-ros-core`

```console
$ docker pull ros@sha256:78e187b7198b30bf74a3763de70a1f6b9060d19129ffcf3dcaed0d85578fbb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:103d58131043fe218f9fb1aeb8c1110d81005458d71000f117bb7219f62fad6d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139168012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dbd16d87b5a79f30e898cd6e666e9491ca7ee7a46ac3a074a0f236c4b8c699`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:44:56 GMT
ENV ROS_DISTRO=galactic
# Fri, 02 Sep 2022 04:45:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:45:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:45:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:45:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4606a5228ccb52337657838c69716d528a1cd36a6adb320134ad9f72dac1b0`  
		Last Modified: Fri, 02 Sep 2022 05:10:57 GMT  
		Size: 103.9 MB (103882165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1077970b7ff447bda164171d709fbff427233431a1b4e67f2c042babb86581d`  
		Last Modified: Fri, 02 Sep 2022 05:10:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d188c2c8fa40b0a33ea208fdfa152bc426266ed2bb7206b4a1cdc951f93f4506
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134002148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e49fda94cfbb24093edc051b459c556171662bdd4b4a1a5157bc9ceb1dfba1f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

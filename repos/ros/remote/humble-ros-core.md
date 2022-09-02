## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:b85a352e7f40139d3291a0a0bf83821fd971bf54e3d224b087fc3b1d46f902b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:9563bfd3172e8574e1715fcb30492c30b83fb2df3cf85d3ea29cc7057654b280
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141622125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ff91d7a0709c149df8e6061c129ad8b19cad65d1d90d21a7c4dd39918822a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV ROS_DISTRO=humble
# Fri, 02 Sep 2022 04:49:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:49:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:49:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:49:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3dbe0ec1046bb9bdd0276165d66b03aafb64279b2077b7fbdac5b1047b98e`  
		Last Modified: Fri, 02 Sep 2022 05:12:12 GMT  
		Size: 106.2 MB (106189810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5ef6ac4127ac4c6d2c35e9befe4af09debd87c5e55110651f46e88a35c631`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:13bf1b82f69a790ce0598ce60a1ab623d7d674831da3ae908b07b894293296e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137062381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a82769945152d9b284ed53731acfa50b3c4d02b968684c2b23e18ba2cde644`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

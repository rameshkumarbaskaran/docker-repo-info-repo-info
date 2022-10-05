## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:0744aa6cb44884826ce5328e47753950252b9e892d94ecf1282e52d6b8669330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:13a54ab3b90b8524851f56c52c0461be93b2f50efe05f107fe5da4376ab86df7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141809056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af6195cf9e62a94108f0efd3276f5333cf3f15a9d422cad76afb79575e01a0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:20 GMT
ADD file:6cd2e13356aa5339c1f2abd3c210a52f6ed74fae05cd61aa09f37b6a4764f65c in / 
# Tue, 04 Oct 2022 23:35:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 10:30:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:30:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:30:33 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 10:30:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 10:30:34 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 10:30:34 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 10:42:22 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Oct 2022 10:43:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:43:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 10:43:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 10:43:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf92e523b49ea3d1fae59f5f082437a5f96c244fda6697995920142ff31d59cf`  
		Last Modified: Tue, 04 Oct 2022 03:04:01 GMT  
		Size: 30.4 MB (30428928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a657ed4bbca2b6e38d245b68fa4e7d8cb04af5f8ce38c735e74ff1efd995ddd2`  
		Last Modified: Wed, 05 Oct 2022 10:57:47 GMT  
		Size: 1.2 MB (1176207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace20a5ecec201be10011eb11e7db7eb3e16a30b7920fb10c049af041ad5ae8f`  
		Last Modified: Wed, 05 Oct 2022 10:57:46 GMT  
		Size: 3.8 MB (3827905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d795fabe79c02ef1562fee456701ad431e78c468d6b007d9022f0ee8f59d1f2`  
		Last Modified: Wed, 05 Oct 2022 10:57:45 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce660d1b5501b0f6b681547a1cc5bea2b0b3e273fa38be01bd5cd9e602edcea`  
		Last Modified: Wed, 05 Oct 2022 10:57:45 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596e5f6e471571a79c07d753e166119b42b7dffc65e8eb51a2519d6184e69ecb`  
		Last Modified: Wed, 05 Oct 2022 11:00:52 GMT  
		Size: 106.4 MB (106373598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd5b83de457e8bad7d32198416bef6f3825171761f6f4e27df9a095e38360f0`  
		Last Modified: Wed, 05 Oct 2022 11:00:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b17fedbb473fb50f4e28ae046b8a279b6c7219b56300afc94bf4f24224eb4640
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137036700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8302d02ce0698a6abda67eeeeb5c09dde3e47a0326483c19f08f3993f1ed40ee`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:51 GMT
ADD file:550e7da19f5f7cef52c6ea160a33daa482f44df086ddecffca8ec9be6385b848 in / 
# Fri, 02 Sep 2022 00:57:52 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 06:15:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:15:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:15:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 06:15:57 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 06:15:58 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 06:15:59 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 06:20:47 GMT
ENV ROS_DISTRO=rolling
# Fri, 02 Sep 2022 06:21:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:21:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 06:21:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 06:21:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:00f50047d6061c27e70588a5aab89adada756e87d782a6c6bd08b4139eb8ea10`  
		Last Modified: Fri, 02 Sep 2022 00:59:40 GMT  
		Size: 28.4 MB (28381340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81e8a90c277865b9fe52db2db44bfadc7b4a5b90c6e35f9ff56b0949e79f9a9`  
		Last Modified: Fri, 02 Sep 2022 06:34:29 GMT  
		Size: 1.2 MB (1177947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d06c25b67bbbdda5958c2b397a6a9868ac31ba8a8adf79f16a867441aaf6339`  
		Last Modified: Fri, 02 Sep 2022 06:34:27 GMT  
		Size: 3.6 MB (3594798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ae3c2eb3de8889d4850076f921c47d4392ed652c6c949e8bbd1934fa565a93`  
		Last Modified: Fri, 02 Sep 2022 06:34:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755bc2feb97c1316b5973891dbae4001df11b9f157554abbfac9b81d446cbd52`  
		Last Modified: Fri, 02 Sep 2022 06:34:26 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57709850deb7ebb6da7e7913dd7f347b87d4aff6128c1297029b1764763a4c43`  
		Last Modified: Fri, 02 Sep 2022 06:37:27 GMT  
		Size: 103.9 MB (103880245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba67b53a682dfe82f8a87e67d34d26e3a50eacc3e0bf38649a8b67d96c7e03ea`  
		Last Modified: Fri, 02 Sep 2022 06:37:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

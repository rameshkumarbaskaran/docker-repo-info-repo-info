## `ros:foxy-ros-core-focal`

```console
$ docker pull ros@sha256:edc931ade9f76b6a2063657b3957441f372edfeebb15ba782c2eabab98e63e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:47bbdada6ec4dbc2f19ed702bcbd8916a26f8964a2c25790dd65668cfb939d27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155701113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7ee85a49e46466a088fa050f4373b9accb131b1b137c3650e9919ecd67d036`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 10:02:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:02:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:22:08 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 10:22:10 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 10:22:10 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 10:22:10 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 10:22:10 GMT
ENV ROS_DISTRO=foxy
# Wed, 05 Oct 2022 10:24:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:24:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 10:24:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 10:24:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db398de1191a2231a78b6d5d54baa0f980aa763df67adb3394a7269111109671`  
		Last Modified: Wed, 05 Oct 2022 10:50:03 GMT  
		Size: 1.2 MB (1163849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d2c75c8d50e5aa3470df0fc55d0148e41867398126d721472b626f05229661`  
		Last Modified: Wed, 05 Oct 2022 10:50:01 GMT  
		Size: 5.5 MB (5546788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62dae53f0e9e7911f61e2af662dfc6c10a32cd5717c41369e1316e320c64345`  
		Last Modified: Wed, 05 Oct 2022 10:55:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01c1f05f8d44c933ce4daf7979f608925683f5ab3dd0b86b37b69af0df974d2`  
		Last Modified: Wed, 05 Oct 2022 10:55:12 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f51876d6577a35c5e59f0be2aaf21be35ae0ccc2ae98272ff4fdc2a4710942e`  
		Last Modified: Wed, 05 Oct 2022 10:55:32 GMT  
		Size: 120.4 MB (120413613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f290f8a7da3fe7da67791a679b225fdfbea4a063f69014d0cc798b572a00606`  
		Last Modified: Wed, 05 Oct 2022 10:55:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7f9005dd7ebcdadf141323e4565fabc2cb83540712209e98ddb71eebefb729c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137949484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ef402b59da714c63118e97bdf771216fbd936d7092d7468eefe82c5d598ba3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 06:04:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:04:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:09:20 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 06:09:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 06:09:23 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 06:09:24 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 06:09:25 GMT
ENV ROS_DISTRO=foxy
# Fri, 02 Sep 2022 06:10:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:10:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 06:10:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 06:10:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6679da592cfdf550fcdc4b85e065118bc5d71a57534760b4abedb490355889fa`  
		Last Modified: Fri, 02 Sep 2022 06:29:12 GMT  
		Size: 1.2 MB (1165138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5eb560b76837a662c9463136466570590371e820399defb1c9bc087709ea18`  
		Last Modified: Fri, 02 Sep 2022 06:29:11 GMT  
		Size: 5.3 MB (5323438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326b3ae8b95a7a2d08be20d992070269ef1ad4349f2d337fedfab469b6943e72`  
		Last Modified: Fri, 02 Sep 2022 06:31:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930dd26a6d335c1bf1f6cde29714b2fab3f457e05a2adc40b520764ea272ee7a`  
		Last Modified: Fri, 02 Sep 2022 06:31:50 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6669566fcc115df3d85e1176e7e645889db7959d6a954ba485ed11367dc9863a`  
		Last Modified: Fri, 02 Sep 2022 06:32:07 GMT  
		Size: 104.3 MB (104266721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d0c7829bec3aa8e600c8677d001a505e7a97ce46e7e8d34a667fa41b38b06a`  
		Last Modified: Fri, 02 Sep 2022 06:31:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:dcdcf0a78d356f6c9e521fd141cc4beab8a2db838a1a584257490088f5ba35ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:916ccdc4fb015c163586431e403398e9bbfc9f2826111e325cd004ada298fcb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 MB (349058814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c142f83d4bb74d1974a95aed03499ef4f432ebe1986c774237a7dd27127d3483`
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
# Wed, 05 Oct 2022 10:24:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:25:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 10:25:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 10:25:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:25:55 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 10:25:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 10:25:56 GMT
ENV ROS1_DISTRO=noetic
# Wed, 05 Oct 2022 10:25:56 GMT
ENV ROS2_DISTRO=foxy
# Wed, 05 Oct 2022 10:27:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:27:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:27:18 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
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
	-	`sha256:3bed5d7de950633b22457faefa5a82b47b766d96c02665e4faf86d9b7ebe9703`  
		Last Modified: Wed, 05 Oct 2022 10:55:53 GMT  
		Size: 73.3 MB (73322093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e37e53cfffae15445cfdce1b4b7ef7cea4b3e153ea7abf8cd18ebf02b77e34`  
		Last Modified: Wed, 05 Oct 2022 10:55:42 GMT  
		Size: 267.4 KB (267375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677b37769ea581ebd1d2e907d8c68c8a2c4f7920ce4e81e0099e4165a54aca77`  
		Last Modified: Wed, 05 Oct 2022 10:55:42 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216bc94919c7136aa052456840629454991399309eea61f5b2f7b34471de467c`  
		Last Modified: Wed, 05 Oct 2022 10:55:45 GMT  
		Size: 21.7 MB (21663849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d94baadca69524a33d3ca807ea019bbad1438b2b7217b4e86ba0e93367003`  
		Last Modified: Wed, 05 Oct 2022 10:56:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccc523540c72f37ce74bb0e501bd649759b2c7dfcb655447fac8913c1517dee`  
		Last Modified: Wed, 05 Oct 2022 10:56:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30e1cb5bcf08c41cd9a4d2e6fe7eaf091057e629ff6f04e3d14c40db29b0048`  
		Last Modified: Wed, 05 Oct 2022 10:56:20 GMT  
		Size: 76.4 MB (76429483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb854b70cf802670e97b4d6ccb7d054bba536f3eb14a57315543c577468c56e`  
		Last Modified: Wed, 05 Oct 2022 10:56:10 GMT  
		Size: 21.7 MB (21671851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dda7b30665fed39bcf488e91c73c1165eea1cd815014048c13330d18959877`  
		Last Modified: Wed, 05 Oct 2022 10:56:06 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2aae4ed32137ebeef84ed5c1fb571d1130ea4aef9fd955ca09e50f31dfc6326a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.4 MB (316402985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deecf343d9441be7dd5f7f4e27af589e8f2af1c72feb0775c5e2f462e90e848f`
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
# Fri, 02 Sep 2022 06:10:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:10:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 06:11:05 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 06:11:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:11:34 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 06:11:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 06:11:38 GMT
ENV ROS1_DISTRO=noetic
# Fri, 02 Sep 2022 06:11:39 GMT
ENV ROS2_DISTRO=foxy
# Fri, 02 Sep 2022 06:12:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Sep 2022 19:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Sep 2022 19:05:19 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
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
	-	`sha256:ec5f8d617cb17da8504e284767c00fc2feed07e2f35c7a7b4313b804d53e56b8`  
		Last Modified: Fri, 02 Sep 2022 06:32:28 GMT  
		Size: 67.4 MB (67449113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6935c838d5eb4cd0b713a76063e82036a165b8bc62634dec158e4729749a38`  
		Last Modified: Fri, 02 Sep 2022 06:32:18 GMT  
		Size: 262.7 KB (262739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f707611d281f0c907bf51272891d4009de29c408cf77e296e33d8b7dc31983b3`  
		Last Modified: Fri, 02 Sep 2022 06:32:18 GMT  
		Size: 2.4 KB (2378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985a2c9bbb7d25390f08e6efb8200c4a037a6c8bd6980b91e33212c2d3378a6d`  
		Last Modified: Fri, 02 Sep 2022 06:32:21 GMT  
		Size: 20.4 MB (20366833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af4cff9d793717a3b0b2b2160532e7259e9405b855066328b8b9598efd67ee1`  
		Last Modified: Fri, 02 Sep 2022 06:32:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4504cdf7ed57b671e8d8daec007271bb91637e5b2096e97548c9477c5d6c136c`  
		Last Modified: Fri, 02 Sep 2022 06:32:57 GMT  
		Size: 76.3 MB (76272363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9e3a5fcc9fb676a59a0869e49e77e55c8a8c438e9734c2bf6a146128223188`  
		Last Modified: Fri, 30 Sep 2022 19:07:56 GMT  
		Size: 14.1 MB (14099602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47403f1e8c6016ef023fadd7d95a9ccfe4cb67cc7ec15170b7fe9b9363e5c6d4`  
		Last Modified: Fri, 30 Sep 2022 19:07:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

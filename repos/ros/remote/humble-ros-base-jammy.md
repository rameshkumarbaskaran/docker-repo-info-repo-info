## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:e7bf15870b85c499ffebbb0e5e7fc733b9d6ac8ebd506cf90a8feb24e455a1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:fdf2d8cc92e72e6052aa63633e09ce09bcc03e9ef0a65d5e9df7f16590e43a56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262801720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0caff7409322c718dbd0b7a41890bf399cc025ce752ce5f0d3c200cec6a66d8a`
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
# Wed, 05 Oct 2022 10:30:34 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Oct 2022 10:32:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:32:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 10:32:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 10:32:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 10:33:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:33:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 10:33:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 10:34:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:f95ff840521c5abed0b7ee2eb74488a50f38a6639eb95a973054a41d0fa4eb98`  
		Last Modified: Wed, 05 Oct 2022 10:58:02 GMT  
		Size: 106.2 MB (106210386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcc82456ade47aabed8266e54a40aa857a47f06099009e7410d9f1a8462436f`  
		Last Modified: Wed, 05 Oct 2022 10:57:45 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029b0929144e1fbf7711875151abd541f900c4585b654005cb2f30f7c7868386`  
		Last Modified: Wed, 05 Oct 2022 10:58:27 GMT  
		Size: 97.9 MB (97851596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34dd89c6f6c80b4bc94a816c40e961d447dd97ed548e5bcdd9acbc88324dbda`  
		Last Modified: Wed, 05 Oct 2022 10:58:12 GMT  
		Size: 293.4 KB (293380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d56e31efd937f3db1aa9ed649784bf002d8082e7b4521dea01a898299485e44`  
		Last Modified: Wed, 05 Oct 2022 10:58:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5c96f9d9f9a99d848a73ea8e509d25fd737ec31111b3fb98d55502de9f0dd5`  
		Last Modified: Wed, 05 Oct 2022 10:58:15 GMT  
		Size: 23.0 MB (23008452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b52db8801d9e46e66e2f1b84031e242bd5f8c85d836c9ee80ae69bcb98b9e4a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255055044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97fa8fa54f8dd58526781db889c6bd8e5ee3e784971669964178b5512fcdb32`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:55:19 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Oct 2022 13:56:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:56:17 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:56:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:56:19 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:57:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:57:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:57:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:57:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77135164a4ca214d5baefbf18732e85e199d498ecc59003672487d9c648b74`  
		Last Modified: Wed, 05 Oct 2022 14:16:58 GMT  
		Size: 104.0 MB (103957828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6965bb2d35a3d18ae4266c452f2a47be3cc9d2dba39a969448e52ad4b37a5b3`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce2c8431570b35ece0db3a51d240fe2781ad038af3c8da3b55b03b4fe8de8ac`  
		Last Modified: Wed, 05 Oct 2022 14:17:22 GMT  
		Size: 95.2 MB (95215132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f80f204207eef3b331605f2054caba003953f6e525e487fe268099461c7eef`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 293.3 KB (293326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44490e7bf336a1cd0e4bbdfc0cb509173c0643c5572dea249d5900bd9121742a`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 2.4 KB (2382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d44d5787adf5963e3ae22a342cafe9f33a160f2cc03b123c4d6996867e0535`  
		Last Modified: Wed, 05 Oct 2022 14:17:12 GMT  
		Size: 22.4 MB (22428695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

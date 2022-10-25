## `ros:humble-perception`

```console
$ docker pull ros@sha256:777725e051baea3119caa2479f38e77f904e54814fc2a463b4f76bdefdd00975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:76645b46dcf6ffbf3fdac6944597995377c4640b15b343bdb7f223d323b81e1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1087032972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ae91661e2cf574b08b75a61ebef5b0786b5a33c59bdab811b81be7e84e98dd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811c764114f804d6bc0acc7e66e888ceacf4c5537574a5de8c4d40fb90c9999e`  
		Last Modified: Tue, 25 Oct 2022 08:05:05 GMT  
		Size: 824.2 MB (824187861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8d33b1eda15a566ef8d7f32e8d9def7e1da4c9bf71d80e0d9ce5495a9737f625
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1036772436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d72876cd51856f6c06f3479fae29de0e96685b3944854f72e4e39bc6c90566a`
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
# Wed, 05 Oct 2022 14:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:bc3bcbbe799e24821f61a98ab3360ded019455e6da2828098c9b7ed7d6f5a5d9`  
		Last Modified: Wed, 05 Oct 2022 14:19:54 GMT  
		Size: 781.7 MB (781717392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

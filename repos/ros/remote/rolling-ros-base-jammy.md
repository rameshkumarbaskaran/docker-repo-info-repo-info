## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:100afa8d605fdd232638c325f38ddb6d31c3ec2758e56f71b51192baf4b751f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:44bdbd819383462c025ea361c9c8427375ba5c38201356b93c5827ae7b1ebf8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263221662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef1ef5ce96f4a5c4ee7e03559ae7c8da886e0ac2f52a705eb33428dce931`
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
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:46:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:46:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:46:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:46:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb38b610c9d923dbe6bbe532a0559a4064856d0105bf842e52ce1ad4ff11e8b`  
		Last Modified: Tue, 25 Oct 2022 08:05:58 GMT  
		Size: 97.9 MB (97879015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faad8ca67596a7af7c25ade2313bccb1e13db2a2646e408a7171bdcce0e48b6`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 289.2 KB (289222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4659981956310c677c0249ba2e2eba19ae8b8670034f1b14176d899fde8b0`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af086c324a03d7da5c2309c2b4691d12e9153d09eb5464a8a4442fa3a8c24ae`  
		Last Modified: Tue, 25 Oct 2022 08:05:49 GMT  
		Size: 23.2 MB (23226799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:33669f7bf08ec323d17bd2d63532f30fe9982bbb13f7cf849dd97b000c8a1827
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255407846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0b50bb3221f9dcf4ace9413a489fa328657908bfeada9464bac70440cca785`
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
# Wed, 05 Oct 2022 14:00:21 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Oct 2022 14:01:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:08 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 14:01:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 14:01:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:01:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 14:01:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 14:02:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:3834504b668bb13d4fcded46b2444690bed0603eccbb71ffd03d0ab432593c8e`  
		Last Modified: Wed, 05 Oct 2022 14:20:23 GMT  
		Size: 104.1 MB (104103500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ce9b251482e03203dd3f2b75f07f06ff803e68b582e12a53ce6cc1028c9c58`  
		Last Modified: Wed, 05 Oct 2022 14:20:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2767f80cc9b7f92921da87e086a643d8d80b257ce273716d8795816f765216`  
		Last Modified: Wed, 05 Oct 2022 14:20:48 GMT  
		Size: 95.2 MB (95215484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1c34644006693e54ff50141efeaec2467a06586f1f28d4e4874485d96ad999`  
		Last Modified: Wed, 05 Oct 2022 14:20:35 GMT  
		Size: 287.8 KB (287799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9377d158c53ca57fb20de69f4e1e1f1bb1741c856365104a808553e58c611ecc`  
		Last Modified: Wed, 05 Oct 2022 14:20:35 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f3f8b1a658efb974ec2a2c92261fc0ca9d5ad9d4eecf003b8752e7b82ab271`  
		Last Modified: Wed, 05 Oct 2022 14:20:38 GMT  
		Size: 22.6 MB (22641030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

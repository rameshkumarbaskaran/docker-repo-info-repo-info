## `ros:rolling-perception-jammy`

```console
$ docker pull ros@sha256:dcaaaa3353d40019c34a6311cb6309971b5ebbdaee007a9a2c5c7bdf948c4da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:e92add0853cca3d90353b7c3ba02856c8fa37ecb63bfc3d8bc2539575ee03eea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1087993863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f0831d37aba9bc5d9342e34dcf4211ee421e0c3ad4187b266805c064b550f0`
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
# Wed, 05 Oct 2022 10:43:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:43:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 10:43:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 10:43:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:46:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1ab1a884c0500e4a2eccb5a2a364d8d1cdc8c80689d7292e492c144c4dee8f69`  
		Last Modified: Wed, 05 Oct 2022 11:01:16 GMT  
		Size: 97.9 MB (97851974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420841bcfe85d95f042c1930c98a9f177ba6b518fc1c10bd66c341017785ccf5`  
		Last Modified: Wed, 05 Oct 2022 11:01:02 GMT  
		Size: 287.9 KB (287858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4896c641876dd5da58d9cd9d3b9c73d0a464a3dcb760e5efa747239c51261735`  
		Last Modified: Wed, 05 Oct 2022 11:01:02 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5b4eca3f72bccb69be61064fc7d85e752e7d5c0d0cf14b71a6fe5dea6feb8c`  
		Last Modified: Wed, 05 Oct 2022 11:01:06 GMT  
		Size: 23.2 MB (23226838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c89eceebff238f8a817010c80116db9da5db72367acbeed110da2b63ce962ee`  
		Last Modified: Wed, 05 Oct 2022 11:03:07 GMT  
		Size: 824.8 MB (824815681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:78be1143dc94dd563150a00555027432042e7bf6add3629226596a7999011f96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1037757233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9ba2abd3234b7b99a4632f3b505eb02d7129973d39e19be1d45f31ae01566e`
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
# Wed, 05 Oct 2022 14:04:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:f4de81c13532f2a3ae50f8a84d32f7fbe4788fc88103638857e208cc54f63ef1`  
		Last Modified: Wed, 05 Oct 2022 14:22:40 GMT  
		Size: 782.3 MB (782349387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

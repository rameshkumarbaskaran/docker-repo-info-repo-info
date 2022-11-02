## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:09462aee0815a4e78b9b755769d805e2f999b5d94e6aad4a958dfa1859627894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:300f09c7c4c4922805309d27bf9ce31cce8c69de2d4b5b5fe89a781fcdd65a2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141822657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe26daf1d7246d5e5a14976e6508af0276c90382fbef5b92acfa3905df1100`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:07:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:07:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:07:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 02 Nov 2022 19:07:15 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Nov 2022 19:07:15 GMT
ENV LANG=C.UTF-8
# Wed, 02 Nov 2022 19:07:15 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Nov 2022 19:19:39 GMT
ENV ROS_DISTRO=rolling
# Wed, 02 Nov 2022 19:20:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:20:21 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 02 Nov 2022 19:20:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Nov 2022 19:20:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0e309791760cb897f78d6ecdca3ecfa35842379a8f68578fae97e3ed231487`  
		Last Modified: Wed, 02 Nov 2022 19:24:38 GMT  
		Size: 1.2 MB (1174801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda1968667a68200295ab81fbbe7a340eefffe28e7765ccce0ac08e4e840058f`  
		Last Modified: Wed, 02 Nov 2022 19:24:35 GMT  
		Size: 3.8 MB (3828037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80ba109583179b86f91d9cef7488e67ac530a78c620ebe127cde962b001e8bf`  
		Last Modified: Wed, 02 Nov 2022 19:24:35 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00beac66efa2733f4c56752491978562f4fd073a619736ec1ee66f17d44324c7`  
		Last Modified: Wed, 02 Nov 2022 19:24:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11614817332af0948a51dccc0ac2fec8909f110de95b78985b29b8c3f7e970c1`  
		Last Modified: Wed, 02 Nov 2022 19:27:43 GMT  
		Size: 106.4 MB (106391794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fa3a122b2ab87848b5d17fb2971645d70a05f26186dd83469908b5fc2782c9`  
		Last Modified: Wed, 02 Nov 2022 19:27:26 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2fa82fc9712adf8939173b6b69926b5de8f62637b57115f0089595207ddeaae6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137484035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ce525d434486e5df407554c6885b5814dfade488b61e23111b16235fa6d910`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:21:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:21:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:21:31 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 02 Nov 2022 19:21:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Nov 2022 19:21:33 GMT
ENV LANG=C.UTF-8
# Wed, 02 Nov 2022 19:21:33 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Nov 2022 19:35:10 GMT
ENV ROS_DISTRO=rolling
# Wed, 02 Nov 2022 19:35:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:35:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 02 Nov 2022 19:35:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Nov 2022 19:35:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11760287344b02d03930af87d27c6b9dc1acc8842adc4df018fbc979edafe07e`  
		Last Modified: Wed, 02 Nov 2022 19:39:41 GMT  
		Size: 1.2 MB (1175024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57286bbac2dc9c1c64117272c5610b0ccabf76c64c0d83ada53661e5bd6c7235`  
		Last Modified: Wed, 02 Nov 2022 19:39:38 GMT  
		Size: 3.8 MB (3799957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe77194dbcb3cb1b9324930f565438ef05948cba7bb01a453e85a976f50cb1f`  
		Last Modified: Wed, 02 Nov 2022 19:39:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeeadbd7d6fc1cd7ec48cf66192a01ee8304012593c12a1aaa6934e051205a1`  
		Last Modified: Wed, 02 Nov 2022 19:39:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe01c46c01bb82aca483b1c908f1f744fbf5f514d7bc29127dc2d13c92c43fd`  
		Last Modified: Wed, 02 Nov 2022 19:42:12 GMT  
		Size: 104.1 MB (104124486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b03d2faf31fcaa3607b8d6642d0d7aebc0c888fc741c6b7477337a853bbe199`  
		Last Modified: Wed, 02 Nov 2022 19:41:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

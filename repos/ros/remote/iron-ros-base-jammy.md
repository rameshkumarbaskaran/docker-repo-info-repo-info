## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:1324764690fc87b7e75cee69b55ddfdf35031a6cf6ded8147b7ea0a80d28fc9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:49326bbc8f3ecc1802a595387200d1e9fdb7b940c955e6db0ebd496545d4ec78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.9 MB (270851839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343486d1e5d51609c0590e37e174e7f2277ffc1fe9a978fa4ad59843a9ceb2fb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 21:45:33 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:45:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:45:39 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 03 May 2023 21:45:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 May 2023 21:45:41 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 21:45:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 17:25:50 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 17:29:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 31 May 2023 17:29:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 31 May 2023 17:29:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 17:29:11 GMT
CMD ["bash"]
# Wed, 31 May 2023 17:31:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 31 May 2023 17:31:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 31 May 2023 17:31:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 31 May 2023 17:32:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d709c34b032e9c25f3ef7dbc9cc5be0ab87d014082e04d1f4a5d20e2970446b`  
		Last Modified: Wed, 03 May 2023 22:04:52 GMT  
		Size: 1.2 MB (1239802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58a8c29b4dfa9054fe01f5590245b9ad2e27c309027d00b628451f55bfde59c`  
		Last Modified: Wed, 03 May 2023 22:04:50 GMT  
		Size: 3.8 MB (3828401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707c946d99b6f2ae4da84c6c0af0b3204f17c5371e0ef1e1968fc20d3c812123`  
		Last Modified: Wed, 03 May 2023 22:04:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89451566146a587c0f7bde9c5bd208af5e73072fa556ff6ad6ac85c213406cb6`  
		Last Modified: Wed, 03 May 2023 22:04:49 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c56b0611d6c6c3e22e553e0042ab39e3ed4b4214dc9230412e22704fba3d9fe5`  
		Last Modified: Wed, 31 May 2023 17:50:04 GMT  
		Size: 126.4 MB (126391882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70f0a0b21eca468b4344a7f6723cb2517bc5498bcacc3f6471b4399c426c23`  
		Last Modified: Wed, 31 May 2023 17:49:45 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458cca7ae6c5340ded5bc40b9c5754c979e95b9bbcf1a6fac4012a4fa2241388`  
		Last Modified: Wed, 31 May 2023 17:50:23 GMT  
		Size: 85.0 MB (84994423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadc7d5ad2be0481c06f145c9e5c04c276ef6420f7b2fc3bb14c19a3218df669`  
		Last Modified: Wed, 31 May 2023 17:50:13 GMT  
		Size: 289.8 KB (289753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26de6b401028247439e9d2b3580ad41edcdda3eb8a60e848988b2c2ce433e289`  
		Last Modified: Wed, 31 May 2023 17:50:13 GMT  
		Size: 2.4 KB (2426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d369c0325aa0a6d434fd266c9842fb045c457f0a30c0439a08bf17ac2321dac4`  
		Last Modified: Wed, 31 May 2023 17:50:16 GMT  
		Size: 23.7 MB (23672525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6db1f350aae0568226975d48003a5ac2416348f3ca8433c98b8f2bdffa7e01cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263200375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c815297ba4dc8cdfc9327117d0c94de80ca2025b91ee85c36f19fbdf0f494b37`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:19:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:20:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:20:18 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Jun 2023 00:20:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Jun 2023 00:20:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Jun 2023 00:20:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Jun 2023 00:34:03 GMT
ENV ROS_DISTRO=iron
# Fri, 02 Jun 2023 00:34:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:34:50 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Jun 2023 00:34:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Jun 2023 00:34:50 GMT
CMD ["bash"]
# Fri, 02 Jun 2023 00:35:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:35:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Jun 2023 00:35:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Jun 2023 00:35:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755c90e9cf79faad5cb53bf52c5426df1ff04c218894ffbb077e2524f6d717e2`  
		Last Modified: Fri, 02 Jun 2023 00:43:37 GMT  
		Size: 1.2 MB (1212932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35deec7a88f66396ce147c78c621f166491b3bb0d43295ac2a27879c9d37369e`  
		Last Modified: Fri, 02 Jun 2023 00:43:35 GMT  
		Size: 3.8 MB (3800450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ef7ef73bca581875e598a71ca009ce9fded1b1da4ce3b0c008979125eb05d7`  
		Last Modified: Fri, 02 Jun 2023 00:43:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037d33ca89bd5d376d834aebec1592a65631f40a1423a08a248d2b1c8df162c6`  
		Last Modified: Fri, 02 Jun 2023 00:43:34 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1b53e432c1aa39a1b9a2e0a202a4d9cba5d0556606ed966559e6119ec1bcfa`  
		Last Modified: Fri, 02 Jun 2023 00:46:08 GMT  
		Size: 123.7 MB (123701103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec255af92373156a6dd4f07f43fc82f9da1c835dd61eae48f88a923e11ad2e4e`  
		Last Modified: Fri, 02 Jun 2023 00:45:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca49b7450908e85e05e83a8562dca50d41c46c0f13653c59c1459e04abe33ee5`  
		Last Modified: Fri, 02 Jun 2023 00:46:24 GMT  
		Size: 82.7 MB (82735519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4258bbb676d02e9be047f40f277e61fc93ce81d232282a503cdf63e892a0f25`  
		Last Modified: Fri, 02 Jun 2023 00:46:16 GMT  
		Size: 290.2 KB (290205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96ba38249cd70d0d47d13965a7488081c5f69f23b7c01c208e9d1391b26fb74`  
		Last Modified: Fri, 02 Jun 2023 00:46:16 GMT  
		Size: 2.4 KB (2408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bf34622b2849dc4d94e66c206e80d56a2e1cb461aa21e0e0669baac2d023cf`  
		Last Modified: Fri, 02 Jun 2023 00:46:19 GMT  
		Size: 23.1 MB (23066303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

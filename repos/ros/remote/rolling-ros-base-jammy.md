## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:e262b4b58d7394cfe9e2dc49b36e9b985541f26f0fee78c40d4cfea0d4f2924b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:60f2a37f45af89cb5a543e58e191560ccc0da14b3ed1346578abc6873d702571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263707932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce213b690e983e6d1f65eec950595f8104e0b5a2a8c61823889ee8536220239`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:26 GMT
ADD file:76dd6cab5732b31272279bb8868954cbbecf591f596f0c318524454e95eabfb9 in / 
# Thu, 21 Apr 2022 23:00:26 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:42:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:42:45 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:42:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:42:46 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:42:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:42:46 GMT
ENV ROS_DISTRO=rolling
# Fri, 22 Apr 2022 03:44:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:44:24 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:44:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:44:24 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:45:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:45:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:45:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 22 Apr 2022 03:46:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8527c5f86ecc162d68a9d38c8f4c6a6443158c67417e8bc2c3cea9f3868394eb`  
		Last Modified: Thu, 21 Apr 2022 23:02:00 GMT  
		Size: 30.4 MB (30421209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341919f757e419f6142944f5ea95c19b61bf1ff648abdfff94ed8c99c0bfd52c`  
		Last Modified: Fri, 22 Apr 2022 03:55:07 GMT  
		Size: 1.2 MB (1191091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0455c8ef748e7b3e35f60511f8e8053ee76492c9a72a5afd00d55d351854556f`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 3.8 MB (3826746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b72761451ff916be9282f71adece9e357fc9710e86559b986d1f01583fd312`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3452459740e87b470a88f20122447689e1640a2b865eb50f2f4a866ad75d391`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2037c4fb46b3cec9022f679d45d7834d6c89ac325348efc7af3d5d92bcd7658`  
		Last Modified: Fri, 22 Apr 2022 03:55:22 GMT  
		Size: 106.4 MB (106381750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0221e7e4829eedc9594c53ce3492bccdc39ea2c1b77da83a10fdb689100c68`  
		Last Modified: Fri, 22 Apr 2022 03:55:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c7fbeb7e1d7385b2109f0df086ca744db3d917acd012c123fa8edc585a2080`  
		Last Modified: Fri, 22 Apr 2022 03:55:46 GMT  
		Size: 98.8 MB (98754384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b30b9dcc84973150cb0c195863fd24646a6ba41a76b5f0b33c806b25f12281c`  
		Last Modified: Fri, 22 Apr 2022 03:55:33 GMT  
		Size: 268.9 KB (268885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8e6a2755512e3269961eabe5ea4b4f1aec52de907316bb4f8654466d684b8a`  
		Last Modified: Fri, 22 Apr 2022 03:55:32 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba940d517ddac55ea1379c9f2cff56d93e8aa91f44e1303dc4a4261a1ef6810`  
		Last Modified: Fri, 22 Apr 2022 03:55:36 GMT  
		Size: 22.9 MB (22859264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d0e911a94a4c436c6eaac9f332755592ed90fe0be25b9af63f9a2f49ba05f158
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255862942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb412fe1d9860ee058814b5c7aaa792e3483edb85047600538597591910b5b63`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:52 GMT
ADD file:1e18e22e32f06a7e93275cf3a2eb2a1d3892be27628bdae2de4b2aadb992bd50 in / 
# Fri, 29 Apr 2022 22:49:53 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:26 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:32:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:32:29 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:32:30 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:32:31 GMT
ENV ROS_DISTRO=rolling
# Sat, 30 Apr 2022 00:33:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:19 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:33:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:33:21 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:34:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:34:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:34:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 30 Apr 2022 00:34:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b84950154c181a602d2e93b68e84660f96dc78f94ae36f3df2db8d5701abb6a5`  
		Last Modified: Fri, 29 Apr 2022 22:52:07 GMT  
		Size: 28.4 MB (28376457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4339dcf07e4fd919aa10dc0e01fb8f44184f74bf6baf5aef6e8fdd30f5e603`  
		Last Modified: Sat, 30 Apr 2022 00:43:58 GMT  
		Size: 1.2 MB (1192681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0db3fdf5b04e561797500fc1d19d79a37ca0586b71bee71ce2acaee153d4dee`  
		Last Modified: Sat, 30 Apr 2022 00:43:56 GMT  
		Size: 3.6 MB (3594435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af71d8cd404a31e077722270696cf33d59cff54d35c9dad864264138bc3ac`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e01b1250d40bc108a995e5fc6c1630b0abdbfff31529a87a4096271f2a6115`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ae3a3b720aed16343416b9bb5eea4967087c21dee2c39948d0ca129037dd4f`  
		Last Modified: Sat, 30 Apr 2022 00:44:12 GMT  
		Size: 103.8 MB (103773129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be65bd445679ba8af650c6dd6742dc9a2d31871d4bac42819d92857e3a5892d`  
		Last Modified: Sat, 30 Apr 2022 00:43:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ea6f66376f6e1da9bb78a2df21de836c30ea4379d4641ce9b7a1dfce84b6b4`  
		Last Modified: Sat, 30 Apr 2022 00:44:38 GMT  
		Size: 96.2 MB (96157476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a8f645f0a9603e60db84a3de8b50d76b5e58918fc81c2b4b19cea51a1a2a1`  
		Last Modified: Sat, 30 Apr 2022 00:44:24 GMT  
		Size: 269.8 KB (269758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773bf167794f3f7af31d32325c1d102af94787ef5a9d239074eafe9b5582dc75`  
		Last Modified: Sat, 30 Apr 2022 00:44:24 GMT  
		Size: 2.1 KB (2137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ab25ab23b7e441a52f03a15aec7da83f14b6f0843949bdbfee2aa35beb1787`  
		Last Modified: Sat, 30 Apr 2022 00:44:28 GMT  
		Size: 22.5 MB (22494500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

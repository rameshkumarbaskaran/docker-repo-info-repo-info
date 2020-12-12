## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:5bcb07c88c681353d7ad0d83ae563dd6b7141135ae0e3ccd23ec3d912afa6219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:ded61fde5f4d65506c7c25ef5601b61f7be384db7db3ebaf8b934554a35bfbf1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 MB (300209802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019b2a27930f1dbdb3cf1c358aac4842233e671468635fa07877b0fd1c0fd26e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:52 GMT
ADD file:6014cd9d7466825f80d4a3345847efd6fd7ef600b8135811cab4f0e304f66cd7 in / 
# Fri, 11 Dec 2020 02:05:52 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 19:38:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:38:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 11 Dec 2020 19:38:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 11 Dec 2020 19:38:33 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 19:38:33 GMT
ENV LC_ALL=C.UTF-8
# Fri, 11 Dec 2020 19:38:33 GMT
ENV ROS_DISTRO=noetic
# Fri, 11 Dec 2020 19:39:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:39:40 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 11 Dec 2020 19:39:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 11 Dec 2020 19:39:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6c33745f49b41daad28b7b192c447938452ea4de9fe8c7cc3edf1433b1366946`  
		Last Modified: Fri, 11 Dec 2020 02:12:07 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8976c0b6dafba8e29d428307d1a731a8cf6b1ebef7280ec00f1582e30d70e9bd`  
		Last Modified: Fri, 11 Dec 2020 19:48:43 GMT  
		Size: 10.9 MB (10890369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03728db810730c356cc4e6d117dbb856990d83d8b424404820b83e60d1c0a62f`  
		Last Modified: Fri, 11 Dec 2020 19:48:42 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c01b817549038fd01886fb541048dc802d51175b3d0280699ef1b4a2ce5826`  
		Last Modified: Fri, 11 Dec 2020 19:48:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a229b50b83602782324ede7d94e323985fd1bb2769db16f2cbf549387fd7fe41`  
		Last Modified: Fri, 11 Dec 2020 19:49:31 GMT  
		Size: 238.9 MB (238919867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86cd2429c18dcfca36b2d9dc7c45899f54bd706f389805d0ad288196ec67a94`  
		Last Modified: Fri, 11 Dec 2020 19:48:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8fc5a63cfb8e9777d2c94c0cab1c70027b788863d16ef7648872a51c231ef83e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244210979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc2d256194b2b1695bdbd420657b89a4a0221c2ae871caa923bd1afd18480c7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:23 GMT
ADD file:b08f373022952dba7d08b7fc02909d9e369c9727e0e4f62d6110e41e70e668cc in / 
# Fri, 11 Dec 2020 02:45:25 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 23:25:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 23:25:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 11 Dec 2020 23:25:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 11 Dec 2020 23:25:11 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 23:25:13 GMT
ENV LC_ALL=C.UTF-8
# Fri, 11 Dec 2020 23:25:14 GMT
ENV ROS_DISTRO=noetic
# Fri, 11 Dec 2020 23:27:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 23:27:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 11 Dec 2020 23:27:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 11 Dec 2020 23:27:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:99e5136f81cd2a8cc226c42435d6f4f30584d168cc51f4d4afd2d5611e4d2215`  
		Last Modified: Fri, 11 Dec 2020 02:52:45 GMT  
		Size: 49.2 MB (49180317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6802a596e847ecc40fc64a4020bce9c6b7ec241a9a0adff6a2f4b93c30b2144`  
		Last Modified: Fri, 11 Dec 2020 23:41:10 GMT  
		Size: 10.9 MB (10882958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d048a0e9c93d12fc2502ef2bd5aff74d265481bfe6a09ed85acc1b9d28d689`  
		Last Modified: Fri, 11 Dec 2020 23:41:07 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89503d24c7d28733c7447800ad677d2131c8d16d0a168ebb554b2b3daaf1a1f1`  
		Last Modified: Fri, 11 Dec 2020 23:41:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215ec51670c89e647b8382b61d566bad5238b2661b6575cae78036b6dbc1da44`  
		Last Modified: Fri, 11 Dec 2020 23:42:01 GMT  
		Size: 184.1 MB (184145865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f19aa0624291920427cd6503ba38ebd048f0d00f4e6f303a9893c73a1d212a`  
		Last Modified: Fri, 11 Dec 2020 23:41:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

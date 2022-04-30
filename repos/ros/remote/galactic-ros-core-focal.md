## `ros:galactic-ros-core-focal`

```console
$ docker pull ros@sha256:ec99a1f4552a6e073e072406131b25f6b3fd6b793626a909e4b6c1dadf5b54b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:c644630aa2cadfb39da6be16c872c066e583724bb601c338cd9f9bba235c12bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138958088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce7931771f1d143f583c2a02af3a0452f1f4abd91a6da08f4bdab2b99b69347`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:21:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:26:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:37:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 22 Apr 2022 03:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:37:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:40:00 GMT
ENV ROS_DISTRO=galactic
# Fri, 22 Apr 2022 03:40:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:40:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 22 Apr 2022 03:40:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:40:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ade01d9d7a3d8c0634326d89adaba6d97dd2884f45e985281ea88d141f73f`  
		Last Modified: Fri, 22 Apr 2022 02:33:12 GMT  
		Size: 1.2 MB (1180875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4624fbd86c08e579fe05e18065911602478ec2bdc1239e5b786f8b5515dc6e90`  
		Last Modified: Fri, 22 Apr 2022 03:49:39 GMT  
		Size: 5.5 MB (5546643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9020050231a832ea7ec08f8436054efcd6e8a4d4ff6650fa51af143b21e723`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0ad51f3ba74c73756f5c46e18fe955db3d8a6a7ea0457271430340cb811b85`  
		Last Modified: Fri, 22 Apr 2022 03:52:24 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a86987c94783b7f050791cd972e66bdcf20ee12dcccd1a0162756a9bbea3ff5`  
		Last Modified: Fri, 22 Apr 2022 03:54:05 GMT  
		Size: 103.7 MB (103662159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca3e7c02467d0b63472d97b71a8664755cfe96d8fe8c6842a7b4861910bc761`  
		Last Modified: Fri, 22 Apr 2022 03:53:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3ed6a9e83e2aa8bc98fc3a7fd76344b5bbe2185f77d65a86c46a9e8ce47e57e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133716329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8861d548374a54940b31d30055fa3ce4692be4ea9418ac6afd0e5bb342237f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:20:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:20:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:25:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 30 Apr 2022 00:25:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:25:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:25:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:29:05 GMT
ENV ROS_DISTRO=galactic
# Sat, 30 Apr 2022 00:29:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:29:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 30 Apr 2022 00:29:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:29:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2837428b54ca227343b28e2aebf5f943eb61317acb706203bbd53ccd36b1faa`  
		Last Modified: Sat, 30 Apr 2022 00:38:20 GMT  
		Size: 1.2 MB (1182149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782caaf301f52c6f48c207e662cbaff846f5e221ff2d301aa5123d59be9f9cdc`  
		Last Modified: Sat, 30 Apr 2022 00:38:18 GMT  
		Size: 5.3 MB (5321931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e518f0b96ea742e65f2524920ef0978594bec0e17d20b42b1068bfc73720bd`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be28b19174686f17ae1317ae4d3c9000a0c5da2daba3797916241b4eff9b024e`  
		Last Modified: Sat, 30 Apr 2022 00:41:03 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc429bf8652d7c199bc2696f50eb5d6d96995a020de7042fcefc0c861e53b494`  
		Last Modified: Sat, 30 Apr 2022 00:42:49 GMT  
		Size: 100.0 MB (100040496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24d376e5e7a9471996a0ba2517b9f4860601c4b261f5b4568a13a3138e91451`  
		Last Modified: Sat, 30 Apr 2022 00:42:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

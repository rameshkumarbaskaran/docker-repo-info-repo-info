## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:a8bc877d8e19973956ef30749608188b630d2bbe1983beec52e724b5afe13811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:abc6f12263c36be6cf4c61255c8db80e47f6f30763d5e5c8238c316f359d7e47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155377641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33df2c326276a958a69054ea4588ce1c733bf56d232003df252b1d33389a471`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:18:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:38:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:02:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 02 Feb 2022 05:03:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 05:03:32 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 05:03:32 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 05:03:32 GMT
ENV ROS_DISTRO=foxy
# Wed, 02 Feb 2022 05:04:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:04:42 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 02 Feb 2022 05:04:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 05:04:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762bb72141f73c9f8d23d9bc2396670126e4d86b9784e31484c651effc425f91`  
		Last Modified: Wed, 02 Feb 2022 03:38:42 GMT  
		Size: 1.2 MB (1182237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52b7e3f584549fa72b610dfd0819030eb6eb0a3a76a5d820599a986bb362dfb`  
		Last Modified: Wed, 02 Feb 2022 05:17:49 GMT  
		Size: 5.5 MB (5546994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ae25a4694ef2001927cb29325cd8fc4076b59d0d944cec831ce55095c4cb64`  
		Last Modified: Wed, 02 Feb 2022 05:20:30 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b7b6d92a2fd7f05c2ab982e2eaf8a7bb43a271459e4c3d5b978ff3f3de151f`  
		Last Modified: Wed, 02 Feb 2022 05:20:30 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0b826832564aea720214fd8993bf4bcd30e5c5affc246139bbb4355706836a`  
		Last Modified: Wed, 02 Feb 2022 05:20:50 GMT  
		Size: 120.1 MB (120081897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e227a65e902c4854536530c1bde6ed394c7fbf9e73cece166b682cdc5b436c`  
		Last Modified: Wed, 02 Feb 2022 05:20:30 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5ea949ed75ca8434d35585e70a0b31d4a4ef845cd37e38af8e29fb4b5728f0ae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137960201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b561f4eeba9abbf1c6202eac12bbb42ee6e61fe309ae52768003766d303ed912`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:16:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:16:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:22:43 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 02 Feb 2022 05:23:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 05:23:13 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 05:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 05:23:15 GMT
ENV ROS_DISTRO=foxy
# Wed, 02 Feb 2022 05:24:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:24:05 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 02 Feb 2022 05:24:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 05:24:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ab66679c5f55612a5d5bd5d43275d9d9341f5a8d22f9ab693b0ead2cc11a1`  
		Last Modified: Wed, 02 Feb 2022 05:38:36 GMT  
		Size: 1.2 MB (1184127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ae39722cb5853b6834527ad3541d6b6ee8351493f8694fbe2c77537d74b0fe`  
		Last Modified: Wed, 02 Feb 2022 05:38:34 GMT  
		Size: 5.3 MB (5322515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7946f51a9043a39941ea735b23552ad9871c050c9a76146ecbca02f3b2ccc0df`  
		Last Modified: Wed, 02 Feb 2022 05:41:14 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674eebb3ef8d3ac94a8d3359380c6daf533589b04c7ab1556a43889517abf0d2`  
		Last Modified: Wed, 02 Feb 2022 05:41:14 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d967b39d264a4018be170e1a117f2d1d186ab6260726f1ba1308a3226b6fd8d2`  
		Last Modified: Wed, 02 Feb 2022 05:41:32 GMT  
		Size: 104.3 MB (104281545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd2ed2e208297943b1f55f54d868f092c5729863692293b427e9fe549ccb6c2`  
		Last Modified: Wed, 02 Feb 2022 05:41:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

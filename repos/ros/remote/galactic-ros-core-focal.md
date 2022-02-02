## `ros:galactic-ros-core-focal`

```console
$ docker pull ros@sha256:51c482779a3bed81ac4c16fdfc76bdfeaa7c14ca7f1299ef41249106672e0afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:4e7b1f59bf6f2fd23993afa33400c0d5087e44a96a0e80958127d6876f0a5cae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138952032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d13b96c6fdfdd91c0b95a4ce7a96b68b626fb7aec400158db94ed1a018e87b`
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
# Wed, 02 Feb 2022 05:07:19 GMT
ENV ROS_DISTRO=galactic
# Wed, 02 Feb 2022 05:08:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:08:35 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 02 Feb 2022 05:08:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 05:08:36 GMT
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
	-	`sha256:3e536d0c494a5276b71c9d82029062e7da9214fb3128b19858f6dfce02d4c824`  
		Last Modified: Wed, 02 Feb 2022 05:22:09 GMT  
		Size: 103.7 MB (103656288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d0b260cdec3fe6f1e815f69f56a0aba63e551fd21355e861e53d044fa9e6d2`  
		Last Modified: Wed, 02 Feb 2022 05:21:52 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:144e86e7194de71fd683f8b77ea30e6f2b42030a80fb3bca4f63d9a677662479
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133717368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f896daf72fd8adf8037b43d2254f7f542170473a0d35eef21057eaa68bc228`
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
# Wed, 02 Feb 2022 05:27:22 GMT
ENV ROS_DISTRO=galactic
# Wed, 02 Feb 2022 05:28:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:28:13 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 02 Feb 2022 05:28:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 05:28:15 GMT
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
	-	`sha256:d1352fc18e4fa42b18faf684faac514cf3fb5b806bd5a0a75a6b25b7527a1cda`  
		Last Modified: Wed, 02 Feb 2022 05:42:58 GMT  
		Size: 100.0 MB (100038713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e90864b9aa3c0f76feeebbb7c4bcbf4da257ac2f3323d82d3ef9a2bdd84ec0`  
		Last Modified: Wed, 02 Feb 2022 05:42:40 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

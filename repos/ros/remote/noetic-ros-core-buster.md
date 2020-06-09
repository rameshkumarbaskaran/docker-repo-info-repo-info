## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:c77ec535307922c328c304afbd57f33e31658476ad5c2e145682ab658bfa86d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:6dde1b447061f2d391dc4d3c35015cc7b738b8022c190f540ed26ff8012c7980
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300090627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4f1c4d8f1ec8f6bcf5274a05b812d11d67ad1f1321e5fb97980f6ab1a0250a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 06:28:12 GMT
ADD file:fb54c709daa205bf9d04eb3d90ba068db4c34dfe3b6ec0d7691f677286120903 in / 
# Fri, 15 May 2020 06:28:13 GMT
CMD ["bash"]
# Wed, 27 May 2020 01:32:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:32:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 May 2020 01:32:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 May 2020 01:32:34 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2020 01:32:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 May 2020 01:32:35 GMT
ENV ROS_DISTRO=noetic
# Wed, 27 May 2020 01:33:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:33:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 27 May 2020 01:33:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 May 2020 01:33:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:376057ac6fa17f65688c56977118e2e764b27c348b3f70637fa829cd2a12b200`  
		Last Modified: Fri, 15 May 2020 06:37:20 GMT  
		Size: 50.4 MB (50391294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8414f05e9d7866ccb09d6c12bffe517dbed01796d379b94ff6b0770b033c5a6`  
		Last Modified: Wed, 27 May 2020 01:41:58 GMT  
		Size: 10.9 MB (10889343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516488eba09f3ee350bd860fcde1a77e8fded44cd0d73c1d38f31168c7fb2df2`  
		Last Modified: Wed, 27 May 2020 01:41:56 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0678db7e4fd2cd1e19b4e34680b821e27743d7cec864d22adcc09347221944f9`  
		Last Modified: Wed, 27 May 2020 01:41:56 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18958b3f6adbdd4706051abe00b90ba861588fa198287d6cb479f837d72bb8c`  
		Last Modified: Wed, 27 May 2020 01:42:46 GMT  
		Size: 238.8 MB (238808157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b0dd0d7aa0f76d7ded8e0eb4b9326f5beee9a9995cf4e49d684260c7354e9d`  
		Last Modified: Wed, 27 May 2020 01:41:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:03bbf3d6ace7111623cc33ae5076b1a888dd68fd9ea1deeb486bf10555c2e208
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244098903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5289fd4819d37f41583d31b8e64fce2e0b63dcb114843930737070c264a4867`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:51:33 GMT
ADD file:73f1cc6ac15b24788e78ae41cd6c89cb5211d64baf491accbd95b6fe9718f17f in / 
# Tue, 09 Jun 2020 01:51:36 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 13:05:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:05:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 09 Jun 2020 13:05:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 09 Jun 2020 13:05:33 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 13:05:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 09 Jun 2020 13:05:35 GMT
ENV ROS_DISTRO=noetic
# Tue, 09 Jun 2020 13:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:08:05 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 09 Jun 2020 13:08:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 09 Jun 2020 13:08:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1db90d3d3b6598d485690f804e96153fb632e7434251d334e9a0c49b773855c9`  
		Last Modified: Tue, 09 Jun 2020 01:57:52 GMT  
		Size: 49.2 MB (49167914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754a42675c9c6fb259aa9d305f565b45c35444de6deaee3143fb56477372bb67`  
		Last Modified: Tue, 09 Jun 2020 13:23:16 GMT  
		Size: 10.9 MB (10881984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24dae9041ffde16867846c8dc990ca42ed1e294c72b3060c495946be316ecf0`  
		Last Modified: Tue, 09 Jun 2020 13:23:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efc0e56bd18d48d8ccc89e984449e10ded921e728cef559dba731616be82bb1`  
		Last Modified: Tue, 09 Jun 2020 13:23:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafb1ab885364f60259d270c2d3791ed51aaf39b5a03364b73600d7dd72f2c4f`  
		Last Modified: Tue, 09 Jun 2020 13:24:18 GMT  
		Size: 184.0 MB (184047168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea9cc53a321a61c0dcc7accf7d1a059153fdd405bd5b16e1dc6fc6c2c902221`  
		Last Modified: Tue, 09 Jun 2020 13:23:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

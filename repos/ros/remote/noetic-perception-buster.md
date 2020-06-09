## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:1d96bed20eb65e6710d93279e9b21b7265033e616116150b52b6caab3b565ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:3fffa5f04862946f2e4fee523342fff5d84a36a919742ae8ae9797775dcc5dd9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **967.3 MB (967250471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e6a5375b2bec5902124c8abe3c4872dc7543c1e11811672fc2b0a49c720e29`
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
# Wed, 27 May 2020 01:34:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:34:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 27 May 2020 01:34:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:37:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:0ab67c6618bd901419e1937d43f6dedbcfdcb2104a1b515f320f8d76938baf29`  
		Last Modified: Wed, 27 May 2020 01:43:06 GMT  
		Size: 86.6 MB (86563228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cdba14561c081bf85ff3f9b0fd54839671df9712d72fc2d6a12300cac236e9`  
		Last Modified: Wed, 27 May 2020 01:42:50 GMT  
		Size: 185.9 KB (185912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1bd830ac707944e355244ce832b9877d77a87a4c62541ec0d17a218bd19006`  
		Last Modified: Wed, 27 May 2020 01:43:03 GMT  
		Size: 76.0 MB (75966400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4802cbc6efd702384e3d78045b2d5fbc5847f3cba30e001092f313cb6f3582ac`  
		Last Modified: Wed, 27 May 2020 01:44:56 GMT  
		Size: 504.4 MB (504444304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0bd2c25ef49a79ba41c7380216891d5a73d6081fc4b42875a2bee4b0c5a5b249
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **884.1 MB (884106361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccc13f3c993b5f80f4352b293fbe0810ebfc53f1ace3f2ba0fabc8b619cf2f0`
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
# Tue, 09 Jun 2020 13:08:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:09:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 09 Jun 2020 13:10:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:17:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:57e858d951b016c6b27902affe779566632a4274e26898d0e128bbbc5e9cd856`  
		Last Modified: Tue, 09 Jun 2020 13:24:43 GMT  
		Size: 84.4 MB (84354203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e88070e535eb6222848c6c5e21b81314ea1f15bfc66938d789bae88a1b0eca`  
		Last Modified: Tue, 09 Jun 2020 13:24:23 GMT  
		Size: 193.6 KB (193575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8d803494aafc6c9af2032fd359f9decf7edcf48564b7c282149a840034d22b`  
		Last Modified: Tue, 09 Jun 2020 13:24:45 GMT  
		Size: 74.1 MB (74090252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4561792f97d98547069f4e36a71f20c415b331f48483cca4c7cd8b36cc5f4517`  
		Last Modified: Tue, 09 Jun 2020 13:27:15 GMT  
		Size: 481.4 MB (481369428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:e1995420c092ed41cc734b0df5f86496d29b65fe3488272404dd6207ecb9d248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:e0e17b700196408888ab48ab7c914db7819ee82f326f2ba2cb6f8fe6d75f4919
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262693307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014f0adf022ed5d398f0b7f1dbd93f0daf5c2c99f625fc0225a710c59afc1ed1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:25 GMT
ADD file:11157b07dde10107f3f6f2b892c869ea83868475d5825167b5f466a7e410eb05 in / 
# Mon, 06 Jun 2022 22:21:26 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:28:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:28:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:28:35 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 07 Jun 2022 01:28:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 01:28:36 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 01:28:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 01:28:36 GMT
ENV ROS_DISTRO=humble
# Tue, 07 Jun 2022 01:30:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:30:13 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 07 Jun 2022 01:30:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jun 2022 01:30:14 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:31:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:31:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jun 2022 01:31:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 07 Jun 2022 01:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:405f018f9d1d0f351c196b841a7c7f226fb8ea448acd6339a9ed8741600275a2`  
		Last Modified: Wed, 01 Jun 2022 03:03:39 GMT  
		Size: 30.4 MB (30423715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d1d4bf62a3722d7122bc1b8ee8ad3051fcaf598ca72ad725fea76cb53f6b3c`  
		Last Modified: Tue, 07 Jun 2022 01:52:41 GMT  
		Size: 1.2 MB (1191642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5c906965a7cb2488a6e23da68abe175ee9acffbe27e61b1152cfff4fbf840b`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 3.8 MB (3827182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c1af53ce2d5965bf4c8489cf5459894d2e6c3f6b00538c076d38e41668d6cf`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8d3945eb76a1a2076630ee2752a89342d614a9298134e198075975ec08400d`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc5978e994b6f023efb223710613e46034904f6dce39ece5e5b8bf07fe938e1`  
		Last Modified: Tue, 07 Jun 2022 01:52:55 GMT  
		Size: 106.1 MB (106124318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff090f1a8ef849bdfa42139c0684e11771a61f5bb61ffba6a2b7c1d2fda9239`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f9c0d1c45afeb74327e597df16894662a900d8c355992eefeeb675d0769066`  
		Last Modified: Tue, 07 Jun 2022 01:53:18 GMT  
		Size: 97.8 MB (97838689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14416f74a08632618c2f5b301b40e1537c737981626b6d5a308c05ac0685cc69`  
		Last Modified: Tue, 07 Jun 2022 01:53:05 GMT  
		Size: 275.5 KB (275465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02f37a74d93c667b726c4a1db0b1e11226232ac78f437a285603c07d13d92ca`  
		Last Modified: Tue, 07 Jun 2022 01:53:05 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53e3e8d33911936f4e2551e3eae9526aa1994e89d0d66c3c0459900bd6d68ba`  
		Last Modified: Tue, 07 Jun 2022 01:53:08 GMT  
		Size: 23.0 MB (23007607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dd53e9e2406ccf7d756ffb8cf2ceeaa6dcf07913d02998b8cb7403253db4f282
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257481706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5870b8c68ed6ef3977a99e806781cd2794f727b434122942bcf81257410cf214`
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
# Mon, 23 May 2022 22:43:54 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 22:44:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2022 22:44:57 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Mon, 23 May 2022 22:44:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 22:44:59 GMT
CMD ["bash"]
# Mon, 23 May 2022 22:45:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2022 22:45:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 23 May 2022 22:45:42 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 23 May 2022 22:46:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:5686ce861dda605e75ee4a6bab3e53f097e4010fef23f34179217491d430d824`  
		Last Modified: Mon, 23 May 2022 22:48:33 GMT  
		Size: 106.4 MB (106393737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8fffc177af7b7119460aff11709207884cdfd1b72a774646124001a5718646`  
		Last Modified: Mon, 23 May 2022 22:48:16 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b0dfdb1762464e987b98fc9d974453ac3415bbfa8d9496752d012dba3294f`  
		Last Modified: Mon, 23 May 2022 22:48:59 GMT  
		Size: 95.2 MB (95223771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a449faeb594cb721b14a7fdb85cbeb8785586887a31b23fa6789b7606800ca7f`  
		Last Modified: Mon, 23 May 2022 22:48:45 GMT  
		Size: 271.1 KB (271074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2665d21fe01d8b1054c89ad2166988f46fadfa08fff394859103f47f7d2687`  
		Last Modified: Mon, 23 May 2022 22:48:45 GMT  
		Size: 2.2 KB (2178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73198756089c073e8dc6861da51d15bf7a80f3ef1ec0d9ea5bded64f40c08154`  
		Last Modified: Mon, 23 May 2022 22:48:49 GMT  
		Size: 22.4 MB (22425004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

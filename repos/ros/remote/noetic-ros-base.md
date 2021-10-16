## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:2a28053ca9ebd69e171aebfff8941ffdf17e0bf9bf890ec9cb2ba1e41b382659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:ccaf1b2477838808d73663f41c34719386ad7ea977091fdcbd19c95b9feff8c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339184977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c618f40d6ef1b8f46c2c5e4114809283344e4b751a46ab67c77aa17f174d411`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:03:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:02:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:02:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 01 Oct 2021 06:02:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 01 Oct 2021 06:02:23 GMT
ENV LANG=C.UTF-8
# Fri, 01 Oct 2021 06:02:23 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Oct 2021 06:02:23 GMT
ENV ROS_DISTRO=noetic
# Fri, 01 Oct 2021 06:04:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:04:15 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 01 Oct 2021 06:04:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Oct 2021 06:04:15 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 06:04:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:04:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 01 Oct 2021 06:05:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da6d2c6667ea5660473b4dbbded093f5fb0330bb09072dd5f023fe8917898f5`  
		Last Modified: Fri, 01 Oct 2021 05:15:23 GMT  
		Size: 1.2 MB (1183161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d76f6f81fcfbb67046fda7409d7f51373035330bf4b0b3f29d51ce1531379df`  
		Last Modified: Fri, 01 Oct 2021 06:24:29 GMT  
		Size: 5.5 MB (5547583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8985568900a589503a6b64505536a7ed14c04be58f49125487546556e4bf16d2`  
		Last Modified: Fri, 01 Oct 2021 06:24:28 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d396a66dc135f942aded0cbf41869920dd471f4ae69a577ef485c7fad6ad26f6`  
		Last Modified: Fri, 01 Oct 2021 06:24:28 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0e67a2d329fca5d4ed9676dc99b6786e3b630fb2cdc61a582593ee9c0d2af6`  
		Last Modified: Fri, 01 Oct 2021 06:24:57 GMT  
		Size: 176.7 MB (176698260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14f46e6b695aaf67ea964cbc89cec1bb208303e42ef77d8ae91776e089bb5ca`  
		Last Modified: Fri, 01 Oct 2021 06:24:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9999226e85f92a036c340a8cd8f6223dae10b187aabfcafcb3bf8db55c579c4c`  
		Last Modified: Fri, 01 Oct 2021 06:25:15 GMT  
		Size: 47.3 MB (47259853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d72ee051e2ffafedab97e53d9c1c7dd3d04e22c91edd5a6f5998bbc8649d9d`  
		Last Modified: Fri, 01 Oct 2021 06:25:07 GMT  
		Size: 321.5 KB (321468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e3373d9dd06236066e1567f04e4344c9a90b98b797e7f2ad101fbb541811bd`  
		Last Modified: Fri, 01 Oct 2021 06:25:20 GMT  
		Size: 79.6 MB (79603325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:0a3716d6cb18a81fec1cfc5432a842d427d986e07b8d7665dba5fb18bb1b6687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284608839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c32c2fedb278f6c38d9255abb83eedd072db50ee75a9e3462dac4cb7832785`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 01:12:00 GMT
ADD file:625e3906181f4bd86e59a0e9748f67fcb1391a2e65e36c729e71353381a49757 in / 
# Sat, 16 Oct 2021 01:12:00 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:17:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:17:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:17:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 16 Oct 2021 02:17:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 Oct 2021 02:17:54 GMT
ENV LANG=C.UTF-8
# Sat, 16 Oct 2021 02:17:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 16 Oct 2021 02:17:55 GMT
ENV ROS_DISTRO=noetic
# Sat, 16 Oct 2021 02:20:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:20:16 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 16 Oct 2021 02:20:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 16 Oct 2021 02:20:17 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:21:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:21:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 16 Oct 2021 02:22:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8795d4da4abd6abcafe7285749aa85d3a164999e84720a3845f764e56e306771`  
		Last Modified: Sat, 16 Oct 2021 01:15:01 GMT  
		Size: 24.1 MB (24064451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764ddf81fcf398a2a4cf14036409b82f4f4a06bd8f23171e840ff36accba4d4f`  
		Last Modified: Sat, 16 Oct 2021 02:29:43 GMT  
		Size: 1.2 MB (1186846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02b4dedc9080b63cee4513e2787d54376223246780de27866414412fce505a7`  
		Last Modified: Sat, 16 Oct 2021 02:29:43 GMT  
		Size: 4.7 MB (4676770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb049eda64c876c1ee585dd51f3f8b9a9807c82541e8243ea725bcf5ee59fb2c`  
		Last Modified: Sat, 16 Oct 2021 02:29:40 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7037e3e565c8acccf66678f470f9ceae8503c90974e2dd927764191193ffdbb`  
		Last Modified: Sat, 16 Oct 2021 02:29:40 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69724b9a0973ce0c31fba9293b5ca2cc8e252ee13673b3053258594c1fa8b815`  
		Last Modified: Sat, 16 Oct 2021 02:31:48 GMT  
		Size: 157.2 MB (157179504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df68017d0a78706560ec19c60581120f31997ecd5e9223e1eec432c47ae86e8`  
		Last Modified: Sat, 16 Oct 2021 02:29:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb98f2a916633a1fb1a69dd5aebc5416fb396d43233943523788ff874a76fde`  
		Last Modified: Sat, 16 Oct 2021 02:32:19 GMT  
		Size: 36.7 MB (36691673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7242c94fc3e260adf5325a33e1e99237f52197a87e7ea5b471bdd8bd9eb4b0b0`  
		Last Modified: Sat, 16 Oct 2021 02:32:00 GMT  
		Size: 322.9 KB (322903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5bbb4e057a5f879119a31a98e9617ab535d39046bf80b55735ded907115af3`  
		Last Modified: Sat, 16 Oct 2021 02:32:38 GMT  
		Size: 60.5 MB (60484275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ec02baf086f3161863a635d2b2df2454d0295eebf71581502327d6660c166562
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.2 MB (318192403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de807f1bc97c1d09c087e0a9f287128a9b048361c5f049ce3ea7bfdae5ae3be`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:19:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:19:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:19:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 16 Oct 2021 02:19:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 Oct 2021 02:19:41 GMT
ENV LANG=C.UTF-8
# Sat, 16 Oct 2021 02:19:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 16 Oct 2021 02:19:43 GMT
ENV ROS_DISTRO=noetic
# Sat, 16 Oct 2021 02:20:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:20:37 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 16 Oct 2021 02:20:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 16 Oct 2021 02:20:39 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:21:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:21:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 16 Oct 2021 02:21:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44426e3a0ed188569ceb995612f61d01b012f19e6849dacdcdef24f70e9e820b`  
		Last Modified: Sat, 16 Oct 2021 02:44:04 GMT  
		Size: 1.2 MB (1186725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74557b92a76c488a6e2f31c091f03671baadbd5b593c4af9dbde2baea1616333`  
		Last Modified: Sat, 16 Oct 2021 02:44:02 GMT  
		Size: 5.3 MB (5322455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c260b335cf07f336d1a4e8a82a9d7c692b2bd9787a59304939f8efa4f0101336`  
		Last Modified: Sat, 16 Oct 2021 02:44:01 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c22181ff3d3903d9cd1bf4e764959b25637ae8513f97bce318dd8a7bd39e5ac`  
		Last Modified: Sat, 16 Oct 2021 02:44:01 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4102e4fa66f5f968fd33f8eba29fb388cbe15692b65aa6ee4b73ee49911cc03c`  
		Last Modified: Sat, 16 Oct 2021 02:44:31 GMT  
		Size: 171.1 MB (171127704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd3223aef57941776d9e8c82021b54601bc6c98c9c4e37c09088868f34689ad`  
		Last Modified: Sat, 16 Oct 2021 02:44:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67dce296a497287c39667aecbda14a56772cabb7fce0bf6814c5b0fc71fe902`  
		Last Modified: Sat, 16 Oct 2021 02:44:48 GMT  
		Size: 41.3 MB (41305313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b380c08d48bfaa5743c1d9aa123728e4bfe4d4de65c3042c42b18d2316d777`  
		Last Modified: Sat, 16 Oct 2021 02:44:42 GMT  
		Size: 322.8 KB (322832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c1c8b80456c31f0be34412d39189749a6937d731e58136ac9d81186b6dbc6b`  
		Last Modified: Sat, 16 Oct 2021 02:44:52 GMT  
		Size: 71.8 MB (71754103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

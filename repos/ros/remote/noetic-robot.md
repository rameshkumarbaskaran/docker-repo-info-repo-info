## `ros:noetic-robot`

```console
$ docker pull ros@sha256:e5a3c06599ad6e7a0f872d9b9534946f709419156df861e9a08f339ee3b2771c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:55837b1cb4d123a7d660ef72f2049c8f0549ec14d8880662d5df6bfd1c1b8f67
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.9 MB (354923887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc39b9cef5aa66733784d741535e752bbb6d1588294e89ba4ecfc10d91eed3b`
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
# Fri, 01 Oct 2021 06:06:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:29d8971de91fa5cee1dee45e2e717a59c529854e5c18f2619545c3b5163bf712`  
		Last Modified: Fri, 01 Oct 2021 06:25:35 GMT  
		Size: 15.7 MB (15738910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:9a7de897dae99a7589a7d920c3fc323a2b1b2ab317f8d997a0958605ec26188b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298573997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4021fb42a3360ba288aadda7e5e6d7d9f5b59bfcf5ecb74b9ca689f5d238c6f7`
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
# Sat, 16 Oct 2021 02:22:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a5a73ef1a5ea79bedbff1bb66d2f1ca1debb4e3e7765cdeeb3e358f8ce0414b5`  
		Last Modified: Sat, 16 Oct 2021 02:33:03 GMT  
		Size: 14.0 MB (13965158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2f3aeaf51a9ac77b48225d1409b34c215f795f9a712512976654c5aca682694b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333540491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43134256327b8117993acef98a723b33f18ce79eeb96bc4afdc4664950dcbe35`
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
# Sat, 16 Oct 2021 02:21:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:b9588c58320e3d7dc3f7913b1c3e314b42ff8f4161ab305728a1932470117d2b`  
		Last Modified: Sat, 16 Oct 2021 02:45:09 GMT  
		Size: 15.3 MB (15348088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

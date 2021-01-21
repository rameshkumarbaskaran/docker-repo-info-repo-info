## `ros:rolling-ros1-bridge`

```console
$ docker pull ros@sha256:fc6d78a0292ec82e8851d6fdf578da56425f906938948ac249b552475e83536a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:537f792e5d003317d24f5645aff9d2021d209871bd1507afd4229bd65dbb5b0d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334735301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b7dadb6f5874e89eaccf26bd1fbb107f92c085fe797a8a69f2bfffa6069be1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:26 GMT
ADD file:4f15c4475fbafb3fe335e415e3ea1ac416c34af911fcdfe273c5759438aa8eb4 in / 
# Wed, 25 Nov 2020 22:25:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:29 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:07:03 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:59:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:59:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 02:19:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 26 Nov 2020 02:20:00 GMT
ENV LANG=C.UTF-8
# Thu, 26 Nov 2020 02:20:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Nov 2020 02:23:04 GMT
ENV ROS_DISTRO=rolling
# Thu, 26 Nov 2020 02:23:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:23:54 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 26 Nov 2020 02:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Nov 2020 02:23:55 GMT
CMD ["bash"]
# Thu, 26 Nov 2020 02:24:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:24:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 26 Nov 2020 02:24:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 26 Nov 2020 02:24:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:24:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 02:24:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 26 Nov 2020 02:24:57 GMT
ENV ROS1_DISTRO=noetic
# Thu, 26 Nov 2020 02:24:57 GMT
ENV ROS2_DISTRO=rolling
# Wed, 02 Dec 2020 19:31:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.9-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:17:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.10.0-1*     ros-rolling-demo-nodes-cpp=0.11.0-1*     ros-rolling-demo-nodes-py=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:17:58 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:da7391352a9bb76b292a568c066aa4c3cbae8d494e6a3c68e3c596d34f7c75f8`  
		Last Modified: Fri, 06 Nov 2020 15:20:07 GMT  
		Size: 28.6 MB (28563271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14428a6d4bcdba49a64127900a0691fb00a3f329aced25eb77e3b65646638f8d`  
		Last Modified: Wed, 25 Nov 2020 22:26:39 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2d948710f21ad82dce71743b1654b45acb5c059cf5c19da491582cef6f2601`  
		Last Modified: Wed, 25 Nov 2020 22:26:40 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5df4314d5099f1cf2100a5313a0658ed554a2983ba59b623b5bad8c4809e05`  
		Last Modified: Thu, 26 Nov 2020 02:31:32 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c14ddc5480deadf9144c474a609532b85769b3254ed91b971659b90177719f`  
		Last Modified: Thu, 26 Nov 2020 02:31:32 GMT  
		Size: 5.5 MB (5547277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0070f07bf5a4e96efca137c61d59aaadf64010bc606c054d868f3afa6e44a981`  
		Last Modified: Thu, 26 Nov 2020 02:31:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9effa899cb9a89f581ee93ba079029c694a6fb10175cfeb3309ebc4551872a`  
		Last Modified: Thu, 26 Nov 2020 02:37:49 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279675193622226863d2accf21f93581d754d3cc767cf826e516b87dc3db5e3b`  
		Last Modified: Thu, 26 Nov 2020 02:39:51 GMT  
		Size: 119.6 MB (119589291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e078e688a9d7470ed7945fd897dd8706a44e54faa117af3cddab0b75ce4ed9e2`  
		Last Modified: Thu, 26 Nov 2020 02:39:16 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f69afe775a00eb582006e78d5292f9a00125eea9eaadeacea3629bf869bd615`  
		Last Modified: Thu, 26 Nov 2020 02:40:10 GMT  
		Size: 66.6 MB (66588090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcf884fe79efaad0e13cb4249d690c0e4ca003dd43375c7681945a64f83bd7c`  
		Last Modified: Thu, 26 Nov 2020 02:39:56 GMT  
		Size: 191.9 KB (191864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e13fa34c164e85d3585644067165e6f28003f00a4abbeb89c68a779387d78da`  
		Last Modified: Thu, 26 Nov 2020 02:39:55 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06e9b59af3f86339cf1866af69ee107bec19189c301fab2007da6a7eceb74d1`  
		Last Modified: Thu, 26 Nov 2020 02:39:59 GMT  
		Size: 10.5 MB (10476192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81b55a9a3cd3fc4a7a2118626f47b2dcc057cf111ef5a5f9fa0f798f0a54bb`  
		Last Modified: Thu, 26 Nov 2020 02:40:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5d40c8940df51e23f4ca90f51160421dbe8d2812a011b72c1565a9269f848e`  
		Last Modified: Thu, 26 Nov 2020 02:40:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb259285a832ef5d4208863a89ddcd48b63ce4069b29ee253fe756cadf14d27`  
		Last Modified: Wed, 02 Dec 2020 19:33:52 GMT  
		Size: 76.1 MB (76088688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e791116ccb1c8f5bf341c797beba5228bc99c41f13d6a6777f484e6ae72ef697`  
		Last Modified: Tue, 12 Jan 2021 01:29:20 GMT  
		Size: 26.5 MB (26506655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b67f436ea826b386be55dc5c2b2fd7cdd6cf4c4237402f8365dfdb8a9873677`  
		Last Modified: Tue, 12 Jan 2021 01:29:11 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:68f48b5b48069a5dd7995c564331598a34076566a0c3f3ed1c455a4ad04b5f2a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308569273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a79160af9c7d4c802840e449a0dd2326d26cb2e2e29b88d6f53c9049265f01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 06:45:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:45:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:45:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 07:09:09 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 21 Jan 2021 07:09:09 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 07:09:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 07:14:48 GMT
ENV ROS_DISTRO=rolling
# Thu, 21 Jan 2021 07:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:16:39 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 21 Jan 2021 07:16:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 07:16:42 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 07:17:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:17:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 07:18:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Jan 2021 07:18:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:19:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 07:19:16 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 07:19:17 GMT
ENV ROS1_DISTRO=noetic
# Thu, 21 Jan 2021 07:19:18 GMT
ENV ROS2_DISTRO=rolling
# Thu, 21 Jan 2021 07:20:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.9-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:21:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.10.0-1*     ros-rolling-demo-nodes-cpp=0.11.0-1*     ros-rolling-demo-nodes-py=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:21:15 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf194558d7d697893645e2928d8c12f602b77dd0aaf2f5344233277d7b160d1`  
		Last Modified: Thu, 21 Jan 2021 07:29:34 GMT  
		Size: 1.2 MB (1183038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f15cd3db3fa7d5351aa9b332d57ca02a4276fef9f7b3363ef98b2c4f9611d8`  
		Last Modified: Thu, 21 Jan 2021 07:29:31 GMT  
		Size: 5.5 MB (5514280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de67e6495e9d3639f76b9c4f19a8a602bcf7fe068fb7b7f08ee8cba855c1f301`  
		Last Modified: Thu, 21 Jan 2021 07:29:32 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dba3fea46fa21f2e435af76ebf72934a3b25fc18e9d03b07f583304b0335d7e`  
		Last Modified: Thu, 21 Jan 2021 07:36:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292fe15401fa20919feee7ef656cc89d14e3fd4588d3acf9afa81ba5d694e418`  
		Last Modified: Thu, 21 Jan 2021 07:38:55 GMT  
		Size: 104.0 MB (103959553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65506f9e42a413dd004c5ca05f35b5c93d44d17eaaaed4ecb4a0ba086f6d5788`  
		Last Modified: Thu, 21 Jan 2021 07:38:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cb10bf9dab8eb9804d307c75f6f9bbd32e7c44b246c486243b21d832e9c76d`  
		Last Modified: Thu, 21 Jan 2021 07:39:29 GMT  
		Size: 60.9 MB (60916470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b67cfd545dfe0a02a40ee2e48799f77df6ad16188aec7af2b8b825e0aee06f`  
		Last Modified: Thu, 21 Jan 2021 07:39:16 GMT  
		Size: 198.9 KB (198915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a946c6ab8cde674a07a2c180f1524bc4fae61a10c18f7db345664a8498e1d9`  
		Last Modified: Thu, 21 Jan 2021 07:39:16 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60d6fed229d22b0a8f7e78d2c929ad203ee660769e5dffbf7865d88ad2fddb2`  
		Last Modified: Thu, 21 Jan 2021 07:39:20 GMT  
		Size: 20.9 MB (20941494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c5ed917db6ef6b506817f3237dc6e9a3f959c1f9ae16149e308e3f0e6fa71b`  
		Last Modified: Thu, 21 Jan 2021 07:39:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce8b3b65709e415a646e5f7175809c44f997933362d87f1af96207d5950cfd2`  
		Last Modified: Thu, 21 Jan 2021 07:39:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d86a384366eda9a5a905f8823eb46d1bfef41f0cce84ce75279415bfed89b`  
		Last Modified: Thu, 21 Jan 2021 07:40:10 GMT  
		Size: 76.2 MB (76170532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174a31b07955e956c15e5bd687e21a71ea79e8d9f1e0a55c81f3cdbf1c5935ff`  
		Last Modified: Thu, 21 Jan 2021 07:39:49 GMT  
		Size: 12.5 MB (12506503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fae7eb5f99aec60c182b506cfbbe5fcd62421f14337fd3ee153894bcc122e59`  
		Last Modified: Thu, 21 Jan 2021 07:39:42 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:dashing-ros1-bridge`

```console
$ docker pull ros@sha256:928e5861094173afd678ce6f7410ca9072e9e722ac1bf274c0facb913dd8e1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:1e16744e26c98ce41ef74838e3c42df9af8bd91b9be1c617f1de4a12264eef8b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.6 MB (418552199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a513e0f729c397fe399625dc4cb1355e0fd93abfedc9b0b00bd6f93b3441ea6e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Tue, 19 May 2020 18:27:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:29:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:29:35 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 May 2020 00:45:30 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 27 May 2020 00:45:30 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2020 00:45:31 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 May 2020 00:45:31 GMT
ENV ROS_DISTRO=dashing
# Wed, 27 May 2020 00:47:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:47:25 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 27 May 2020 00:47:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 May 2020 00:47:25 GMT
CMD ["bash"]
# Wed, 27 May 2020 00:48:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:48:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 27 May 2020 00:48:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 27 May 2020 00:48:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 08 Jun 2020 22:21:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Mon, 08 Jun 2020 22:21:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Mon, 08 Jun 2020 22:21:29 GMT
ENV ROS1_DISTRO=melodic
# Mon, 08 Jun 2020 22:21:29 GMT
ENV ROS2_DISTRO=dashing
# Mon, 15 Jun 2020 23:23:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.6-1*     ros-melodic-roscpp-tutorials=0.9.2-1*     ros-melodic-rospy-tutorials=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 15 Jun 2020 23:23:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.5-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 15 Jun 2020 23:23:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Mon, 15 Jun 2020 23:23:49 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1fb7c1137ce366c52ed0850f79d5d96e24ecd02d5e5a6692c4265203713bdd`  
		Last Modified: Tue, 19 May 2020 18:53:24 GMT  
		Size: 837.5 KB (837516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6481f53850f8302d04fa37826e23bd91669bb22244764a2378bc03775063b3c0`  
		Last Modified: Wed, 27 May 2020 00:53:51 GMT  
		Size: 4.9 MB (4867298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d033e4703843b0f18fa16f9373153855816f953158e199abd64dec4a381abefe`  
		Last Modified: Wed, 27 May 2020 00:53:51 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf4d671437c6cca9ed496889014b8140ef23f5c4675b72c0d0fe9efba15e7dc`  
		Last Modified: Wed, 27 May 2020 00:59:08 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b37429f6191c8a30c1c62ff7647594e16b6415145b942e005cf2a6dc4a8b83e`  
		Last Modified: Wed, 27 May 2020 00:59:45 GMT  
		Size: 179.4 MB (179409193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a367d9722953d38910e5191d790edc3a4bcc27d16372bfbf892eaca53816406`  
		Last Modified: Wed, 27 May 2020 00:59:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ddc41e729381811da1ef118d91242a3287e98f52da65ec2e28e8bf781cfd2a`  
		Last Modified: Wed, 27 May 2020 01:00:02 GMT  
		Size: 64.1 MB (64139165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d33dd09802f5fd52215082bb7634d7822c89df179456833f25d231167c1ba0`  
		Last Modified: Wed, 27 May 2020 00:59:49 GMT  
		Size: 181.3 KB (181304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58000c3324d41e55f36ea63ee56dccd44871edc87e9601aaa728c6c8f00d0da1`  
		Last Modified: Wed, 27 May 2020 00:59:50 GMT  
		Size: 2.0 KB (1974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60a629b4df67fd3f9c0048c71e0649e0d80892a364ad88030a2974cf3409cb7`  
		Last Modified: Wed, 27 May 2020 00:59:51 GMT  
		Size: 4.3 MB (4311731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e43e462c72c1c193ce5bade61f24e2a66de3e82d8abb974844463f1c0cccb9`  
		Last Modified: Mon, 08 Jun 2020 22:28:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947b393027d9702fd3fcac2432286bfc9f99aa8a48259f1f653d86c8253fbaae`  
		Last Modified: Mon, 08 Jun 2020 22:28:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1792b94a0c69ab8f25e4e4695ec3bb8ffa382ce2d6bcbd6867eccf0258dee569`  
		Last Modified: Mon, 15 Jun 2020 23:26:28 GMT  
		Size: 117.7 MB (117664569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122644b8acbd088cbea324db35c4381cb87368ec65f30b6321eb4b983e58f7e0`  
		Last Modified: Mon, 15 Jun 2020 23:26:12 GMT  
		Size: 19.8 MB (19772935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ea4255e329cd6165ef3c3df0328706399c7062996a55337251ef1d4d484de8`  
		Last Modified: Mon, 15 Jun 2020 23:26:06 GMT  
		Size: 637.9 KB (637880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a98b1e1d7ed8a5650f7bb728db78f225733ea8411375d6ae14822de26598dbf`  
		Last Modified: Mon, 15 Jun 2020 23:26:06 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge` - linux; arm variant v7

```console
$ docker pull ros@sha256:3a8b2082e9264076698ce7adaf000defe7eabbc19c57f4690097a46b44eb879d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354683878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d162f7fdc0f705cfb029603de4bff63c47eb1be7a1260ed11123c9bc4f9fa2b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Jun 2020 02:02:00 GMT
ADD file:579f3bbed274bd8ec97aa5bfc4eb09fdcfe3e12e37fb3739f3096138b765581c in / 
# Wed, 17 Jun 2020 02:02:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 02:02:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 02:02:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 02:02:09 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:20:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:20:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:21:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 17 Jun 2020 03:34:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 17 Jun 2020 03:34:15 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jun 2020 03:34:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 17 Jun 2020 03:34:18 GMT
ENV ROS_DISTRO=dashing
# Wed, 17 Jun 2020 03:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:37:20 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 17 Jun 2020 03:37:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Jun 2020 03:37:23 GMT
CMD ["bash"]
# Wed, 17 Jun 2020 03:38:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:38:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 17 Jun 2020 03:39:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 17 Jun 2020 03:39:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:39:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 17 Jun 2020 03:39:40 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 17 Jun 2020 03:39:42 GMT
ENV ROS1_DISTRO=melodic
# Wed, 17 Jun 2020 03:39:43 GMT
ENV ROS2_DISTRO=dashing
# Wed, 17 Jun 2020 03:43:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.6-1*     ros-melodic-roscpp-tutorials=0.9.2-1*     ros-melodic-rospy-tutorials=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:43:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.5-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:44:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:44:05 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:2d63ac53d1bca136340c80fe8b64c0b8e2d9a62eddb6fcb794c489840dc027d6`  
		Last Modified: Sat, 30 May 2020 09:27:47 GMT  
		Size: 22.3 MB (22275987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e03e3a8e7321c64d7a483fc9cc0054ce81e5b230b32300b7c68d21001f661a`  
		Last Modified: Wed, 17 Jun 2020 02:05:28 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0e8090890c513488a0f67683f23dcfcfbf2b67e5be854edf1323ad87a60b26`  
		Last Modified: Wed, 17 Jun 2020 02:05:28 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b801ccb19e43939aa60383f674f0e1f65ab062890870d42d0fa7a7a62fc5b708`  
		Last Modified: Wed, 17 Jun 2020 02:05:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd193992630ce3c05616b2d6384bc7261c04210de22ad6879778b9aca67aaa81`  
		Last Modified: Wed, 17 Jun 2020 03:55:51 GMT  
		Size: 838.2 KB (838177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a62e43a84ad9c1d846a6d034c6ec80467b2e21c620fd37591f04eba4cdb0c01`  
		Last Modified: Wed, 17 Jun 2020 03:55:49 GMT  
		Size: 4.1 MB (4083577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76400ef72b32df9a8e2460f1a21fdf6afb134ef4aa07c8141f7bb89eb6dcff9c`  
		Last Modified: Wed, 17 Jun 2020 03:55:48 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918fdc185d3fb3945554b26f476ae406a19ce7616be5e247ed94bf07f74d446e`  
		Last Modified: Wed, 17 Jun 2020 03:59:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da62c2e483ea00a55a9d65d7737f90a97abd29a1d4b79325672db4747f115b6`  
		Last Modified: Wed, 17 Jun 2020 03:59:58 GMT  
		Size: 153.5 MB (153529872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f1f42827fdc461d12676571e811b8498190d7c068b00a782305f02b7c6c579`  
		Last Modified: Wed, 17 Jun 2020 03:59:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c979a019c92d1d8b61b50498482754a06cc0aff8cb700ef276307fefe5d8a148`  
		Last Modified: Wed, 17 Jun 2020 04:00:20 GMT  
		Size: 48.5 MB (48521547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d56ea6003bb1e56d2ef68b3dc57b95428134355f14ee8321dd07c5a0c63d2d5`  
		Last Modified: Wed, 17 Jun 2020 04:00:14 GMT  
		Size: 182.1 KB (182123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3809834686d16cb261b5af7ad27c28c7fb8946aa71065a0e2e5d1ef6606d9e`  
		Last Modified: Wed, 17 Jun 2020 04:00:14 GMT  
		Size: 2.0 KB (2040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5350355b05b6202f9342228f1000ae003e802d6796855bfe2a09ee2bc036cf09`  
		Last Modified: Wed, 17 Jun 2020 04:00:14 GMT  
		Size: 3.2 MB (3249127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9152345f837c3633eec3ddf20b28ba76b5b7150280be9bdfa6f85534d35cdfd`  
		Last Modified: Wed, 17 Jun 2020 04:00:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3046b23c22415ed950fec5201b7fd9249480fcbd9e8e6f68d448c4bd16624bc`  
		Last Modified: Wed, 17 Jun 2020 04:00:28 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e508ccb0afb801600d8e8a130a75af82fec4db9a84e4761267e8940246fe44`  
		Last Modified: Wed, 17 Jun 2020 04:01:02 GMT  
		Size: 110.5 MB (110537636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9750b0af23205926586909e61d61d078d3d61bee3f6c1929eaccdcb9c23864`  
		Last Modified: Wed, 17 Jun 2020 04:00:33 GMT  
		Size: 10.8 MB (10790023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2456122253b403d1ec6c74ba6da6679435e8c069ff117a6c8d836807a30009b`  
		Last Modified: Wed, 17 Jun 2020 04:00:27 GMT  
		Size: 634.8 KB (634801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2e2398aefaa8ad3a3355887877907d06775a97e7abca21e419020d455efd0a`  
		Last Modified: Wed, 17 Jun 2020 04:00:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d94646ef9f9451ba919d04c35dd6059f4d8d16183316a187f035ec71111dd8ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 MB (386964395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c97dcb08b369159ec413c402121b893aac24cb5b0f40013bddf8d7629799f2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Apr 2020 00:16:45 GMT
ADD file:bd5b3470601aa4a28132ec60a8b1c33516d09a1391864fe1dbf82a4030397fd1 in / 
# Fri, 24 Apr 2020 00:16:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:16:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:17:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:17:05 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2020 00:49:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:50:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:50:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 May 2020 01:15:33 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 27 May 2020 01:15:34 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2020 01:15:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 May 2020 01:15:36 GMT
ENV ROS_DISTRO=dashing
# Wed, 27 May 2020 01:18:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:18:12 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 27 May 2020 01:18:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 May 2020 01:18:15 GMT
CMD ["bash"]
# Wed, 27 May 2020 01:19:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:19:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 27 May 2020 01:19:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 27 May 2020 01:20:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 08 Jun 2020 22:42:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Mon, 08 Jun 2020 22:42:30 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Mon, 08 Jun 2020 22:42:32 GMT
ENV ROS1_DISTRO=melodic
# Mon, 08 Jun 2020 22:42:33 GMT
ENV ROS2_DISTRO=dashing
# Mon, 15 Jun 2020 22:46:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.6-1*     ros-melodic-roscpp-tutorials=0.9.2-1*     ros-melodic-rospy-tutorials=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 15 Jun 2020 22:46:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.5-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 15 Jun 2020 22:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Mon, 15 Jun 2020 22:46:36 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:c2cd007b69f7e5f37c851aa689e0e617fbaa3fe3e470f714337a03e569b7f434`  
		Last Modified: Sun, 05 Apr 2020 20:25:25 GMT  
		Size: 23.7 MB (23720401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c087f8bf83d28baa9c53fc5cfb0dfc79d5062cfad77563076553b04259e822f`  
		Last Modified: Fri, 24 Apr 2020 00:21:16 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474b5c43e9a24e1958763941a17a7cac60b13460a47f2ae9067ec03ceadab33a`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7083e6591d76b9a6c13497a6a89bfbae3e7eb2eb31bec366bec3884c8e4517ce`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dda2f76658374dcd686c5a8ced496568ee3c27f769ca4f27b8239ed598f93b3`  
		Last Modified: Wed, 27 May 2020 01:28:57 GMT  
		Size: 838.0 KB (838048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e9c4511121659f47ba9f8f9e13143b1a9be59dc0bcec713ae442df0061f984`  
		Last Modified: Wed, 27 May 2020 01:28:56 GMT  
		Size: 4.5 MB (4451160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac08a94b43dc19626f7d5dff278d0b87e673351b9b1daf1f6237c03ebd0e1e4`  
		Last Modified: Wed, 27 May 2020 01:28:55 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9aa3ce985352c2d0665b9b6f9367163fb2ee2459ebb2936933495dba1079f86`  
		Last Modified: Wed, 27 May 2020 01:36:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cd2fa20f67cb3ca0f805ddceceeb35ca128ccfdaba409b59768e6561d91167`  
		Last Modified: Wed, 27 May 2020 01:37:11 GMT  
		Size: 165.0 MB (165045268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a415da9dd923170e50b6de800c897efa45c6cca3dd4f9cb4e03d4afdd89dc2`  
		Last Modified: Wed, 27 May 2020 01:36:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7068f6fa8b6c6cc9edab04646347af160cafab8d308fa1e71df0145cb0a75fd`  
		Last Modified: Wed, 27 May 2020 01:37:30 GMT  
		Size: 56.8 MB (56848958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06a62e119d34d15248d610cca63d28820282330e78e7d02e4451f67363f1fa5`  
		Last Modified: Wed, 27 May 2020 01:37:17 GMT  
		Size: 181.4 KB (181368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16eb2ea6b71ddcdd7402014cfd605217965f5c85b20ee94be357c598ce383b7`  
		Last Modified: Wed, 27 May 2020 01:37:17 GMT  
		Size: 2.0 KB (2046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6caaa91f8cd632ba18b0fc53314d680f815e8f0bd74808d0376f01b6d54acc`  
		Last Modified: Wed, 27 May 2020 01:37:18 GMT  
		Size: 3.7 MB (3664524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aef62de8d024604631797c9fb698fd425f7824ca14ccbc91432ed9753d53a59`  
		Last Modified: Mon, 08 Jun 2020 22:55:13 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453fa02d06d024b36cb437320d453042166da72e2b369368079435774a6d7d03`  
		Last Modified: Mon, 08 Jun 2020 22:55:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d494bb8cbaf0fc633795f0cae500f3dfd76b49d72ae148db51e594f3166f0e95`  
		Last Modified: Mon, 15 Jun 2020 22:51:17 GMT  
		Size: 116.6 MB (116606898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff3b41a43806740407787baaf72c0f907da5b12ead6ee5f28177530bde0c0a`  
		Last Modified: Mon, 15 Jun 2020 22:50:48 GMT  
		Size: 14.9 MB (14931203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6416e8f099635d037abc8739b940a3a3738b59415447334f4a324b469e031de9`  
		Last Modified: Mon, 15 Jun 2020 22:50:42 GMT  
		Size: 635.8 KB (635818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff703d07eb83362e7531df4ad4cd0cc5b60ca4df455856d5e6dd20185b8bf34`  
		Last Modified: Mon, 15 Jun 2020 22:50:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

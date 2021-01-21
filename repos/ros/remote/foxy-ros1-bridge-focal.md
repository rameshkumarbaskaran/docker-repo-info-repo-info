## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:32b585f8f02564a076c39c4a346a792ff8afa3fa003e74a3df175cdeed3f564e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:9ee5de2e787af271976cdc29b4e51a8d7b7879107aa27009b86133c565392e22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340536418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a5afbb5c912619d29d5ab5007950a9f0755c6a37d9bda5b3b2478948fe5e39`
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
# Thu, 26 Nov 2020 02:20:00 GMT
ENV ROS_DISTRO=foxy
# Thu, 26 Nov 2020 02:20:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:20:57 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 26 Nov 2020 02:20:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Nov 2020 02:20:58 GMT
CMD ["bash"]
# Thu, 26 Nov 2020 02:21:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:21:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 26 Nov 2020 02:21:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 26 Nov 2020 02:21:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:21:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 02:22:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 26 Nov 2020 02:22:00 GMT
ENV ROS1_DISTRO=noetic
# Thu, 26 Nov 2020 02:22:01 GMT
ENV ROS2_DISTRO=foxy
# Wed, 02 Dec 2020 19:30:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.9-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:39:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:39:58 GMT
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
	-	`sha256:97ca2b4177d6cde94467250628146b3ec2b4878c689a5793c95255bd1810cf98`  
		Last Modified: Thu, 26 Nov 2020 02:38:20 GMT  
		Size: 119.6 MB (119550944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69214d623bffdbd15fa6fe5c7e8522d6b8f25c2a30dff43e2331f7b8e96afbc`  
		Last Modified: Thu, 26 Nov 2020 02:37:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449bf3abdc883d6b34dc34d574ece3fab8b7692736c3f417d741c64098b0a612`  
		Last Modified: Thu, 26 Nov 2020 02:38:39 GMT  
		Size: 66.6 MB (66587550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53cb93c23f47e979e29921a9a0be94caee8835213ebc5b9352b98f7248fbc4b`  
		Last Modified: Thu, 26 Nov 2020 02:38:26 GMT  
		Size: 200.4 KB (200412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1f899623aee959f4ef131352aab4a4c7ddd5edd22e9bed8add4d29f9ad1dbf`  
		Last Modified: Thu, 26 Nov 2020 02:38:26 GMT  
		Size: 2.0 KB (2004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66830fc82a9368c7df302f2f860e9789a16893acf72f27d66c92ed9070b7c50b`  
		Last Modified: Thu, 26 Nov 2020 02:38:29 GMT  
		Size: 10.3 MB (10283427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b607718e9c3c5e8a8c90900e803c433b71a7e8d70ad236fdd2e811511552c2c`  
		Last Modified: Thu, 26 Nov 2020 02:38:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e532030053d411e1426487ed99c929dad34870891ff6761cad0699bc3a879d6d`  
		Last Modified: Thu, 26 Nov 2020 02:38:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea656baddd5eda69ed59385ec4998344df1619881efa6b6e934a8eda236482f`  
		Last Modified: Wed, 02 Dec 2020 19:33:10 GMT  
		Size: 76.1 MB (76087755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28f412c087cc1afae61629a349efb254a96101b6f3ab2589b09c157eeaca87f`  
		Last Modified: Mon, 14 Dec 2020 22:43:08 GMT  
		Size: 32.5 MB (32531776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0ecfd18205c6aeccfebb328a734dc16cb68f2466c7af7fef66cff84890f3d6`  
		Last Modified: Mon, 14 Dec 2020 22:43:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e21f19d1c6436150cd9720d1a3b8a2d7937e20e9df3df014bb2f0937d31eef1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.3 MB (309280824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611402ca59e7cc6f75f5e03c1e89655101b94ddeadc1494ba197ac3d28acb894`
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
# Thu, 21 Jan 2021 07:09:11 GMT
ENV ROS_DISTRO=foxy
# Thu, 21 Jan 2021 07:10:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:10:56 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 21 Jan 2021 07:10:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 07:10:57 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 07:11:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:12:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 07:12:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Jan 2021 07:12:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:12:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 07:12:48 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 07:12:49 GMT
ENV ROS1_DISTRO=noetic
# Thu, 21 Jan 2021 07:12:49 GMT
ENV ROS2_DISTRO=foxy
# Thu, 21 Jan 2021 07:13:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.9-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:14:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:14:29 GMT
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
	-	`sha256:9f91591140f1d30742b9bc74216ea65efb94af4c394cce84b7b2fe198767ae5e`  
		Last Modified: Thu, 21 Jan 2021 07:37:11 GMT  
		Size: 103.8 MB (103787544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b99cacb692debf9d4361dce6953ff14335b7d041eb854b15d5821e6856a5065`  
		Last Modified: Thu, 21 Jan 2021 07:36:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a208dbc4f03b742bef52fb1e5fce8691b1968159312ad723c181fcaeb88b0dd5`  
		Last Modified: Thu, 21 Jan 2021 07:37:37 GMT  
		Size: 61.0 MB (60960284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c5f3216884412ea3074277cc33323cd237873504b26931dd1a91442f07dc6d`  
		Last Modified: Thu, 21 Jan 2021 07:37:22 GMT  
		Size: 211.3 KB (211317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66752a00633f8d87929fc217ddf9325223ad15113d8b6b4c807c20a243960d4b`  
		Last Modified: Thu, 21 Jan 2021 07:37:22 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39324780393ceb2d62140c698f51132fcbcfca2bc48e3f4f652c9cf4215cf7de`  
		Last Modified: Thu, 21 Jan 2021 07:37:26 GMT  
		Size: 9.3 MB (9309437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9141363b3bbaca13476e46f05eb56577389f5c5f175dd9ae7e222753a1dae3`  
		Last Modified: Thu, 21 Jan 2021 07:37:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e566c9576c5996d73d9d99b0ba405ead78d1ecedd92bb8769fea25e936ae049b`  
		Last Modified: Thu, 21 Jan 2021 07:37:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5001c3a24669856860aee07650d2a052dc6404b2218029a471d401fdb5676a6`  
		Last Modified: Thu, 21 Jan 2021 07:38:15 GMT  
		Size: 76.1 MB (76142034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c884f87b2ed454477db6bdf42e71ba71878c5c2a093717cd1ce7c59108d930b`  
		Last Modified: Thu, 21 Jan 2021 07:37:57 GMT  
		Size: 25.0 MB (24994439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff9c0da17b48f6cb53e8689dc4bae10b9c650d59a147f4c9b46c522801d83e2`  
		Last Modified: Thu, 21 Jan 2021 07:37:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

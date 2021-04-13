## `ros:rolling-ros1-bridge-focal`

```console
$ docker pull ros@sha256:cbb79a5eb082d66429e5f670241e130060dce67a67a33ccd42d6b4a72dc7dfdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:b702d3fe119440dfde159641ac3f90cbd52293c3948e9d3779c6b07c57c861d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320761054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad7ce58f81f222fd29b4e40c5073911c0fb2c49e5dfe1740451175e5aa514fe`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 03 Apr 2021 00:53:06 GMT
ADD file:27277aee655dd263ee698d1f2fe17f0b1dbba740615bcac8642723a6ac0d62be in / 
# Sat, 03 Apr 2021 00:53:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 00:53:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 00:53:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 00:53:09 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 02:08:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 02:20:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 02:20:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 03 Apr 2021 02:33:42 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 03 Apr 2021 02:33:42 GMT
ENV LANG=C.UTF-8
# Sat, 03 Apr 2021 02:33:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 03 Apr 2021 02:36:34 GMT
ENV ROS_DISTRO=rolling
# Mon, 12 Apr 2021 19:00:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 12 Apr 2021 19:00:12 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Mon, 12 Apr 2021 19:00:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 12 Apr 2021 19:00:12 GMT
CMD ["bash"]
# Mon, 12 Apr 2021 19:01:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 12 Apr 2021 19:01:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 12 Apr 2021 19:01:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 12 Apr 2021 19:02:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 12 Apr 2021 19:02:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Mon, 12 Apr 2021 19:02:20 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Mon, 12 Apr 2021 19:02:21 GMT
ENV ROS1_DISTRO=noetic
# Mon, 12 Apr 2021 19:02:21 GMT
ENV ROS2_DISTRO=rolling
# Mon, 12 Apr 2021 19:03:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.9-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 12 Apr 2021 19:03:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.10.1-1*     ros-rolling-demo-nodes-cpp=0.14.0-1*     ros-rolling-demo-nodes-py=0.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 12 Apr 2021 19:03:48 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:a70d879fa5984474288d52009479054b8bb2993de2a1859f43b5480600cecb24`  
		Last Modified: Thu, 01 Apr 2021 15:20:06 GMT  
		Size: 28.6 MB (28569016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4394a92d1f8760cf7d17fee0bcee732c94c5b858dd8d19c7ff02beecf3b4e83`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6159c56c084c858f5de2416454ac0a49ddda47b764e4379c5d5a147c9bf5f`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7c5d2d7a6606006c3c9ad68491e77516419c59fceb2f4c04ca5580c96d8501`  
		Last Modified: Sat, 03 Apr 2021 02:40:16 GMT  
		Size: 1.2 MB (1182070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccd2266e6deaba5ba5682d19318df74543102cf36e0b3e2be8240cbd58404eb`  
		Last Modified: Sat, 03 Apr 2021 02:40:15 GMT  
		Size: 5.5 MB (5547325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2974076651535b81ed47daec0c9ac8a8a614de3b86c54d48a04c89ad19e07559`  
		Last Modified: Sat, 03 Apr 2021 02:40:13 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcd05d1e076faa0694af18a98a932e308a61016ec9d22d17a4a5d09ee624c5b`  
		Last Modified: Sat, 03 Apr 2021 02:43:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa1e95a491e1011c05bd5d893107c47f4bf45b9d273494616573b09db4a24ff`  
		Last Modified: Mon, 12 Apr 2021 19:05:48 GMT  
		Size: 104.4 MB (104372912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ff6e26da947927b44192b6354522593f1f6d60a2b2923599c528da51496d59`  
		Last Modified: Mon, 12 Apr 2021 19:05:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f1e60208630fcf34636311408b3bc8bc7bc7312f72f80b48a77031edb1f1ac`  
		Last Modified: Mon, 12 Apr 2021 19:06:11 GMT  
		Size: 66.5 MB (66549605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2ee70a693615ca0241b5759ef50995c37a2b1688de4b15c6d4d2d203e0d113`  
		Last Modified: Mon, 12 Apr 2021 19:06:00 GMT  
		Size: 212.0 KB (212018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211a0547fe610ebd4ca24c4514574d801fbcbdecadce46e0fabb06fcfe29690`  
		Last Modified: Mon, 12 Apr 2021 19:06:00 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e07387dcb51bd6d7f980d9677f6ba1b3ad9f270e718fc60b18d653290e9f1d`  
		Last Modified: Mon, 12 Apr 2021 19:06:04 GMT  
		Size: 21.7 MB (21702412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36b40a3620cc50d0a4a25a91540cf3eb902501e6cc2caef4f69c37c16452e94`  
		Last Modified: Mon, 12 Apr 2021 19:06:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd7a3d11eeaa9d74425d9423b1b4889acb97be264bb721421ba1f23e0b8705e`  
		Last Modified: Mon, 12 Apr 2021 19:06:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b971343bc312d0d1c4daa516086bf21035d245647019296ef4d7529c01252b0`  
		Last Modified: Mon, 12 Apr 2021 19:06:42 GMT  
		Size: 78.4 MB (78406090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc483782a60db1fba49e05d9f3946b34b8c438cf44a4f211ab176957ea654e7f`  
		Last Modified: Mon, 12 Apr 2021 19:06:30 GMT  
		Size: 14.2 MB (14214055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a287651e552831cc1ece3c56f72780cd61c2c51f519460346572ab56a4881d`  
		Last Modified: Mon, 12 Apr 2021 19:06:26 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4960c7df6387389b1f5dc1cd5b61a319edad0f450493fbdfd22d0e14f0230790
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.0 MB (309040774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3df0ee0215c92cd2bbb93b454a475ca9d930e7f10fa62ed2e0a38c8f508d1d2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 03 Apr 2021 04:10:04 GMT
ADD file:5a9b188c70f1f07ae9d68f3eb7aa18a1683faf50d5ff20eda1b04db3255877b9 in / 
# Sat, 03 Apr 2021 04:10:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 04:10:11 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 04:10:13 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 04:10:14 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 06:25:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 06:26:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 06:26:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 03 Apr 2021 06:35:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 03 Apr 2021 06:35:56 GMT
ENV LANG=C.UTF-8
# Sat, 03 Apr 2021 06:35:57 GMT
ENV LC_ALL=C.UTF-8
# Sat, 03 Apr 2021 06:41:20 GMT
ENV ROS_DISTRO=rolling
# Mon, 12 Apr 2021 18:37:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 12 Apr 2021 18:37:30 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Mon, 12 Apr 2021 18:37:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 12 Apr 2021 18:37:32 GMT
CMD ["bash"]
# Mon, 12 Apr 2021 18:38:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 12 Apr 2021 18:38:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 12 Apr 2021 18:38:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 12 Apr 2021 18:39:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 12 Apr 2021 18:39:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Mon, 12 Apr 2021 18:39:40 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Mon, 12 Apr 2021 18:39:41 GMT
ENV ROS1_DISTRO=noetic
# Mon, 12 Apr 2021 18:39:42 GMT
ENV ROS2_DISTRO=rolling
# Mon, 12 Apr 2021 18:40:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.9-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 12 Apr 2021 18:41:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.10.1-1*     ros-rolling-demo-nodes-cpp=0.14.0-1*     ros-rolling-demo-nodes-py=0.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 12 Apr 2021 18:41:06 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:2b20d1a80822f7dbd2175f235caa068029e82a265d0924d4f4d39c1bf9dc7f9b`  
		Last Modified: Thu, 01 Apr 2021 08:25:41 GMT  
		Size: 27.2 MB (27176807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e993c4ee9ad2dd0f069e7c34bbf137c835c5a2c2cc3f111e37fba05c79c1d7`  
		Last Modified: Sat, 03 Apr 2021 04:11:51 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2befefc5146bc156f83e891873a69526513f1e942e3d2bf68129f1e2fa17613`  
		Last Modified: Sat, 03 Apr 2021 04:11:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b425e160ecdc1ce2e8f2c9394df0bf787e591ab7983fa386fa029ed26a92c1`  
		Last Modified: Sat, 03 Apr 2021 06:48:05 GMT  
		Size: 1.2 MB (1183308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19dbee98155e4cab1ca612d6d81cf3e8713fb2f87fc42d92530e2635fd1ba8f`  
		Last Modified: Sat, 03 Apr 2021 06:48:04 GMT  
		Size: 5.5 MB (5513345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874fc4821a261dd3d76266f77f06518b341b2bea50a79bd0dbc4fd367823c520`  
		Last Modified: Sat, 03 Apr 2021 06:48:03 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c452bc5faf1f1e451a20172334f340dd4489b450beb68b361113cbb662c759`  
		Last Modified: Sat, 03 Apr 2021 06:52:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0ab3c512753b244538a8ab37fab37708be74125f14fd61ffbe824570feacef`  
		Last Modified: Mon, 12 Apr 2021 18:43:19 GMT  
		Size: 100.8 MB (100802871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff110debec88d4efc22b471c583e4d003b48447246d2b20184c57cb87516c98`  
		Last Modified: Mon, 12 Apr 2021 18:42:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66add836c70786e8b06214211a3a496542847ab4595abaccaf03001c287f3ebe`  
		Last Modified: Mon, 12 Apr 2021 18:43:42 GMT  
		Size: 60.9 MB (60920449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a46eb6f6958451e1d6267cb15b3bba62854011d8205a9ab8a43cfc4b5ea021`  
		Last Modified: Mon, 12 Apr 2021 18:43:27 GMT  
		Size: 212.0 KB (212012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70793ad075a9a5d93af0bb9c61a605bfb4b5690b50ad58e41f4c162a6cb68a2`  
		Last Modified: Mon, 12 Apr 2021 18:43:27 GMT  
		Size: 2.1 KB (2066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db13371532fe154e67a3468ae8388048a4c6f775fe8afe44fd0e9ba270d28271`  
		Last Modified: Mon, 12 Apr 2021 18:43:32 GMT  
		Size: 21.1 MB (21055526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef06967f9363c364da0728d94cc7141bde4aa70d7e5c8b405aa11808cf62b809`  
		Last Modified: Mon, 12 Apr 2021 18:43:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4070ab70039d0e2def53f0a72110212ed20734d0c53c04d2215a3d5232573a85`  
		Last Modified: Mon, 12 Apr 2021 18:43:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3d23b7c44c601016f892967d64fa18067d7929e5f648d0c036ff9035f86071`  
		Last Modified: Mon, 12 Apr 2021 18:44:16 GMT  
		Size: 78.4 MB (78352387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0a988d82bc066a80d5cffecbe482e57a8c59265771cce49c60e9d97b7c51d5`  
		Last Modified: Mon, 12 Apr 2021 18:43:56 GMT  
		Size: 13.8 MB (13818490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf49b35da8841f21a123fd6cbea58d09e8785960096a3157ca598702311d6f31`  
		Last Modified: Mon, 12 Apr 2021 18:43:51 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

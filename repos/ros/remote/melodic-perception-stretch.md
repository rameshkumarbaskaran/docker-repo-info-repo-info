## `ros:melodic-perception-stretch`

```console
$ docker pull ros@sha256:665b16625a1bc2031a2878b952f37a354f1bde0557baf9793f7702b329efeda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-perception-stretch` - linux; amd64

```console
$ docker pull ros@sha256:763db42a5d92b1826bd35b903cdd339fdf277577f81dca703265eb1b01cb355a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **828.0 MB (828012050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c34dff5ea722dff4dba70e4385b39084e5fd258c4ad9ac6ddeb19389237e375`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:29:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:29:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 22 Jul 2020 20:29:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 22 Jul 2020 20:29:42 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 20:29:42 GMT
ENV LC_ALL=C.UTF-8
# Wed, 22 Jul 2020 20:29:42 GMT
ENV ROS_DISTRO=melodic
# Wed, 22 Jul 2020 20:31:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:31:35 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 22 Jul 2020 20:31:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 22 Jul 2020 20:31:36 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:32:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:32:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 22 Jul 2020 20:33:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:36:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40906fc9f8b2b8a56bcfb4722f5852e4b44c411ca4920de277f8918bda8cf4f`  
		Last Modified: Wed, 22 Jul 2020 20:45:35 GMT  
		Size: 6.9 MB (6866450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6d372ce5eef2222822237de281a86ffbf352f436e4a2d0c8c6004bff4b1bab`  
		Last Modified: Wed, 22 Jul 2020 20:45:34 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18fe21b5c4a5260fb018eb41aeea35891bd8c794ac4577cc34bdf43e09d0fe3`  
		Last Modified: Wed, 22 Jul 2020 20:45:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78d712f176959e0679792cfa27f71e34bab75b51798bcc66a97b4895e3c656e`  
		Last Modified: Wed, 22 Jul 2020 20:46:52 GMT  
		Size: 269.9 MB (269880803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c160d001a2a5b6a00b738e8015b92469234b60e6f5dfbecf7b4aa4699b0590be`  
		Last Modified: Wed, 22 Jul 2020 20:45:33 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17e9bc7f05fd42e803d8842676c9843e8fdfdc3ad163a1725dbe58fbe832a5d`  
		Last Modified: Wed, 22 Jul 2020 20:47:18 GMT  
		Size: 70.1 MB (70149773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac321b75213e5c39b58eb62ac16279838200f9ae2a58fd1fb7cf79ed08c441fc`  
		Last Modified: Wed, 22 Jul 2020 20:46:56 GMT  
		Size: 254.0 KB (253982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac773c927ecffa716e5d95666c65c78f2eaf4b8010c7cd52ca68c2dcb98860a`  
		Last Modified: Wed, 22 Jul 2020 20:47:17 GMT  
		Size: 55.1 MB (55051919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f54ba4a55487620522e5ada2a86ec24175af4471e9ff39290a6969d81eccfcb`  
		Last Modified: Wed, 22 Jul 2020 20:49:06 GMT  
		Size: 380.4 MB (380437633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:49797cb4acd716423761642145b0955a16f0142a51cd7e839be44d36bc14707b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.5 MB (749481459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4549a957d7b2c9fd15ac88cc5f4310f106d9568db94dd8a00eca03515cef4862`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 10:02:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 10:02:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Aug 2020 10:02:24 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Aug 2020 10:02:25 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 10:02:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Aug 2020 10:02:26 GMT
ENV ROS_DISTRO=melodic
# Tue, 04 Aug 2020 10:05:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 10:05:49 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 04 Aug 2020 10:05:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Aug 2020 10:05:56 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 10:06:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 10:07:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Aug 2020 10:08:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 10:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac412b2554318f4b6050db40ac7104b507a6e40edba068b5a1c3e30ffdf3c35e`  
		Last Modified: Tue, 04 Aug 2020 10:31:28 GMT  
		Size: 6.4 MB (6438845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01136f9bde07ae51236af3dbff422307927028bbc5414c25554993f0595bac8a`  
		Last Modified: Tue, 04 Aug 2020 10:31:26 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a1883d43a0d6aeea6bba737aa6c11a01844b88be21462e4055ccb98e91d892`  
		Last Modified: Tue, 04 Aug 2020 10:31:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90009b0420756860fcd9aa0ce9221d6c3972877e576855a480e34a4e4281651`  
		Last Modified: Tue, 04 Aug 2020 10:32:37 GMT  
		Size: 225.0 MB (224953525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736029edcfd0de1adc7218032511d84d44a5cf7909c2de0c35f3e311ee13292d`  
		Last Modified: Tue, 04 Aug 2020 10:31:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f52684428f2f1c5ddb65bb4ac4804d92e6f187ad94a5500e31d3f9522ca120c`  
		Last Modified: Tue, 04 Aug 2020 10:33:00 GMT  
		Size: 64.8 MB (64840268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df4438146edf4f0172672fb2eed6b4759c6dd5807cba1560f036b0476054e68`  
		Last Modified: Tue, 04 Aug 2020 10:32:43 GMT  
		Size: 254.9 KB (254908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd47fd5638bcf1fa58b899ba6e5cc0ae8479595dff5c3c3c65b35bab46c1c25`  
		Last Modified: Tue, 04 Aug 2020 10:33:15 GMT  
		Size: 53.2 MB (53230719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9eb31f3abcf3d69e702285fc12d729d02bed32bc2ca3465db1481d3eed5ac6`  
		Last Modified: Tue, 04 Aug 2020 10:35:09 GMT  
		Size: 356.6 MB (356589733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

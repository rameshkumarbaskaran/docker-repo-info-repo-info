## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:15b6ceafa0d41f86985d03f098ce1ab20f654032b14739a2d0218690c92c6bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:26ee7d27c07e131afbe2b0d8df3a479c7e41931f5116c36f0815ebe5952b9d6d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.9 MB (484863624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0a98162000767aad3a21a3320626245a63247696805bb8e28bb08b39a7c999`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:50 GMT
ADD file:1fb366429a5df94c7ba642735d6aa77e201f90e0843de03721a6ad19f80ee4e0 in / 
# Tue, 04 Oct 2022 23:26:50 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 10:15:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:15:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 10:15:10 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 10:15:10 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 10:15:10 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 10:15:10 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 10:16:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:16:49 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 10:16:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 10:16:49 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 10:17:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:17:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 10:17:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:18:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b6d6a76ebdbe1e858fec4564af6c6c3fe9e9bf1c502c8c8a51afd0fcf3374d44`  
		Last Modified: Tue, 04 Oct 2022 23:31:15 GMT  
		Size: 50.4 MB (50441102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2341aa83c173ccc7896ed46aadb5f8da7ef58882bd50ab70db04adad01c7dd54`  
		Last Modified: Wed, 05 Oct 2022 10:52:43 GMT  
		Size: 10.9 MB (10893675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4707ffddc54db884ea0f0b8d3dcb59efecf4b23f05ca9678cdb9093afeb503ed`  
		Last Modified: Wed, 05 Oct 2022 10:52:42 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189ff615727a275e72ab0b25ee32ab5bbaf9038ec984ac9590b05ec0bd699420`  
		Last Modified: Wed, 05 Oct 2022 10:52:42 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02002ab3d47e892389b5c1698d3762ba599087c17a75d1c89b38eba2d10e9e73`  
		Last Modified: Wed, 05 Oct 2022 10:53:15 GMT  
		Size: 239.2 MB (239205312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b538c244b3c01ac7f43cbbe81f3828c21d135d04e3f09c2be3cbd996f74e2d`  
		Last Modified: Wed, 05 Oct 2022 10:52:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df699501c681c16e834b1d4c6a0020da7a337123f2599fa0138c7a689abe2c00`  
		Last Modified: Wed, 05 Oct 2022 10:53:34 GMT  
		Size: 86.6 MB (86571557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c877ef0ff6f06ed582cc68bf1bb2a9f3febf8e8d6812c86c77fa110bf09fe22`  
		Last Modified: Wed, 05 Oct 2022 10:53:22 GMT  
		Size: 324.6 KB (324645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6360754d0398a4f26fe2e6909f0d860b818f474a42c16d8f1fb6232def5a53d`  
		Last Modified: Wed, 05 Oct 2022 10:53:33 GMT  
		Size: 76.0 MB (75976232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c893fae4daed6c6414cc2281b66f2fc63c8c815eff25b0833189f66bfbef8a40`  
		Last Modified: Wed, 05 Oct 2022 10:53:44 GMT  
		Size: 21.4 MB (21448689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:121b3e7b2ca5e8da32dfd01553c6ac1900af316462c74b3d1e9e796edb3aa97e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (424049494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246b8ee8dc3e0e2b08a175ccb03cab632821d038b2c68104063a478f2f6db59`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:06 GMT
ADD file:304a544562f139d7ab96511b7f1e059966cf90169117e835072f132468bf91c8 in / 
# Tue, 13 Sep 2022 02:11:07 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:56:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:56:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 13 Sep 2022 12:56:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 13 Sep 2022 12:56:44 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 12:56:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 13 Sep 2022 12:56:46 GMT
ENV ROS_DISTRO=noetic
# Tue, 13 Sep 2022 12:58:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:58:13 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 13 Sep 2022 12:58:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 13 Sep 2022 12:58:16 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:58:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:59:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 13 Sep 2022 12:59:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:00:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e2406a452ad23ba9085e0708f5e15309206a618eb828aa307becbb239414392f`  
		Last Modified: Tue, 13 Sep 2022 02:16:42 GMT  
		Size: 49.2 MB (49228261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ec060bafb85a1c4fb32a456ed970628f926c8b985fb90ed243d4c7d4d96d6f`  
		Last Modified: Tue, 13 Sep 2022 13:06:39 GMT  
		Size: 10.7 MB (10689346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f272eefce84866a380e21ef07b830d72077f566702b1dc8432c9bd460423b18`  
		Last Modified: Tue, 13 Sep 2022 13:06:37 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d4d36aa5f5718c160f03a683078a7a6a33c621f22763243a6cba5a31fec922`  
		Last Modified: Tue, 13 Sep 2022 13:06:37 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4b761086d86c468aad5c1c5a5a8b2904284754e9efa06d510edcc4b50a638`  
		Last Modified: Tue, 13 Sep 2022 13:07:08 GMT  
		Size: 184.5 MB (184463015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15616e1c2e135cd3c48087cab44685dcd6953ceeb63f92b3ae64f09578961f44`  
		Last Modified: Tue, 13 Sep 2022 13:06:37 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00b67bbdb5f9e8d9d7db843b5b3004d079a09724f3ac83c20eead20bcb6536e`  
		Last Modified: Tue, 13 Sep 2022 13:07:27 GMT  
		Size: 84.4 MB (84371420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee5988a175290b2b265a5b3255b001f45b42ac83f55aa18d418183c2ee5507f`  
		Last Modified: Tue, 13 Sep 2022 13:07:17 GMT  
		Size: 322.2 KB (322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583b0ab9e5f1ddccc929af774d99cf94fc8cb22ca41e734283678b1dad875c36`  
		Last Modified: Tue, 13 Sep 2022 13:07:26 GMT  
		Size: 73.9 MB (73865756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b28d909643f86dd58e2f1738edd414e9ab03785021a60e39d8296406b1c7b12`  
		Last Modified: Tue, 13 Sep 2022 13:07:38 GMT  
		Size: 21.1 MB (21107140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

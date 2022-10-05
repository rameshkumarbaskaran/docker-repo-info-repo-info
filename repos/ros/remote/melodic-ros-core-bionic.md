## `ros:melodic-ros-core-bionic`

```console
$ docker pull ros@sha256:8cc338266ee97da2e11d4fc03f5441a1ce29995b51ef6ac1f8ba6a551b31732e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:54049e85de367cf82961c3a37fc6af88ae936e8563c1ebfc54203c605c3d414c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291976962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367edf3bdb41bd746cf1277a348f7424c9dc06cbba560ee413e58c4a8375791d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:04 GMT
ADD file:ed601c56cf74241eeb1971b24ed969fb855cd2b9330276d3c5779ecdb0b28364 in / 
# Tue, 04 Oct 2022 23:35:04 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 09:49:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 09:49:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 09:49:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 09:49:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 09:49:44 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 09:49:44 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 09:49:44 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Oct 2022 09:53:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 09:53:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 09:53:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 09:53:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e706e0a9f42365312b366bf4caa22f3cdd8fc7fd8f6f49b4dd3782711f66aca7`  
		Last Modified: Tue, 04 Oct 2022 11:37:26 GMT  
		Size: 26.7 MB (26711852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ec163f2e73ca4c7df5142df330fb9169325367e235b65c457afcc3bf320f35`  
		Last Modified: Wed, 05 Oct 2022 10:47:14 GMT  
		Size: 831.0 KB (831002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc154e3f17c6b6f2816c50c8a5bdf831cd4d8813015cacf86568d64746596b6`  
		Last Modified: Wed, 05 Oct 2022 10:47:12 GMT  
		Size: 4.9 MB (4873641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfe6435278fe5856644c183f90cfb982b207bddda62c63a94d6a938acffaa85`  
		Last Modified: Wed, 05 Oct 2022 10:47:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d8283d791cae1e7c3329c4a1d8f4bc0476769b04e9ce92d6a97fe84026c059`  
		Last Modified: Wed, 05 Oct 2022 10:47:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab60f51f309df710bd88888532e7f25291a9e1d1f54e49a7af43e0771994831f`  
		Last Modified: Wed, 05 Oct 2022 10:48:02 GMT  
		Size: 259.6 MB (259558625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b4b730c4ae1b037fe75c6ca063e9c629e1ed238654786a73fabd60b4ed9719`  
		Last Modified: Wed, 05 Oct 2022 10:47:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:25641d2af939d01a628e61c09d17c0bc244526dc98f0b583fb057a881991c3b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266244546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dcc149de655352815668645267efd86494aa63248e0331e330877fa128ad808`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 19:33:23 GMT
ADD file:45c82fca220161f3905a06e276f12ec0cb3be5c099cca70bb6d495da10088f7d in / 
# Tue, 06 Sep 2022 19:33:24 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 20:02:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:02:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:02:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 06 Sep 2022 20:02:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 06 Sep 2022 20:02:33 GMT
ENV LANG=C.UTF-8
# Tue, 06 Sep 2022 20:02:33 GMT
ENV LC_ALL=C.UTF-8
# Tue, 06 Sep 2022 20:02:33 GMT
ENV ROS_DISTRO=melodic
# Tue, 06 Sep 2022 20:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:04:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 06 Sep 2022 20:04:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 06 Sep 2022 20:04:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:074d633b5bde02245e333b110dde5850e06ea4ebefe4283af6e4dfd8d462b170`  
		Last Modified: Tue, 06 Sep 2022 19:35:07 GMT  
		Size: 22.3 MB (22305954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0da4089b68bf46009d284fa16ca1d621c7049f3db1038f87fdc58aa3e52059`  
		Last Modified: Tue, 06 Sep 2022 20:09:19 GMT  
		Size: 832.1 KB (832054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb5783e1925df093ff571a9432fe1c845b3ece17f25ceaf82d5608e22b05bd1`  
		Last Modified: Tue, 06 Sep 2022 20:09:17 GMT  
		Size: 4.1 MB (4088159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292f716a6e78a03f97c202a01a3e1e98cf10bed5364c7c32c839c867d13681a6`  
		Last Modified: Tue, 06 Sep 2022 20:09:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ca0dfda7d5b871d65a21978a3eb27b0e0df4356a07344a412a47884c99fa97`  
		Last Modified: Tue, 06 Sep 2022 20:09:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f2026bdd33971a08db14214c57a9844a8b07c0419dd4f91cdb452cc945d2da`  
		Last Modified: Tue, 06 Sep 2022 20:10:01 GMT  
		Size: 239.0 MB (239016534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409e6ba5da3e6f8d9bfe01490e9a5fdbc6c46106af86015aa53de972cf17fb92`  
		Last Modified: Tue, 06 Sep 2022 20:09:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8c907a5ab5ab0492604cc0941aedd51ad7bfbe428f07a73d83e78afba257130e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281336466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288b6c8526ade912c05612c7d7023cc9fe381a7736df312efd8b7444ff764137`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:49:02 GMT
ADD file:26cb5ace98a4462b36211bf28f1e73781dd6d8984350d9bd53243dbe50ae180c in / 
# Tue, 06 Sep 2022 18:49:02 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:39:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:39:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:39:34 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 06 Sep 2022 19:39:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 06 Sep 2022 19:39:37 GMT
ENV LANG=C.UTF-8
# Tue, 06 Sep 2022 19:39:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 06 Sep 2022 19:39:39 GMT
ENV ROS_DISTRO=melodic
# Tue, 06 Sep 2022 19:41:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:41:03 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 06 Sep 2022 19:41:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 06 Sep 2022 19:41:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d30cf2a6a25aea48a115837d149468c8de7df7fb51f210b9fa1173c065f7b34c`  
		Last Modified: Tue, 06 Sep 2022 18:50:34 GMT  
		Size: 23.7 MB (23734076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c4f657f16f312fa6dcdfe1497bf20b105de50db3390adc504f994c2e9f5b26`  
		Last Modified: Tue, 06 Sep 2022 19:47:40 GMT  
		Size: 831.3 KB (831309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0409a4a76860508a3bb6248ebf7f6c0e2710dcd922c36a4959dd70bc0bd27e`  
		Last Modified: Tue, 06 Sep 2022 19:47:38 GMT  
		Size: 4.3 MB (4265677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8c9b1355942f3d60e38808189d3e6d165d5be537fefc37fa08042bc39b874b`  
		Last Modified: Tue, 06 Sep 2022 19:47:37 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890877cc8e4438ec9389664d9d410292ebcaed1e9f7bb0790d11083308930c25`  
		Last Modified: Tue, 06 Sep 2022 19:47:37 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d08560eb8db9469de77a96e0f07ccc2d8735796b72d3360b34d33ea2ea3e9e`  
		Last Modified: Tue, 06 Sep 2022 19:48:12 GMT  
		Size: 252.5 MB (252503601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7dfbfc923a78aa6af356834ddc818505716f9ed414c5c15cd9563f4df2d3a4`  
		Last Modified: Tue, 06 Sep 2022 19:47:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

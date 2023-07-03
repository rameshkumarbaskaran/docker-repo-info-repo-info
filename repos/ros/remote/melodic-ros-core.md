## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:9466d74c94f2d76ebe2c4c391ce045fd9afe188d701f96d2bf9e5034e14d5eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:0c326e3a90df05d487c43d7b5e637c779baa9ca90a01de4faafc928f91d2f029
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292029620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7f0a9409c472babbcea610d2fedd908601108b9d4fe1b3a227de7a827cafc4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:55:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:51:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 19:22:20 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Mon, 03 Jul 2023 19:22:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Mon, 03 Jul 2023 19:22:22 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jul 2023 19:22:22 GMT
ENV LC_ALL=C.UTF-8
# Mon, 03 Jul 2023 19:22:22 GMT
ENV ROS_DISTRO=melodic
# Mon, 03 Jul 2023 19:26:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 19:26:18 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 03 Jul 2023 19:26:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 03 Jul 2023 19:26:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27456075680427d55e79ddce0ccec278d1f81ab5181d13386de5ac3f085b90`  
		Last Modified: Fri, 02 Jun 2023 01:02:13 GMT  
		Size: 818.9 KB (818915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8c91ad7650f55a57d952458067fa5d43fc42f60aa1300eac0321468efd7f1d`  
		Last Modified: Fri, 02 Jun 2023 02:17:44 GMT  
		Size: 4.9 MB (4878354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0683d606786339b4368e89c6aaf1c72169b6aa7e6630aefddaeac503bc6552bc`  
		Last Modified: Mon, 03 Jul 2023 19:35:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66495e509f4c45b21e332a761ce4b1d4f207417e3e0b51b3c71dad8e9697cce`  
		Last Modified: Mon, 03 Jul 2023 19:35:21 GMT  
		Size: 2.4 KB (2406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c731a0490674b377c6cd43c7d5012868bf98a22b30417a9bbbc9f016d73d07c`  
		Last Modified: Mon, 03 Jul 2023 19:35:53 GMT  
		Size: 259.6 MB (259612161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f9d35f26e100c81e0e5c8ceecdf6a25d7beb14187fb876d869b81530cf831a`  
		Last Modified: Mon, 03 Jul 2023 19:35:21 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:0ebb36f6deecdfb596ad6c0e4c95e1b01672dc7095a9238cec60889803eaa1b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266301185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1400365d4a6633beab44143961a55984564af64d98210e35619edc08337098`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:52:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:52:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:52:20 GMT
ADD file:d570ab6bd7d664cc6547b6ae228cf825333d9d841969911c7d62afe3ed440803 in / 
# Tue, 30 May 2023 09:52:21 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:03:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:03:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 19:35:29 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Mon, 03 Jul 2023 19:35:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Mon, 03 Jul 2023 19:35:30 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jul 2023 19:35:31 GMT
ENV LC_ALL=C.UTF-8
# Mon, 03 Jul 2023 19:35:31 GMT
ENV ROS_DISTRO=melodic
# Mon, 03 Jul 2023 19:40:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 19:40:04 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 03 Jul 2023 19:40:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 03 Jul 2023 19:40:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76bc0c6b06fc92c1f911be6147b55b6430301b80e4062178329c4fa8a0f79f51`  
		Last Modified: Thu, 01 Jun 2023 23:54:31 GMT  
		Size: 22.3 MB (22312178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296f87f37d6a7831a2d27cf9ba67dbb404857632b477ce335ecbe521cd84db2d`  
		Last Modified: Fri, 02 Jun 2023 00:15:23 GMT  
		Size: 820.3 KB (820335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a424966fc7947ef55ca4db8ed69abeb762dbe613d82cb7b6c248b55d4a76fe8d`  
		Last Modified: Fri, 02 Jun 2023 00:15:22 GMT  
		Size: 4.1 MB (4090754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ab58b432ab762c3e066cf1bbb2cf2cb6e184f7ba4d5eccebe3002f9e0d7f25`  
		Last Modified: Mon, 03 Jul 2023 19:49:13 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31905fc086a9d671f7d3e78111401be4f09982743b2729cab2cedb7226b57932`  
		Last Modified: Mon, 03 Jul 2023 19:49:13 GMT  
		Size: 2.4 KB (2406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac92b51d2d7d1dac38b1cc25ba69f7d4e96a35293a72149ba318d3cf92376ffd`  
		Last Modified: Mon, 03 Jul 2023 19:49:46 GMT  
		Size: 239.1 MB (239075082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e085617659d8479bc89c2ae48b56fbeac53b0f2a62edaceb1393bca8ae6dbb1`  
		Last Modified: Mon, 03 Jul 2023 19:49:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:341577c558cc811914067f5d0b854c89fe1fdc8f96907671f0e275f7ec9ee129
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281548442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be19dee15a45e0dd38b7693830b6100dfa265640333034efbd53df11195376ff`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:07:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 18:54:30 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Mon, 03 Jul 2023 18:54:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Mon, 03 Jul 2023 18:54:31 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jul 2023 18:54:31 GMT
ENV LC_ALL=C.UTF-8
# Mon, 03 Jul 2023 18:54:32 GMT
ENV ROS_DISTRO=melodic
# Mon, 03 Jul 2023 18:58:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 03 Jul 2023 18:59:00 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 03 Jul 2023 18:59:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 03 Jul 2023 18:59:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f5d58f6c858f92b45f1d3e366bcabef3c6821ccaa9ee17c59beb643029cb4d`  
		Last Modified: Fri, 02 Jun 2023 00:41:19 GMT  
		Size: 819.0 KB (818994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9e738cf9edf30ed3cf9686d84733d2d3d3ee28a85c58ada09fabd9660ed336`  
		Last Modified: Fri, 02 Jun 2023 00:41:18 GMT  
		Size: 4.5 MB (4461671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb15c91065685951357c563d50225475bf62ccf00e185b08b5d5aa0d828f9e9`  
		Last Modified: Mon, 03 Jul 2023 19:08:53 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaf40387f745b8b6c023a4647f5ce4a9f784107d4ba1d4356d41f6ccd21a5d9`  
		Last Modified: Mon, 03 Jul 2023 19:08:53 GMT  
		Size: 2.4 KB (2404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d28df4590da4d1b3e217e5b8b28fed95ce13c54228ee8335465c1b72839ef3c`  
		Last Modified: Mon, 03 Jul 2023 19:09:17 GMT  
		Size: 252.5 MB (252524042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffda3f020806b222794eaaa7b5f1cf412f7ebf13aad2e650fd36980f6649787`  
		Last Modified: Mon, 03 Jul 2023 19:08:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

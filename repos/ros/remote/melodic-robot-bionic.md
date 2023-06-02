## `ros:melodic-robot-bionic`

```console
$ docker pull ros@sha256:99451130e69e2cba6e7e5b779a163d22664722a01b2bae0700e2d2a5e99f8c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot-bionic` - linux; amd64

```console
$ docker pull ros@sha256:23456582011b89ff5a83e718b36bbcc9bb96f689f430f702de455580c981dfa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.8 MB (448835699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b9d9052510148a9741a3d24dba79d85bfabca8b35f04cdfde4e4cdd9aa00c6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 May 2023 09:41:51 GMT
ARG RELEASE
# Fri, 12 May 2023 09:41:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:41:52 GMT
ADD file:47682dd3869ca8e57ceb15f69a6ac7c9048d4d42c7a99a976e597cf072423c12 in / 
# Fri, 12 May 2023 09:41:53 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 01:04:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:05:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:05:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 May 2023 01:05:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 16 May 2023 01:05:05 GMT
ENV LANG=C.UTF-8
# Tue, 16 May 2023 01:05:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 May 2023 01:05:05 GMT
ENV ROS_DISTRO=melodic
# Tue, 16 May 2023 01:08:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:08:45 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 May 2023 01:08:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 May 2023 01:08:45 GMT
CMD ["bash"]
# Tue, 16 May 2023 01:09:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:09:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 May 2023 01:10:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:11:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c67806d7e72dd941e600bad2eabe920a17ba1852b325b63900c819ffeae646fb`  
		Last Modified: Tue, 16 May 2023 01:01:48 GMT  
		Size: 26.7 MB (26715509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8112c7660661f5d395aac99b0d2403ccaaf47cfce01b40167688a866847d540`  
		Last Modified: Tue, 16 May 2023 01:17:48 GMT  
		Size: 819.1 KB (819098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64664c88569b54e7b2cace7a7eff36f63ca10a75b05e5c1ddceb69bbff1d387b`  
		Last Modified: Tue, 16 May 2023 01:17:47 GMT  
		Size: 4.9 MB (4878519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20548c67c76407d9f268011684621401f1bb204c67b556072a06759d86b2cd82`  
		Last Modified: Tue, 16 May 2023 01:17:46 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b96bc2cae0fba817ecce5d15aafad4eee15610dfe2178708ed47f732f7f71bd`  
		Last Modified: Tue, 16 May 2023 01:17:46 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60000963f8bb247e6b22511e73ce54d4b3fefb24047ab49992acd24f8272aab5`  
		Last Modified: Tue, 16 May 2023 01:18:20 GMT  
		Size: 259.6 MB (259592143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af96a47a2aa7f522fcdf38f50ca1ff4abda4c7efd140a1d960f59b90f47d7788`  
		Last Modified: Tue, 16 May 2023 01:17:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b12ba5acbea014d663262f916b8adc37a9271199290d917abd458538df9cb70`  
		Last Modified: Tue, 16 May 2023 01:18:38 GMT  
		Size: 70.5 MB (70459679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41bbf0250a9904f7b67e9257aa660ab936db8911b99cd58d9350b109b920e31`  
		Last Modified: Tue, 16 May 2023 01:18:29 GMT  
		Size: 282.3 KB (282294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70f25d5aeddde8c1ec7ab0e2e9b51e8c30c5e7d69ad7cb00cb679682e3a47b3`  
		Last Modified: Tue, 16 May 2023 01:18:40 GMT  
		Size: 75.0 MB (75000304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63750a48b8c413627810e36f792a3f745a8f70ef9615e698c1486f634756d35`  
		Last Modified: Tue, 16 May 2023 01:18:52 GMT  
		Size: 11.1 MB (11086307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:924aac9793d2bd2e6c4155606aa3abec0612fbf4d0048b7f18a33f4206eeb59a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 MB (396501012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba414ade9b7721a44ab4ba78577adaaddac9ed3a7f1ce78c19eedd75d70afff`
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
# Fri, 02 Jun 2023 00:03:51 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Jun 2023 00:03:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Jun 2023 00:03:53 GMT
ENV LANG=C.UTF-8
# Fri, 02 Jun 2023 00:03:53 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Jun 2023 00:03:53 GMT
ENV ROS_DISTRO=melodic
# Fri, 02 Jun 2023 00:07:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:07:03 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Jun 2023 00:07:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Jun 2023 00:07:04 GMT
CMD ["bash"]
# Fri, 02 Jun 2023 00:07:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:07:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Jun 2023 00:08:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:09:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:d6f2b5759d6a592db8d9e7c54cea41255e28a308bb00dd901b0b89e127833484`  
		Last Modified: Fri, 02 Jun 2023 00:15:21 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fe4f77d9ba9445f2717bc343def12bf6a5abffaaea9978f6a7cd08e9dfdd96`  
		Last Modified: Fri, 02 Jun 2023 00:15:21 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ed06e4959894fd0c27932146a90ade048f580b919f2003dc021fe1a3b771c7`  
		Last Modified: Fri, 02 Jun 2023 00:15:54 GMT  
		Size: 239.1 MB (239083601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028706c953b925fc2ae8b0353286f1e65b796003820978cacf6b3fafd5b523d3`  
		Last Modified: Fri, 02 Jun 2023 00:15:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a6586e09f1cb6a3e98681e7381415216b056728fc1638e63d0dfb7185bd95e`  
		Last Modified: Fri, 02 Jun 2023 00:16:10 GMT  
		Size: 55.0 MB (55033923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d0b06f450c92b4d108057aa9ea1678dd83381dde934812520c7557e827262f`  
		Last Modified: Fri, 02 Jun 2023 00:16:03 GMT  
		Size: 283.5 KB (283459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e9ec93d69d137562906fd1dfdef9c60300d24a8dc97255f8d2d9621b30a922`  
		Last Modified: Fri, 02 Jun 2023 00:16:13 GMT  
		Size: 64.8 MB (64751236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42626b24ca50691c98bff90cb9ea40c7f1c277b27d97bfc02f87438d4f077fc3`  
		Last Modified: Fri, 02 Jun 2023 00:16:26 GMT  
		Size: 10.1 MB (10123679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5c38cd9e5f4ba154f14b77838703fa1daf80c3e12f8adac57326c686725c1dba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.1 MB (423096796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e5853794e0c0d3f0eaff7ba2b450d0a7b072301bb6592f88addcd972b47899`
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
# Fri, 02 Jun 2023 00:07:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Jun 2023 00:08:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Jun 2023 00:08:00 GMT
ENV LANG=C.UTF-8
# Fri, 02 Jun 2023 00:08:00 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Jun 2023 00:08:00 GMT
ENV ROS_DISTRO=melodic
# Fri, 02 Jun 2023 00:11:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:11:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Jun 2023 00:11:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Jun 2023 00:11:11 GMT
CMD ["bash"]
# Fri, 02 Jun 2023 00:11:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:11:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Jun 2023 00:12:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:13:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a7b266165314fb42c56d5aa852e1f83c98085f13635a77e632483e5d1e54db9a`  
		Last Modified: Fri, 02 Jun 2023 00:41:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe208ce51fc4b96e5d3bd78f4685dec35d7f46ba9af9eaae4f1e176932cfbdd`  
		Last Modified: Fri, 02 Jun 2023 00:41:17 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff3152851f8844befa32e11f432b0607f70aee9816dd918305b3147e981d80d`  
		Last Modified: Fri, 02 Jun 2023 00:41:55 GMT  
		Size: 252.5 MB (252535476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974be1daf21a49e097d940136b4175294e7e1c4d9d28e1f29cdaaa63ed0234ed`  
		Last Modified: Fri, 02 Jun 2023 00:41:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5aa1ce42c20f65583c0242262f2ad4ea5788b0fbd29c382a9cb8c2b3f4936f2`  
		Last Modified: Fri, 02 Jun 2023 00:42:10 GMT  
		Size: 63.3 MB (63279806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3152008054efae2e8a22aa826a3c81eca11f9da605b00d3548e8adf758442c52`  
		Last Modified: Fri, 02 Jun 2023 00:42:03 GMT  
		Size: 283.5 KB (283467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c114ae5da45ca1eceb7d2db5850e67b66e565bbfedd4316a9ce7d5c8345839`  
		Last Modified: Fri, 02 Jun 2023 00:42:15 GMT  
		Size: 67.2 MB (67234283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdafbee6c01df0019cf65f8b2976ca6179adfccefe38860e6f133882dea2691c`  
		Last Modified: Fri, 02 Jun 2023 00:42:28 GMT  
		Size: 10.7 MB (10740352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

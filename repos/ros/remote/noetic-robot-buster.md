## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:3c65faad07f9e25ad8550728ee38e7ca6a6bfa12062688220c121ffcb3ecdbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:92069777988ba74fdb0cae3bfab8b9e0c4a4da9899793aee6387644b9dc2a36b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.0 MB (483991916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3dfbe903d1f6dbb616e94b911684acbf0549354f8439a8186758a7108f84f35`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:16 GMT
ADD file:89dfd7d3ed77fd5e05f20a0ab631142207ae462f5bbd877f8745d3930c751d87 in / 
# Wed, 22 Jul 2020 02:03:16 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:36:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:37:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 22 Jul 2020 20:37:01 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 22 Jul 2020 20:37:01 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 20:37:02 GMT
ENV LC_ALL=C.UTF-8
# Wed, 22 Jul 2020 20:37:02 GMT
ENV ROS_DISTRO=noetic
# Wed, 22 Jul 2020 20:38:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:38:42 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 22 Jul 2020 20:38:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 22 Jul 2020 20:38:42 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 20:39:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:39:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 22 Jul 2020 20:39:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 20:40:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:31dd5ebca5efc5e96a425402fa85e492b02c8fe757dfd3edfdea2a7c67322909`  
		Last Modified: Wed, 22 Jul 2020 02:09:37 GMT  
		Size: 50.4 MB (50390325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2b4c3e83730582d8aa0afee630f3929243c3f8f169e5caec1fe3ede3cf6ac6`  
		Last Modified: Wed, 22 Jul 2020 20:49:13 GMT  
		Size: 10.9 MB (10889394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6406abb87b09a866ace4e9e958e5615813523268f2aec3d9dbfae13e5846cdc`  
		Last Modified: Wed, 22 Jul 2020 20:49:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b28b9ccd622fdbbf58e61bdad8f8c8dad46da7b9c7f8e34943e50fd8620536`  
		Last Modified: Wed, 22 Jul 2020 20:49:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf679ac616afd10160caa0e2749b11f0089dee06f00347db9e127a0acc7d9125`  
		Last Modified: Wed, 22 Jul 2020 20:50:03 GMT  
		Size: 238.8 MB (238811052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42f3a065603ac47dcbbd4973c26383f24086b994ff77ec0a96af63653e6ff74`  
		Last Modified: Wed, 22 Jul 2020 20:49:11 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da20226b027ad37f8885bcdd2e4c82a17f05df1ef0c7fd846d6fc7a248e0819d`  
		Last Modified: Wed, 22 Jul 2020 20:50:39 GMT  
		Size: 86.6 MB (86562111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c890a4646b0da35aff42dd24cc5b7aa05e2a8fab5829a33fbd7b3a6b78f102f`  
		Last Modified: Wed, 22 Jul 2020 20:50:09 GMT  
		Size: 207.6 KB (207642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcee7fdde209dea082685e77b5f848d6d3dffe257b466ddbd597bbe2922fb073`  
		Last Modified: Wed, 22 Jul 2020 20:50:35 GMT  
		Size: 76.0 MB (75966569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434df1775f6ff5ef837d6199371f7c3cf4dc1019622bc63023a22ddbf07745ed`  
		Last Modified: Wed, 22 Jul 2020 20:50:49 GMT  
		Size: 21.2 MB (21162987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fde10c0934128f3390b3f469f0378bd6c35a0d0b62453b0a7ecb25ca0cd21be7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.6 MB (423599606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217718c2d7a358c3563d68c56d64b70ac832a07cc31716d7da3c98741927f053`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:06 GMT
ADD file:ce999027b153d392f8a0f85e2e7a17b9279f3cf7ad0e45192378d527275f99c6 in / 
# Tue, 04 Aug 2020 06:57:08 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 10:16:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 10:16:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Aug 2020 10:16:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Aug 2020 10:16:29 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 10:16:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Aug 2020 10:16:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Aug 2020 10:19:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 10:19:37 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 04 Aug 2020 10:19:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Aug 2020 10:19:44 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 10:20:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 10:21:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Aug 2020 10:22:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 10:23:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5517ee72007172d5b814636405254dea459120ce08f85777bb287d106a6a240`  
		Last Modified: Tue, 04 Aug 2020 07:03:41 GMT  
		Size: 49.2 MB (49175491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1e3fb9bc333a926aec0d0bd3fd71d27371bc8eee253902e8c37133a1387cf0`  
		Last Modified: Tue, 04 Aug 2020 10:35:22 GMT  
		Size: 10.9 MB (10882026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3292bab18c0d540bd5284459808c3310d802d50ae0abd31163f7d5b610424739`  
		Last Modified: Tue, 04 Aug 2020 10:35:21 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de6918466f489333df325cc01bab8c768887c8d7d799b3049f6693172c7c2f5`  
		Last Modified: Tue, 04 Aug 2020 10:35:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598e4c72a6a58a3a062e73876dfc3af1c41fce791679e367ec49a7d1803fee5b`  
		Last Modified: Tue, 04 Aug 2020 10:36:27 GMT  
		Size: 184.1 MB (184069980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bfa31468fc59d35b1dfa798d96d8124b2d711e844fec9f4eca42b2b18d0e9c`  
		Last Modified: Tue, 04 Aug 2020 10:35:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3abfcbb2f5b21e9158901c82def3138ee0abaec2065c266f65644f630683ea`  
		Last Modified: Tue, 04 Aug 2020 10:37:02 GMT  
		Size: 84.4 MB (84354661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65320f532c15eae3952d71c00e835e6146b10173c6685c9fb881e82e8a37aaa`  
		Last Modified: Tue, 04 Aug 2020 10:36:35 GMT  
		Size: 211.3 KB (211304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2ad80aec0a86d16cd10849469c185220827e370f505219e9f285239d9d99a9`  
		Last Modified: Tue, 04 Aug 2020 10:37:01 GMT  
		Size: 74.1 MB (74088257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c320260d10e07fb43b89e7d588d6425422eb1d4b1d27a85b55d20f8c34da41`  
		Last Modified: Tue, 04 Aug 2020 10:37:14 GMT  
		Size: 20.8 MB (20816047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

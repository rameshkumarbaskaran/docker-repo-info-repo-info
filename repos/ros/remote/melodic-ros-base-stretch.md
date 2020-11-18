## `ros:melodic-ros-base-stretch`

```console
$ docker pull ros@sha256:c6193c36b991876cd14e99421690d13d1e52271b3400edbaadb09c770da16cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-stretch` - linux; amd64

```console
$ docker pull ros@sha256:7efe469f1bbbdfb9b4e866160f2a3eddf307c27a99203eb5b6949e8a1b263bfe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.6 MB (447634573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cda71c92981da4dec575e60f02cd193ccddc571171561fce1489bc51d1b2974`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:13 GMT
ADD file:a8742c34bf12f231279dd5086b8ec1310224c740a95170b916217f22a68eb9a7 in / 
# Tue, 13 Oct 2020 01:44:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 19:17:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 19:17:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 13 Oct 2020 19:17:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 13 Oct 2020 19:17:46 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 19:17:46 GMT
ENV LC_ALL=C.UTF-8
# Tue, 13 Oct 2020 19:17:46 GMT
ENV ROS_DISTRO=melodic
# Tue, 13 Oct 2020 19:19:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 19:19:18 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 13 Oct 2020 19:19:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 13 Oct 2020 19:19:19 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 19:20:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 19:20:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 13 Oct 2020 19:20:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0400ac8f7460260a663e0e97c24d7dfd8a2c947736f0351752b45c53e26d6e02`  
		Last Modified: Tue, 13 Oct 2020 01:50:49 GMT  
		Size: 45.4 MB (45366778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e64d6a7fc5320867400c03832cf54957cbbf98b99714a200a9090f67fa0af6`  
		Last Modified: Tue, 13 Oct 2020 19:32:22 GMT  
		Size: 6.9 MB (6866999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868ec983be87cbebfea0a9dea300e1ae958cdc96a8fd550ed6ba63ceeed46116`  
		Last Modified: Tue, 13 Oct 2020 19:32:19 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7303450037ec364ecd0bff523fa0140a41fbc939b44bcb48abe60b9fe2d1fdc4`  
		Last Modified: Tue, 13 Oct 2020 19:32:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04058250f482c63226262abef7876d3f158f937c4535066c3bacf84b047b5f9c`  
		Last Modified: Tue, 13 Oct 2020 19:33:29 GMT  
		Size: 269.9 MB (269927678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876e825fea60d421a44ae42f1fb98d96cf6acdcf20af70678fd093ce7bc7211a`  
		Last Modified: Tue, 13 Oct 2020 19:32:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b3345f7bb5574ca7d580696fd7f3e8c218a503004f3eff3679e6b29efee8f4`  
		Last Modified: Tue, 13 Oct 2020 19:33:51 GMT  
		Size: 70.2 MB (70152916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59a685afc6f0c271459de511b5c166bbced15374a2f8482920687c0181f415`  
		Last Modified: Tue, 13 Oct 2020 19:33:35 GMT  
		Size: 264.6 KB (264554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d8e96833fe2accef120b31842c4fd2a18a1f5f4685b04fe0b84ae6cbffde54`  
		Last Modified: Tue, 13 Oct 2020 19:33:49 GMT  
		Size: 55.1 MB (55053833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1669f95cc61a447b60b781ac504716880b8dee7c4355c1d26972836dd28ac23c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.1 MB (393059317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7856e59688b267c9f5056b614778925725d7a89fa406214815c13761e06e25f4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:27:33 GMT
ADD file:d2e307c3e54ad69dff47f6bdacca7c8ee0957a09346bb21baec02b9de1a657e1 in / 
# Tue, 17 Nov 2020 20:27:37 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 09:12:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:13:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 18 Nov 2020 09:13:06 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 18 Nov 2020 09:13:07 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 09:13:08 GMT
ENV LC_ALL=C.UTF-8
# Wed, 18 Nov 2020 09:13:09 GMT
ENV ROS_DISTRO=melodic
# Wed, 18 Nov 2020 09:17:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:18:01 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 18 Nov 2020 09:18:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 18 Nov 2020 09:18:04 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 09:18:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:19:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 18 Nov 2020 09:20:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f99bf631c0ebddf9e32516b47bf6e198efc42d06c3eb86d6f5f5739757b5839c`  
		Last Modified: Tue, 17 Nov 2020 20:34:17 GMT  
		Size: 43.2 MB (43176009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92602d4f5b35fbaf1e8fb6e411e04e5971ce33abe3c7fd5964643892b701db93`  
		Last Modified: Wed, 18 Nov 2020 09:48:11 GMT  
		Size: 6.4 MB (6440978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf801218bf713e927fb087f64d89fe28628b81fd8acd57df9e4ba24ba6c30ef3`  
		Last Modified: Wed, 18 Nov 2020 09:48:10 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e48643aeb8ff25cf211053dc193b030b253350d3971e2e58d453851c9d6e2e7`  
		Last Modified: Wed, 18 Nov 2020 09:48:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264bb6a4cb2e6ef5b80b5c02c9dd2dc4f790e1ad5c5e9db55d0014d33248f173`  
		Last Modified: Wed, 18 Nov 2020 09:49:09 GMT  
		Size: 225.1 MB (225086213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6c7356b45f618401b91d614bfe17badbbe1fedbd8b057ac7d88df4f9045be4`  
		Last Modified: Wed, 18 Nov 2020 09:48:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4c5c31a03ea726417639eac21a23e2910ccbe53394b0219a7363783f6368f0`  
		Last Modified: Wed, 18 Nov 2020 09:49:34 GMT  
		Size: 64.8 MB (64842008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647d19d2b200772b31d78fc0ff297f10c12f7f3d7ca10826491e95db88a1a20e`  
		Last Modified: Wed, 18 Nov 2020 09:49:17 GMT  
		Size: 268.6 KB (268580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56db4512c1a14af1ff014c4817e095576dd8fd9b1a58032793555b198bd3e2f0`  
		Last Modified: Wed, 18 Nov 2020 09:49:29 GMT  
		Size: 53.2 MB (53243709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base-focal`

```console
$ docker pull ros@sha256:06ecb5169858b8e1ee682d78ba772db6e76fa555105dc006de81e16c4d65fa51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:569696e5621fad056b14672265a27fb12507999bba8a6d8dcf332d16e6a2dad1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234891739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da8c152231c267d0724f107b91d186a7da80f21ae25d40984d9b4ce79d3985f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:31:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:31:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:31:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7f5b5c701916838562eb61ea9d238d42ecdcf4603217d5f36de002d875373`  
		Last Modified: Tue, 25 Oct 2022 08:01:15 GMT  
		Size: 73.3 MB (73280543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066dfb5edf358837c3acdfe4765a62b10a0588d5ee88a202f18c6decb245a6c4`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 279.6 KB (279618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81213e1334be0f25c6545b79677786f9e06c1aaea8a510b21195f4dc08b6ecac`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c4d1072c5bb0b70378dd5a649ff6468e2763e77a087f95fa4e934dfa18632e`  
		Last Modified: Tue, 25 Oct 2022 08:01:06 GMT  
		Size: 22.1 MB (22138749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9823d71d84a6facb9ad6ab94361c78eaafb082eedee10eb50d0fcf03e3196e40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.2 MB (223197069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a96e112da177db105e7ab8a4629e2f05d7ebf4a0f23fba4094e15b8f76174cb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:51:53 GMT
ENV ROS_DISTRO=galactic
# Wed, 05 Oct 2022 13:52:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:52:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:52:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:52:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:53:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:53:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:53:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8d16a1f7ff237a77f29323231038803c348a1a9f11afc6bb177737dfdcad1c`  
		Last Modified: Wed, 05 Oct 2022 14:15:38 GMT  
		Size: 100.4 MB (100375443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b03d420b9714c9f3dc15cd95ef79baf5b4457aa24c478be8fc2000236b33fc`  
		Last Modified: Wed, 05 Oct 2022 14:15:22 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a956f99c4721f7dc25bfe3b1c9c90ce2a2d8b0474b19e342030574fa077dbc98`  
		Last Modified: Wed, 05 Oct 2022 14:15:59 GMT  
		Size: 67.4 MB (67402819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1231122a3faa9e29e7dcfbc07429b9a375bde70cf77017ed38de61d4a42bb924`  
		Last Modified: Wed, 05 Oct 2022 14:15:50 GMT  
		Size: 277.8 KB (277756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5317376816f40e243dc89e1427d6106c53bd777b2ad592afdce65fa1301cdce8`  
		Last Modified: Wed, 05 Oct 2022 14:15:49 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a90f00672da01678118f187b2830f6621555d9e05eddf1d8c10a2d25f967f2`  
		Last Modified: Wed, 05 Oct 2022 14:15:53 GMT  
		Size: 21.5 MB (21458239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

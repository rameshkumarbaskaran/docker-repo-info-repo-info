## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:a2ead4032040a7d6afa48a83f2342bfb13cb1f3bfeed36fd4940f860c7e672ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:26171861e9728cd5afc87ff920583f1da58207535c4fabbab64bcb1914d761d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359019674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dc1d4306276c53aaf0e61662f2418be18eabe34ff5b4173a789eb77f9d05d2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Aug 2023 07:21:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Aug 2023 07:21:51 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV ROS_DISTRO=noetic
# Thu, 17 Aug 2023 07:23:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:23:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 17 Aug 2023 07:23:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2023 07:23:54 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 07:24:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:24:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Aug 2023 07:25:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab22f0326d7d89686f4eebe2ba52f86ca4e83a4c69d66dfe4f2b1494eae439`  
		Last Modified: Thu, 03 Aug 2023 02:53:09 GMT  
		Size: 1.2 MB (1198625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915067b2cb577e1158572cfb9bb4edba91b52a0f5821152a8a4e2518dd702c`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 5.6 MB (5553744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dd0b38cb0829def318257a357f2d9773c0c0f443432fe0ab8f0e28f8454a13`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b104afafaf102a6ecd5bc760e922c728c4ab27320895943844d8f53c908a025`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f437788a75a65f6ba1decf914b73eaf4b4712c46e542abaf9d51e92f1e6c32`  
		Last Modified: Thu, 17 Aug 2023 07:49:46 GMT  
		Size: 177.0 MB (176961988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8de474ce644ddf64e37acf737479db384d569592e927234ba9775cbf3c044`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71044449a9df53317087cbf1480ae89d0864ed6c767b63f246f2a112cb697023`  
		Last Modified: Thu, 17 Aug 2023 07:50:07 GMT  
		Size: 50.9 MB (50940393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57c22656c0736ccbe5b757eeada9768c4061541ea8fced3debcc9d8e5186c3`  
		Last Modified: Thu, 17 Aug 2023 07:49:59 GMT  
		Size: 305.0 KB (305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01916643bc85febc6c44576e168005fd7892f275d1a187528964c1a062bb36a`  
		Last Modified: Thu, 17 Aug 2023 07:50:10 GMT  
		Size: 79.6 MB (79614040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f781912f3aa6add79d8d355f91f4f813ea41cb3588b44b0946845b83c495dc3`  
		Last Modified: Thu, 17 Aug 2023 07:50:27 GMT  
		Size: 15.9 MB (15862756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:c41539a5a68e47e13122787650225bc42370886628f92db240c164f64f00fc4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303292113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9832067cc8944698d44d3ee6bc021869db790caf4c7eacc6d6f9dafc84f5060d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:25:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 01:25:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 01:25:43 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 01:28:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 01:28:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 01:28:13 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 01:30:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:30:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a3643fb9ea7b4891593c2a71e53f70146f828b8896758ecc6804e843b3eb9d`  
		Last Modified: Fri, 13 Oct 2023 01:38:43 GMT  
		Size: 1.2 MB (1200040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d390fd421e090bebfad483fae5954c8ce4b3d98d6f7964b7d2af20febd3a8dd`  
		Last Modified: Fri, 13 Oct 2023 01:38:41 GMT  
		Size: 4.7 MB (4680598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f635e6735a4e72b10c5401661b398132793e75102ebdae3c1a4bb09369a9277b`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc440f8be875763f266a01bddecd7e5256b0f7024383d18f3ac27b3eefca620c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8576e38b77aab0fa900f38b3857ac3f1f5f2f357b049bb4765eead409392f8ab`  
		Last Modified: Fri, 13 Oct 2023 01:39:16 GMT  
		Size: 157.4 MB (157433981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9929dceae2a7ac00be4bdeef95d2220d21923972182d5a0805ae6a130e9a5c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbc9c70d09913eddb72c3c4f69d3eacc75f42772407b3a7f1b83b8ab76e8609`  
		Last Modified: Fri, 13 Oct 2023 01:39:37 GMT  
		Size: 40.5 MB (40504496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4c4f8456ac317553d22cb6aeb19337c7ba56c832bd9ce3050a5666e4e67276`  
		Last Modified: Fri, 13 Oct 2023 01:39:26 GMT  
		Size: 308.4 KB (308391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11110f8ff52141ed436fcf91a65720ab159af26f35baf35ebec69235529767`  
		Last Modified: Fri, 13 Oct 2023 01:39:41 GMT  
		Size: 60.5 MB (60500564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cd9542cbabe9c5ca1a0dde9973ca6791e1de1468c878a7b6b95d90f1095178`  
		Last Modified: Fri, 13 Oct 2023 01:39:56 GMT  
		Size: 14.1 MB (14069455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e953d7f922e3e94877ce9936dbd76a64eea936fdaf7d24c5691c4661bc65450b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338292245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7334d608f23ea631771a9eead91ab532d13139c7ddb063074bdc1b74018eee86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:24:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 04:24:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 04:27:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:27:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 04:27:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:27:42 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:28:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:28:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87696a1bdfb2280c9c8f032b8dad476643e285ea6a4daaaaf8dea807599345f3`  
		Last Modified: Fri, 13 Oct 2023 04:58:00 GMT  
		Size: 1.2 MB (1199301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c122b6409bbe49fd6863f4fe1b6c386aa8c0839b4d569cc6a7c864c54e4ebc`  
		Last Modified: Fri, 13 Oct 2023 04:57:58 GMT  
		Size: 5.5 MB (5532659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a917760d45f055be63dd5265386c3e099071676cbade870f5fad9204d410ad08`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f178865c356dfadb4351dd90e17e88bc0c96c7a5b00c3fa27f7a7a50854a6`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70efcc630f7ac8f41932a95504f9faf4f5d3a98261ec78847c0b7895c7e38c55`  
		Last Modified: Fri, 13 Oct 2023 04:58:33 GMT  
		Size: 171.4 MB (171412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7380be57882dd81c0bc849142d511e957f6f209e899d784c2169dd1268af381`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03ae63d5fe1e840f0cc374100c4a33137e2c3862f567675d2a4f2a632ca68fd`  
		Last Modified: Fri, 13 Oct 2023 04:58:54 GMT  
		Size: 45.2 MB (45206478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78bb804d06a6c2affa7a4df0cb90051039812dd200a146925a447da4c03248f`  
		Last Modified: Fri, 13 Oct 2023 04:58:44 GMT  
		Size: 308.4 KB (308395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee77018c303d0f8b15482607876c85bd6f9bd91d7320f861f1146fc7f1e5f98`  
		Last Modified: Fri, 13 Oct 2023 04:58:52 GMT  
		Size: 72.0 MB (71972672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2096eb516266a125f99bb94d5b72cc5ffa2827b552aa2e1189a4fe247f072ee`  
		Last Modified: Fri, 13 Oct 2023 04:59:07 GMT  
		Size: 15.5 MB (15458807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

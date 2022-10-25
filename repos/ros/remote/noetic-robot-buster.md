## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:5c647a88e7c67804d7b3e57e1c557b771bd9a64fe57be52d361f2be5a9d21202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:1df3c892d86fd452b24e82eaee409fa376a344437411ebcc64174f683cc20db5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.9 MB (484899656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1b1975f4b9abbde15c6fa7066017b6b11ed67f9bed0616d47b9d8eaa078533`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:17:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:18:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:18:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:18:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:18:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:19:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:19:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:20:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7bb5a8d4409ae76ed240704c8628d248a907ec454b12a0f653fa5180822f32`  
		Last Modified: Tue, 25 Oct 2022 07:56:14 GMT  
		Size: 10.9 MB (10896941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9831692d445c53ad6706089a3b147d293d3267dd486b27109a911c9da182ed31`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2beecf1c3569265300a22936ddda05e835f0c83b2193ea68b4d60f2882113cd`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834cb0e33271e58107ddec676304ba095210344f2ee4310bb860d12b941b510c`  
		Last Modified: Tue, 25 Oct 2022 07:56:46 GMT  
		Size: 239.2 MB (239209563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdd4ac8f13eeeb7f19f875b6a9191a3aedf9fd8006aae02db37664d36f51883`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f066880bf184688bbe3b3bce165ab3ad72850aae130b41b408020b47003491`  
		Last Modified: Tue, 25 Oct 2022 07:57:07 GMT  
		Size: 86.6 MB (86586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c12225f8506452bbdfb135687a0e9642f4fd2bec37dacde2ff8e68f0031c8`  
		Last Modified: Tue, 25 Oct 2022 07:56:53 GMT  
		Size: 326.7 KB (326687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cb66701beaeeb105d227e3c100dab245e25d8e913dcb72fb68145181a9140f`  
		Last Modified: Tue, 25 Oct 2022 07:57:05 GMT  
		Size: 76.0 MB (75978159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e243b3e8516342ad34ac067531d9d7545ff8c35ac1742dfad88b051b3b043db`  
		Last Modified: Tue, 25 Oct 2022 07:57:18 GMT  
		Size: 21.5 MB (21452008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3b603a162a01cffc2f94f0638445bdb64192217fb369bb1d3cf5b3341a353b75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423991607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82425e01996b0f75a886f464dbcb66332c2a722fb5c343e861996462a994d70`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:54 GMT
ADD file:ef2ee78fb3eda698ebec33ff4b6dea672e03908b0f8630a28acb33ec9a7c3e13 in / 
# Tue, 04 Oct 2022 23:44:55 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:42:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:42:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:42:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:42:22 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:42:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:42:24 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:43:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:43:35 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:43:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:43:38 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:44:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:44:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:45:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:45:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:504dcdd9b4a0035dba7a55a5312cf594c3d22fb99b7bf676d397c464db919009`  
		Last Modified: Tue, 04 Oct 2022 23:50:47 GMT  
		Size: 49.2 MB (49228885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c286841822dd708cc8ec03c64947552384e955fad5e3df9a73a5acab4aaaed`  
		Last Modified: Wed, 05 Oct 2022 14:11:38 GMT  
		Size: 10.7 MB (10689488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b51b46470fae12ab22dbf0e0f68d92e335b5d2aec01faf4694f688dcff7ed7e`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01f93551ac4426be901cafe628cfa60e541d98154404fcba3cb02cde1d85358`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a850fdf218d14508c13532bd2745504750003968ec91b47bbc2a16d38af0791f`  
		Last Modified: Wed, 05 Oct 2022 14:12:09 GMT  
		Size: 184.4 MB (184402359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46befb9f0b1823e66932ff7e6bd3b3f7ef17e0115617e47457b2e68aa6db3103`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70142cef45c79ed6c16def65c939723b912688d777616cd8f0394a0a9bed62b`  
		Last Modified: Wed, 05 Oct 2022 14:12:28 GMT  
		Size: 84.4 MB (84371054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec293e0c6336ccbd0d0986af98ef8fd2f6e8caebfc5454d01a8d50bf39f3310`  
		Last Modified: Wed, 05 Oct 2022 14:12:17 GMT  
		Size: 324.6 KB (324579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdd5b15718815c6b2b180f7ba28bb586c4071861d49a281db790d1263561842`  
		Last Modified: Wed, 05 Oct 2022 14:12:26 GMT  
		Size: 73.9 MB (73865277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6113ec2fc7cc5403f1bec46f71179910d1b80ae4844ca9e0759bbaa64a354ea5`  
		Last Modified: Wed, 05 Oct 2022 14:12:38 GMT  
		Size: 21.1 MB (21107597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

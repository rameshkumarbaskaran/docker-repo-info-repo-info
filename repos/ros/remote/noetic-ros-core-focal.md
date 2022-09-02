## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:d764b670e0f25556a150598c6ea1e4d7e2f66e6b45d9e602779a93ceb1bf6801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:15787f4244d2c4f18c65ff9f5e7aa63bad77a3174d734e44c5d2efe18ccedbf6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212281865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b851b252f464f1ba9e081c21053a32f21ce69a6ec8af25754576fe7b6efd082`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:30:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:30:47 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Sep 2022 04:32:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:32:46 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:32:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:32:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e933af47665655d97d902ecb6d264063a041b2c12dfcbaf849a05672cafc9044`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1916d550484243d392ddc6fdca4ba34710bd3305a578bf9d241f2ad6d944c099`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d152bd7bb3b1335dd05a53828858de8ceab15c85e96fdc0181b2e38f72323b8`  
		Last Modified: Fri, 02 Sep 2022 05:07:05 GMT  
		Size: 177.0 MB (176996015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edc8aa6732f94d22820aa0f96400c620b51e015fa6a940c03e9b579f0de306f`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:b627329429c292b2ec2942cf25941025bba74bdd29b28271ffa3758060d0ee56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187929954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7324654dea2b039973f3b058244c1f5bf15eb28690dbe2fd8426e09c3f10323`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:45 GMT
ADD file:7de7e2c2eb5b05b2449f1e73da223081e27d073990c979ec73afd1893c58c551 in / 
# Tue, 02 Aug 2022 01:40:45 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:53:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:53:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV ROS_DISTRO=noetic
# Wed, 03 Aug 2022 22:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:55:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de6f11ffeeef9e471776e52baf8cc454a1249e8caf2d8944a5b0387143608310`  
		Last Modified: Tue, 02 Aug 2022 01:43:13 GMT  
		Size: 24.6 MB (24589273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d345e3aeca1c4dd8930e961af9d46712aa474a7ce53acba4f54b4ff3b113a84`  
		Last Modified: Wed, 03 Aug 2022 23:09:30 GMT  
		Size: 1.2 MB (1181992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf40d14b8b7f81b4f192b1708fbdb0a57c3626f5b72be630a041c1f634f266`  
		Last Modified: Wed, 03 Aug 2022 23:09:28 GMT  
		Size: 4.7 MB (4676289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3223d85d87ee35ea3ab4535feef031631e281f3c617de4cdc218c4983c9b6f`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5bf7f51f5d7e24eec5395780a42aebd0c726cb0466dd5e0b2c492c6d0c84b3`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c66f511399e2f2993ed8fd014bb457c6d6a9483ae665aea0e9eb01fb0a54b4`  
		Last Modified: Wed, 03 Aug 2022 23:10:06 GMT  
		Size: 157.5 MB (157479986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa138f7b3214bda7dc2ae9534dff610b8c2a41d8de8dfb7c8a69ab5eba596887`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2de7b235c0f81dd7f2400b18a72f2e37c2eaff057a552ff4018d27b6e9283537
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205125274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef973504c6d304f7f2ee2f0be2414109ac868cf40926997b3d262097d2c63aa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

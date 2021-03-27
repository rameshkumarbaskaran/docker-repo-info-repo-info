## `ros:melodic-robot-stretch`

```console
$ docker pull ros@sha256:150bf3732790ba6cf105f564ed236cd2fe1e64adf9132dd0b443ee47bfce2dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-robot-stretch` - linux; amd64

```console
$ docker pull ros@sha256:528b8ded067fd0e32fd432ce47f213d2320684d94c16a47230b820b63d1d10a0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.9 MB (462908100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2928c7daf3c7ee9fd0952419d7fa34c821fd46a08e9baa86400080a91ea8b82`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:12:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:12:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 27 Mar 2021 09:12:24 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 27 Mar 2021 09:12:24 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 09:12:25 GMT
ENV LC_ALL=C.UTF-8
# Sat, 27 Mar 2021 09:12:25 GMT
ENV ROS_DISTRO=melodic
# Sat, 27 Mar 2021 09:14:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:14:08 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 27 Mar 2021 09:14:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 27 Mar 2021 09:14:09 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:14:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:14:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 27 Mar 2021 09:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:15:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d657504ffb8f628d70a2b1e2672e16b95f6eac895057e4cdcb97e09f862a1b09`  
		Last Modified: Sat, 27 Mar 2021 09:26:42 GMT  
		Size: 6.9 MB (6869187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa6cca370d6196ae385348a9369c89f41ffa9578e97dddffed55be61d6e0e62`  
		Last Modified: Sat, 27 Mar 2021 09:26:41 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8404a516aba8bbb9ba24fdc7ef19705ce8dd84915cf4cd2986249f95c22db251`  
		Last Modified: Sat, 27 Mar 2021 09:26:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb5474c655269c720249df5c38af05416a1d5e3d33019bffbcd827297ddd6c6`  
		Last Modified: Sat, 27 Mar 2021 09:27:27 GMT  
		Size: 270.1 MB (270070182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab44e97519ff7d9f42f3b133c7e261108a040df6ade9b5001b98fe56d831b1c2`  
		Last Modified: Sat, 27 Mar 2021 09:26:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4e3577ec11e0ec0f964d88d42f446bc25d44365aac4bed90203216f05cef4`  
		Last Modified: Sat, 27 Mar 2021 09:27:47 GMT  
		Size: 70.2 MB (70152067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac8e068e3ef5cdbe90cbc04af49da34966533a80f7beab3646960b0267594bd`  
		Last Modified: Sat, 27 Mar 2021 09:27:35 GMT  
		Size: 249.8 KB (249815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f41d908f054838060d72326ca70b40b4d00631e57e56aae261e2569b448f9c6`  
		Last Modified: Sat, 27 Mar 2021 09:27:44 GMT  
		Size: 55.1 MB (55059313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea369706f9b6549670ecd14c91f5eca8ee228e76b70eed6d05311a81d788002`  
		Last Modified: Sat, 27 Mar 2021 09:27:57 GMT  
		Size: 15.1 MB (15126204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:04346debab571818db0ba84c729e4ef4ebe9d184d49c9222d29dc40d4f824a20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407743452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7364dff7412c82dc466ae0cbefde30468760dc5840ea1d9c3064599b4574f6a0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:44:15 GMT
ADD file:cf753fedc426819aa5f93f4ad934479efd8fbf024b408627239b77ddc5223108 in / 
# Fri, 26 Mar 2021 15:44:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 08:33:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:33:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 27 Mar 2021 08:34:02 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 27 Mar 2021 08:34:02 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 08:34:03 GMT
ENV LC_ALL=C.UTF-8
# Sat, 27 Mar 2021 08:34:04 GMT
ENV ROS_DISTRO=melodic
# Sat, 27 Mar 2021 08:36:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:37:04 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 27 Mar 2021 08:37:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 27 Mar 2021 08:37:08 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 08:37:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:38:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 27 Mar 2021 08:39:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:39:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1a0736e738921f2c70c8ce48d5ba8b042279c41c41f32a1af43a6cbd299f6d89`  
		Last Modified: Fri, 26 Mar 2021 15:50:55 GMT  
		Size: 43.2 MB (43176405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab771badbb8aa014048919f3589fd266ea69c3369386e5871c978f23a8300b4`  
		Last Modified: Sat, 27 Mar 2021 08:56:28 GMT  
		Size: 6.4 MB (6442899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7b2222f36c8d1ffd59561065b458542540fa5d056c07a7c5ff43d4e1084af6`  
		Last Modified: Sat, 27 Mar 2021 08:56:24 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c120925e04f1f36d906c84242cdd9f6d9ae18d015db752ff53635239f1870b35`  
		Last Modified: Sat, 27 Mar 2021 08:56:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50bfea5dbd258a9531ab03eb35139fb5c33ecb25b5a5882f3f243ca5994e9f5e`  
		Last Modified: Sat, 27 Mar 2021 08:57:39 GMT  
		Size: 225.1 MB (225112695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32714704b7f44517608be7e9533727964a04ec6dc8e9c8047053bdf8dc92c9f`  
		Last Modified: Sat, 27 Mar 2021 08:56:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8119ffa5fde8dfba6c39226884180785301afcb5488d367944526fc4dd2deff`  
		Last Modified: Sat, 27 Mar 2021 08:58:07 GMT  
		Size: 64.8 MB (64841607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a40bc6066f10b9b1eb1bcb868f180d1c434236eec089cf30a8a67177035879`  
		Last Modified: Sat, 27 Mar 2021 08:57:45 GMT  
		Size: 249.8 KB (249815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7649ac0f7052ab66028a03fa4317a99e1022009b4a4f6c96689d49cfd3bc7cd1`  
		Last Modified: Sat, 27 Mar 2021 08:58:03 GMT  
		Size: 53.2 MB (53245384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e20efe7d9c2b088ec3b23afeb01accdccc3a3bc531c8ecc3590221e82bdeb`  
		Last Modified: Sat, 27 Mar 2021 08:58:17 GMT  
		Size: 14.7 MB (14672827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

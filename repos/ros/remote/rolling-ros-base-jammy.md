## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:f2bbd1bc2e8c4b7d7f4212961b431e9680f74af886e9a318377f9c27429489c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:979e8631ca260bf051c308446c63d2c2cc5d5fb267fc5412543463e4cbc13da3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283202060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d86fe3731f9d8e0f01689266fe6c1b9aa5cb0e41577a478a50ef371e63844b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:15:16 GMT
ADD file:3f673e2aa3a51c7980f0f25985b44578e091d31b3e0a8f481069c20b363a216c in / 
# Wed, 02 Feb 2022 02:15:16 GMT
CMD ["bash"]
# Sat, 26 Feb 2022 02:24:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 02:24:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 02:24:42 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 26 Feb 2022 02:25:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 26 Feb 2022 02:25:22 GMT
ENV LANG=C.UTF-8
# Sat, 26 Feb 2022 02:25:22 GMT
ENV LC_ALL=C.UTF-8
# Sat, 26 Feb 2022 02:25:23 GMT
ENV ROS_DISTRO=rolling
# Sat, 26 Feb 2022 02:28:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 02:28:08 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 26 Feb 2022 02:28:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 26 Feb 2022 02:28:09 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 01:28:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 01:28:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 01 Mar 2022 01:28:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 01 Mar 2022 01:29:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c610536171e3c233fc979d34130a90e9c9bc030425e5af141fd0c3aa8bcf5fb2`  
		Last Modified: Wed, 02 Feb 2022 02:17:11 GMT  
		Size: 30.5 MB (30532381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69865bdeb36f9908dc95f897cfa52157f167b05547180cd39a6b299ec5066824`  
		Last Modified: Sat, 26 Feb 2022 02:29:52 GMT  
		Size: 1.2 MB (1191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9177dcd66ad47879d77e6a83c2c8c0ed121ac7569db4fa355a902abcba68fe9f`  
		Last Modified: Sat, 26 Feb 2022 02:29:50 GMT  
		Size: 3.8 MB (3828294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51aecbdc07d493e58edb2120715fa312a3a4778f6353c8b89a6dde38c41a3f9`  
		Last Modified: Sat, 26 Feb 2022 02:29:49 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09813fd921e82b5beee394a1640678fb2aae5b027828684f1b9d44378d7cfebd`  
		Last Modified: Sat, 26 Feb 2022 02:29:49 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7938cab3e71d4742241763bd05ede6ea9f334f91b7e7c012d24c36e84982ea`  
		Last Modified: Sat, 26 Feb 2022 02:30:12 GMT  
		Size: 124.6 MB (124647963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279917d4e15f9b0770a34b92772a0887b229ae8b81ba2d4812e08ce19bd41591`  
		Last Modified: Sat, 26 Feb 2022 02:29:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0063b702ba11d68406fa74bd2300b4153b5bdc7d34d4e7feb5705c8661edf77`  
		Last Modified: Tue, 01 Mar 2022 01:30:32 GMT  
		Size: 99.9 MB (99861354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540611fbcddef698f5f5dfbda8c183c7e7d28861726d6d8b2c40efe91631e8d9`  
		Last Modified: Tue, 01 Mar 2022 01:30:18 GMT  
		Size: 264.6 KB (264598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaeb6ebeaa893b69004a25107ed8ad416460cf733552639bd7f079c14deebe3`  
		Last Modified: Tue, 01 Mar 2022 01:30:18 GMT  
		Size: 2.2 KB (2176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce96296e704dc0d80eb3ce429b33f1388e6484d7db2854086313e996d5320d53`  
		Last Modified: Tue, 01 Mar 2022 01:30:22 GMT  
		Size: 22.9 MB (22871056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a9f06a2cd3783fdd97d9963962b46c15a75b64e87cab2a7912757ef2e1e2158b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276681459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc563451289e59c32428decce473402ad442b81721f9011c23dba27fb3cad4d9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:55 GMT
ADD file:14faf487f471b0c41efdbd2280f1d905387bf534ef8810abd3a37774ba55ca12 in / 
# Wed, 02 Feb 2022 03:19:56 GMT
CMD ["bash"]
# Sat, 26 Feb 2022 00:44:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 00:44:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 00:44:29 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 26 Feb 2022 00:45:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 26 Feb 2022 00:45:07 GMT
ENV LANG=C.UTF-8
# Sat, 26 Feb 2022 00:45:08 GMT
ENV LC_ALL=C.UTF-8
# Sat, 26 Feb 2022 00:45:09 GMT
ENV ROS_DISTRO=rolling
# Sat, 26 Feb 2022 00:46:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 00:46:09 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 26 Feb 2022 00:46:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 26 Feb 2022 00:46:11 GMT
CMD ["bash"]
# Sat, 26 Feb 2022 00:46:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Feb 2022 00:46:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 26 Feb 2022 00:47:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 26 Feb 2022 00:47:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a99755935c0ed83076913ebdfc8b5a435fda0bdb7463e3f44b9c68ccfbabfc15`  
		Last Modified: Wed, 02 Feb 2022 03:22:20 GMT  
		Size: 29.0 MB (28957023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58066ccb94244f7b05c1e3f0da559277e10da1c9c0ba92fa419a08eae94a70e0`  
		Last Modified: Sat, 26 Feb 2022 00:49:20 GMT  
		Size: 1.2 MB (1193898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319c7eb9c853b6e46cdbca80f7eef1ecd99450449be76c3335cc15b720c9870d`  
		Last Modified: Sat, 26 Feb 2022 00:49:18 GMT  
		Size: 3.6 MB (3596216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40894fefa8f50a868c983395fcabf33b97aa0717112a45273475437fa80fbace`  
		Last Modified: Sat, 26 Feb 2022 00:49:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f288530d3ee34e27854ee0c701df63d10fb414ed7a7bb00ae7cbfa0371f494`  
		Last Modified: Sat, 26 Feb 2022 00:49:18 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58266d751be66d0d2f814c0010414fe3821c7a1daaa0b2d848cbd773734e67f5`  
		Last Modified: Sat, 26 Feb 2022 00:49:39 GMT  
		Size: 123.2 MB (123197430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6502c9f94ca6d8962989e8134a1c6b91908eb368eede3f2e9a328364a566bb`  
		Last Modified: Sat, 26 Feb 2022 00:49:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe21fb9f030b837dd1aba2be729d795ac8f13ac5ae07aaabe204b50d84b1b0d`  
		Last Modified: Sat, 26 Feb 2022 00:50:05 GMT  
		Size: 97.2 MB (97191425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd56872b6acb157d053d0a7b471ee7e96bff8302b49c71b111542e9504f43311`  
		Last Modified: Sat, 26 Feb 2022 00:49:51 GMT  
		Size: 264.6 KB (264550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ac08fde67a71b5457791a4fa367ad73577ea97fcfcc06494cc178db47b6921`  
		Last Modified: Sat, 26 Feb 2022 00:49:50 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50a89cadb283b5a6d249f660c12216298fc56d461e1f120905c14cae4d41bba`  
		Last Modified: Sat, 26 Feb 2022 00:49:54 GMT  
		Size: 22.3 MB (22276404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

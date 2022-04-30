## `ros:melodic-robot`

```console
$ docker pull ros@sha256:7ea13828785d507116d34792afc9dd2c805226ef4b3600671c1ec5c596d5146c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:a28bc3f892f1dfeecae7a00ba6304b00add7a4f48d9ecc1357d7bd5a3f87a2d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448477280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec5677d8005df5c0680c12d81e6e284c12cbdf56cd93577cbf4d460cf52bd33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:12:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:16:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 22 Apr 2022 03:16:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV LC_ALL=C.UTF-8
# Fri, 22 Apr 2022 03:16:23 GMT
ENV ROS_DISTRO=melodic
# Fri, 22 Apr 2022 03:18:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:18:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 22 Apr 2022 03:18:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 22 Apr 2022 03:18:54 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:19:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:19:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 22 Apr 2022 03:20:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 03:21:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d08ae4a50ec7a4071fcd259c6dc2b8f3219e66e5206c2f15ee781c4691a7699`  
		Last Modified: Fri, 22 Apr 2022 02:30:38 GMT  
		Size: 839.0 KB (838982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca35b07994f608387e199fa484cf0d3a586144538b7ea207fea47c25e64441b`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 4.9 MB (4872320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e99e7d92f7a9c84f55e914a1ad549e14ba4885ce72e1422955549eb8a42412`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda5797f8b0a501462dae5d9c7c7baa2ab56476067c48007d7f7d5f28e027821`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdb800ef4ebf782b8706d3ca51c5602217bfdaccffd3c87e146da0fd5b913a`  
		Last Modified: Fri, 22 Apr 2022 03:47:53 GMT  
		Size: 259.5 MB (259455669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1a8004d93ae4d2dcb4e49fb62c1ad152510f72453bd6d548075d99ffce4a72`  
		Last Modified: Fri, 22 Apr 2022 03:47:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2772d37526d353480c40bc6613660a726bae949372e0b95ff5a4e9aef62d22cc`  
		Last Modified: Fri, 22 Apr 2022 03:48:13 GMT  
		Size: 70.2 MB (70241270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b2bccc87971a9fadd6a92eb4daea27c47e122f6de0c129f9cb64e2aa64019c`  
		Last Modified: Fri, 22 Apr 2022 03:48:03 GMT  
		Size: 279.1 KB (279107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162f4d6dcfc3bd2fa9202d04bbd1d4f684046c0a525682228e9024af7ee3fee6`  
		Last Modified: Fri, 22 Apr 2022 03:48:15 GMT  
		Size: 75.0 MB (74994599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453ce09845a35fb485ffe49a62e58ecd3d528a9aeb7429bdf7fd6941e6eb3ffa`  
		Last Modified: Fri, 22 Apr 2022 03:48:30 GMT  
		Size: 11.1 MB (11083036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:1d14bd9194543ed4a9d9f0dd81dbc60b9e4ceb6ddf151a2e4a2a09cda63e5b6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 MB (396027305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063acd2980c8c66d21cb505f4234c799e9f46aa28de7caa2849f8448d946245a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:25 GMT
ADD file:9604e3641a386ec134596dd717862c2386c1b90009c0646b1773930f98949d9c in / 
# Fri, 29 Apr 2022 22:58:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:28:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:41 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:31:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:31:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:31:55 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:35:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:03ca5b55b2bdc3c68d23c18a88c099e2015c6bdcef6e3c43ca0bfb6aea0b032a`  
		Last Modified: Fri, 29 Apr 2022 23:02:31 GMT  
		Size: 22.3 MB (22300451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ab3231e4fbaccf7df6d1d44ef88608a6c1b716de9810c8e2ad6b7dcc9f5fc`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 840.2 KB (840158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f529e0e8ed7433413f39308a48052c609e82179d4d22b76f62189c616e5fe14`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 4.1 MB (4086200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59f023c86c2016dd149f7a89f71dc59cb35eeaf64c75eadba638336b28f6abd`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdf654803a8e788e4166c4bf287b5137ec541b313ce50e4d9401f0bd63fc8d`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa17f883dcf2090ca188521c82e8ecd78e6182c5c0af353b2dee9a1b0e0c44e`  
		Last Modified: Sat, 30 Apr 2022 00:53:38 GMT  
		Size: 238.9 MB (238937435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27e0b0ee020522ab3317cb8094bd430e3fb49425c99d1cfafe5284f0562f68`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c89127f2ab55d40e6d39537412903ef429801ea54d6baf3a6439a6bb01692f0`  
		Last Modified: Sat, 30 Apr 2022 00:54:21 GMT  
		Size: 54.7 MB (54710630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108adfc0916db7aeda7a39615caa2cee9b6fbe75cd66aa27a2ac82eaf1e6e9b9`  
		Last Modified: Sat, 30 Apr 2022 00:53:50 GMT  
		Size: 280.0 KB (279967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab1dc1feb0f323edf28a08fb0fcfc3796eb524ac698714b37837180467e312`  
		Last Modified: Sat, 30 Apr 2022 00:54:36 GMT  
		Size: 64.7 MB (64746523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b852a9e6f9b9db1a873f5d26b96fa8e2ec994256c7153e1ef272a96d26c60c`  
		Last Modified: Sat, 30 Apr 2022 00:54:59 GMT  
		Size: 10.1 MB (10123526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dc415320b59ed3eceb471c9a86f2fc6febaf558f3bcc16cc737987b61c97d90f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.3 MB (422317875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7546d28bc1ce4883d78a9030d968b5c8fc659fcd88fbf850437db6e51fdd5a57`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:15:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:15:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:15:31 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:15:32 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:15:33 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:16:57 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:16:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:17:00 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:17:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:17:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:18:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:18:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9119a950b820c04a3c9309fd9cd748b4a1c924ef00ac90dcd01791d857977923`  
		Last Modified: Sat, 30 Apr 2022 00:35:56 GMT  
		Size: 839.8 KB (839766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54865980d811f13a848975797615c6b0c5f21fed029eb255b5a1b3a0566900ec`  
		Last Modified: Sat, 30 Apr 2022 00:35:55 GMT  
		Size: 4.3 MB (4264191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d745fee38250cce36d1723e6eb3964a525bb738eb2c82b501244732a881913`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbae97ea1f2eea13534851ba6f58745635c465f6dd61681051632a7cac4bc8c`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccf8a195bad2001e20b085a797b257c60b2e4020d738441e352b661525e5029`  
		Last Modified: Sat, 30 Apr 2022 00:36:30 GMT  
		Size: 252.4 MB (252383482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c7449338629d393daa386d56eda7c00568a57dd328cd7df0410b5e398458d`  
		Last Modified: Sat, 30 Apr 2022 00:35:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9440733505277e8f3f7d4bc2ad385b06e37093582b77feeef90fbf8570dddf3c`  
		Last Modified: Sat, 30 Apr 2022 00:36:51 GMT  
		Size: 63.1 MB (63076164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8b76e35d4800cba2ffd96b6e5766991c5f6f8df302a89558162e2756996fac`  
		Last Modified: Sat, 30 Apr 2022 00:36:42 GMT  
		Size: 279.9 KB (279913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240a0f2f7118df62260d84e096be2a18536d017cef9a31f1ecdb65a6c2608eed`  
		Last Modified: Sat, 30 Apr 2022 00:36:53 GMT  
		Size: 67.0 MB (67001910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7faa7e77a0405102c184b835be4302b1e544dcf264e0d19ea9f3626032a270`  
		Last Modified: Sat, 30 Apr 2022 00:37:10 GMT  
		Size: 10.7 MB (10734993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

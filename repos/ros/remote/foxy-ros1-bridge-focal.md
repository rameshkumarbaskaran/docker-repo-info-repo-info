## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:c711cdcda43183394b0a7679cce6e0261f123c59c50916dc4aef0a141a087098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:912a3f6b315803ca1c97a5e86a94ae218b04489cc85560cb12c70c522a323d9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.8 MB (345847427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d1c1ef4c69dbe8d77e6233330c2f1b06a759ed95daab93722530721ab18e62`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:18:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:38:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:02:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 02 Feb 2022 05:03:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 05:03:32 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 05:03:32 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 05:03:32 GMT
ENV ROS_DISTRO=foxy
# Wed, 02 Feb 2022 05:04:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:04:42 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 02 Feb 2022 05:04:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 05:04:42 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:05:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 05:05:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 02 Feb 2022 05:05:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:05:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 05:06:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 05:06:30 GMT
ENV ROS1_DISTRO=noetic
# Wed, 02 Feb 2022 05:06:30 GMT
ENV ROS2_DISTRO=foxy
# Wed, 02 Feb 2022 05:06:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:07:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:07:16 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762bb72141f73c9f8d23d9bc2396670126e4d86b9784e31484c651effc425f91`  
		Last Modified: Wed, 02 Feb 2022 03:38:42 GMT  
		Size: 1.2 MB (1182237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52b7e3f584549fa72b610dfd0819030eb6eb0a3a76a5d820599a986bb362dfb`  
		Last Modified: Wed, 02 Feb 2022 05:17:49 GMT  
		Size: 5.5 MB (5546994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ae25a4694ef2001927cb29325cd8fc4076b59d0d944cec831ce55095c4cb64`  
		Last Modified: Wed, 02 Feb 2022 05:20:30 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b7b6d92a2fd7f05c2ab982e2eaf8a7bb43a271459e4c3d5b978ff3f3de151f`  
		Last Modified: Wed, 02 Feb 2022 05:20:30 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0b826832564aea720214fd8993bf4bcd30e5c5affc246139bbb4355706836a`  
		Last Modified: Wed, 02 Feb 2022 05:20:50 GMT  
		Size: 120.1 MB (120081897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e227a65e902c4854536530c1bde6ed394c7fbf9e73cece166b682cdc5b436c`  
		Last Modified: Wed, 02 Feb 2022 05:20:30 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cfd69175d085fef31ca65967ff78aa35e0376ba210fbdfe9e74df9d42d3757`  
		Last Modified: Wed, 02 Feb 2022 05:21:11 GMT  
		Size: 70.9 MB (70857299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37b06b58e83047faee82be004d43a6360ccdb747f1f1f041412501e8d27e3e7`  
		Last Modified: Wed, 02 Feb 2022 05:21:01 GMT  
		Size: 248.9 KB (248922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea378eddd32a1562a9e2ce3fd65d0a34bac6fa3878d1c7964095e72b4519b25`  
		Last Modified: Wed, 02 Feb 2022 05:21:01 GMT  
		Size: 2.2 KB (2177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1928770fed4717ca1b7726b81cc53040ce118b598ea7a6432b53dbc4fe5ec292`  
		Last Modified: Wed, 02 Feb 2022 05:21:03 GMT  
		Size: 10.3 MB (10288861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305717e46b82733fb880b5ea4434098db87a53dea2eff167570a59fb3934e6bc`  
		Last Modified: Wed, 02 Feb 2022 05:21:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f807f84c365ab7cf01e31390cc0f08426ee162f29a680772bbb11cf51e93e0e`  
		Last Modified: Wed, 02 Feb 2022 05:21:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83172ddc716ff4ce6563b193fb4f8f178d6b25315b3d57c633be1311cd1ee705`  
		Last Modified: Wed, 02 Feb 2022 05:21:41 GMT  
		Size: 76.3 MB (76301446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd9cff13c3d1cca259cf930969bba8a4551167bdf9aca8795694910e1b49156`  
		Last Modified: Wed, 02 Feb 2022 05:21:33 GMT  
		Size: 32.8 MB (32770456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99648a96e7de3aadbe436a45bf391d6990f1206ce944a3fa2e489ee0798471a`  
		Last Modified: Wed, 02 Feb 2022 05:21:27 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fa93c5e8b753ee81847a165265d09c2bdc37526456828a1dea0cb6591d0bf075
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313543191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecd390e2b614638a76de27126afe7a71d12eb9452502531cdb22d068db4eef6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:16:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:16:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:22:43 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 02 Feb 2022 05:23:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 05:23:13 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 05:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 05:23:15 GMT
ENV ROS_DISTRO=foxy
# Wed, 02 Feb 2022 05:24:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:24:05 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 02 Feb 2022 05:24:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 05:24:07 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:24:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:24:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 05:24:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 02 Feb 2022 05:25:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:25:26 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 05:26:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 05:26:05 GMT
ENV ROS1_DISTRO=noetic
# Wed, 02 Feb 2022 05:26:06 GMT
ENV ROS2_DISTRO=foxy
# Wed, 02 Feb 2022 05:26:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:27:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:27:11 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ab66679c5f55612a5d5bd5d43275d9d9341f5a8d22f9ab693b0ead2cc11a1`  
		Last Modified: Wed, 02 Feb 2022 05:38:36 GMT  
		Size: 1.2 MB (1184127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ae39722cb5853b6834527ad3541d6b6ee8351493f8694fbe2c77537d74b0fe`  
		Last Modified: Wed, 02 Feb 2022 05:38:34 GMT  
		Size: 5.3 MB (5322515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7946f51a9043a39941ea735b23552ad9871c050c9a76146ecbca02f3b2ccc0df`  
		Last Modified: Wed, 02 Feb 2022 05:41:14 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674eebb3ef8d3ac94a8d3359380c6daf533589b04c7ab1556a43889517abf0d2`  
		Last Modified: Wed, 02 Feb 2022 05:41:14 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d967b39d264a4018be170e1a117f2d1d186ab6260726f1ba1308a3226b6fd8d2`  
		Last Modified: Wed, 02 Feb 2022 05:41:32 GMT  
		Size: 104.3 MB (104281545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd2ed2e208297943b1f55f54d868f092c5729863692293b427e9fe549ccb6c2`  
		Last Modified: Wed, 02 Feb 2022 05:41:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc76fa531e4f361c6763a5dca8bd9d2b16931698378a5748598c4131a8e1808`  
		Last Modified: Wed, 02 Feb 2022 05:41:53 GMT  
		Size: 65.0 MB (64978097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49455574a1eff20a357889e7cd12b3d94e4972d19fb6c9972bea469944a6328c`  
		Last Modified: Wed, 02 Feb 2022 05:41:43 GMT  
		Size: 248.9 KB (248870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1942d4230f4220a7c7576ae5335b3601ccc832a909d9a160d7ce278d4857840c`  
		Last Modified: Wed, 02 Feb 2022 05:41:43 GMT  
		Size: 2.1 KB (2128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1c0a0f3226b9ed8921e28a994b0b230215b85cf6e06bb678ea6d8fc3b6e83c`  
		Last Modified: Wed, 02 Feb 2022 05:41:45 GMT  
		Size: 9.1 MB (9086095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8c344586329c20bac0f3776144e0196d280960040c0dfc4ae10c868f873709`  
		Last Modified: Wed, 02 Feb 2022 05:42:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86411348f022d82925120fb19aa7cd7c83ae973deb2bcdd8b921bff63320e1ea`  
		Last Modified: Wed, 02 Feb 2022 05:42:28 GMT  
		Size: 76.1 MB (76134980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3e68bf41dacf3277bc760554dc6126d07359f63f8f9b37558a26e9a9ef54b0`  
		Last Modified: Wed, 02 Feb 2022 05:42:17 GMT  
		Size: 25.1 MB (25132351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7462bd63886b0dbcc4f541f907a87085aa6ad1eacfc27e7fcb1a4425b38c002a`  
		Last Modified: Wed, 02 Feb 2022 05:42:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

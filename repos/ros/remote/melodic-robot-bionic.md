## `ros:melodic-robot-bionic`

```console
$ docker pull ros@sha256:e70d3464abf83af48fdef1c60044628bf2ef3cfcd79d45ded06f593003e4213f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot-bionic` - linux; amd64

```console
$ docker pull ros@sha256:2068a86fbf546af4d2cd04b0e08afa70e29d1381be8b26aa46a966da11982009
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448453243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b178cafe1ea49750b6b35cef8398a435e36e0fecde1734d6c237952eb817cc7f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 04:52:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:50:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:50:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 01 Oct 2021 05:50:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 01 Oct 2021 05:50:38 GMT
ENV LANG=C.UTF-8
# Fri, 01 Oct 2021 05:50:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Oct 2021 05:50:39 GMT
ENV ROS_DISTRO=melodic
# Fri, 01 Oct 2021 05:52:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:52:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 01 Oct 2021 05:52:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Oct 2021 05:52:54 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:53:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:53:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 01 Oct 2021 05:55:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 05:55:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be57c60580131e55159e03672358dbc415078de9b8d6b73691837b848489424`  
		Last Modified: Fri, 01 Oct 2021 05:12:47 GMT  
		Size: 840.7 KB (840739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1f1a2e289084ae7331c7d324ec0bdb4af258b35f6d415aa2a78464eea323f9`  
		Last Modified: Fri, 01 Oct 2021 06:22:10 GMT  
		Size: 4.9 MB (4872323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f66e9143ca30cc349e28aaa680240c521074deafbfe5e607c1edddef9ff9b7e`  
		Last Modified: Fri, 01 Oct 2021 06:22:09 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6333b668b4a22fa1cdec0303e29239d19d5da3da1233dce934bbf3e0b0a29c3f`  
		Last Modified: Fri, 01 Oct 2021 06:22:09 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0d79c3d72ce11cacaac9a60a2a7a56df2d70ce72d76aecb0848c0c7ea69877`  
		Last Modified: Fri, 01 Oct 2021 06:22:44 GMT  
		Size: 259.5 MB (259455264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7485b62d0716c5d117121940b0470fb16b3221d38dfb324bfe80b8bd40ea84`  
		Last Modified: Fri, 01 Oct 2021 06:22:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96d623e8dfff6321c98e2dc21ca6c60c27088565e0bc86da9f05fbec02803a5`  
		Last Modified: Fri, 01 Oct 2021 06:23:05 GMT  
		Size: 70.2 MB (70231150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296f19f55cae6979901def357825f36e69141b265ad585c9bf5326cb2b91ca63`  
		Last Modified: Fri, 01 Oct 2021 06:22:54 GMT  
		Size: 273.0 KB (272993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f8fc01b5f326bafa63ce40161d166e1f5578f5f2d87989a2e5008cd9e812bd`  
		Last Modified: Fri, 01 Oct 2021 06:23:06 GMT  
		Size: 75.0 MB (74994903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03991905598cbe2e1c4ae3b3c38af7910c05944eaaac7548daec1a84855a5bd4`  
		Last Modified: Fri, 01 Oct 2021 06:23:21 GMT  
		Size: 11.1 MB (11078380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:c5a8352da1891710826f59f1449c268663e049f964388d43ce7304dc4a01e158
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 MB (396003438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14ee4a12e3290174f0e8cdbd172eedfea35785d16d298d14a22e5ea2c183018`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 02 Oct 2021 05:58:32 GMT
ADD file:ec8cec062962fe6498197aa4bfaf1953505e272985dda8d5e81465521d850fac in / 
# Sat, 02 Oct 2021 05:58:33 GMT
CMD ["bash"]
# Sat, 02 Oct 2021 22:47:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Oct 2021 22:48:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Oct 2021 22:48:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Oct 2021 22:48:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Oct 2021 22:48:18 GMT
ENV LANG=C.UTF-8
# Sat, 02 Oct 2021 22:48:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Oct 2021 22:48:19 GMT
ENV ROS_DISTRO=melodic
# Sat, 02 Oct 2021 22:51:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Oct 2021 22:51:33 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 02 Oct 2021 22:51:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Oct 2021 22:51:34 GMT
CMD ["bash"]
# Sat, 02 Oct 2021 22:52:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Oct 2021 22:52:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Oct 2021 22:53:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Oct 2021 22:54:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fe312f6db8a357ff205c74a1649d8c36186a76057c3223acbd31367e2dfd049`  
		Last Modified: Sat, 02 Oct 2021 06:02:32 GMT  
		Size: 22.3 MB (22304304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056c4e1c45e7370c0a89001ce3f27b8cb29dda1a3045cd21b5feb45b86814cc7`  
		Last Modified: Sat, 02 Oct 2021 23:10:35 GMT  
		Size: 841.6 KB (841600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761ddc01c5cd4707b222831b5c898c4b7c72dedbdf08c7c034c52e27d8fb48df`  
		Last Modified: Sat, 02 Oct 2021 23:10:34 GMT  
		Size: 4.1 MB (4085877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffb81f09de324d7eafb7dc79196a2d1a0aaaaeff8cf5ac7d677a48cca9b9c11`  
		Last Modified: Sat, 02 Oct 2021 23:10:32 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348110f0ae217262ab74d39bdb78bc24d293b05a66c566e992e393aa8636729f`  
		Last Modified: Sat, 02 Oct 2021 23:10:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35cea75c843f202719e12d6c0b65b06a1a2743414d67560aa090dfab89f781a`  
		Last Modified: Sat, 02 Oct 2021 23:13:03 GMT  
		Size: 238.9 MB (238932373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4a908a0a89a54ec468746bc176e64be9430edab2bf39917df6e1f5bebad7d8`  
		Last Modified: Sat, 02 Oct 2021 23:10:32 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ef458d73013d5c9b799742848a41a1f9cbd78cbde326a39b803252e573e99d`  
		Last Modified: Sat, 02 Oct 2021 23:13:45 GMT  
		Size: 54.7 MB (54696354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bca198f4909aba3f932611e3d650c626d3d048ef94761ee6c32858e7e4b54e`  
		Last Modified: Sat, 02 Oct 2021 23:13:15 GMT  
		Size: 273.0 KB (273025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61086c7dd1564bcc465f85db1b7f2909f76c12955724943f3cc231f86fb8d123`  
		Last Modified: Sat, 02 Oct 2021 23:13:59 GMT  
		Size: 64.7 MB (64746332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f065e02bc77045d335e7e916e032acac076408cc0601a0541e5880438c6173`  
		Last Modified: Sat, 02 Oct 2021 23:14:23 GMT  
		Size: 10.1 MB (10121158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:55adcec7df0fe472d169a29eb71a1a1a980016075c544146ff6db0932dec7b49
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.3 MB (422262375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb22982445c9975ae941f18159a931abd4ad545cfcf0b2c2782f6bf73225e73`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:38 GMT
ADD file:35e2504756850fc1add00516fa89b0499b59c348457a96708eedb61313e7b25e in / 
# Sat, 16 Oct 2021 01:47:38 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:13:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:14:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:14:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 16 Oct 2021 02:14:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 Oct 2021 02:14:19 GMT
ENV LANG=C.UTF-8
# Sat, 16 Oct 2021 02:14:20 GMT
ENV LC_ALL=C.UTF-8
# Sat, 16 Oct 2021 02:14:21 GMT
ENV ROS_DISTRO=melodic
# Sat, 16 Oct 2021 02:15:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:15:37 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 16 Oct 2021 02:15:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 16 Oct 2021 02:15:39 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:16:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:16:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 16 Oct 2021 02:16:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:17:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f46992f278c2dd50c481ff60ce8528b6eb59016ac6243e1a7fb385c79c5944b9`  
		Last Modified: Fri, 01 Oct 2021 02:45:30 GMT  
		Size: 23.7 MB (23727476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b375d18c489948026f16ab6561023b9683664146a16727ea0d507f3212d10c88`  
		Last Modified: Sat, 16 Oct 2021 02:41:41 GMT  
		Size: 841.5 KB (841522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948ee8d4939a8e2553ea047e48055e411b82560a018db242d498108e70b60627`  
		Last Modified: Sat, 16 Oct 2021 02:41:40 GMT  
		Size: 4.3 MB (4264000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5862199e119a42d1ded50dd77acbe2078a38f8e1e7d178aa1132f95d77fc039d`  
		Last Modified: Sat, 16 Oct 2021 02:41:39 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14963566c87e352863745e6c6c88f5e7dce6d77061d5c8585ba2f302da70ab7e`  
		Last Modified: Sat, 16 Oct 2021 02:41:39 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4813509a2fdd51eb3e888f1b92d34fbeef04e05d071344ffb92fb8d5317a1a13`  
		Last Modified: Sat, 16 Oct 2021 02:42:15 GMT  
		Size: 252.4 MB (252356358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9e7629c2e32c08e9d73766f92d20e6568336a56f47e9a3452bef255c562a66`  
		Last Modified: Sat, 16 Oct 2021 02:41:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cabbc72c38b3bd93fa364c1bf2771868db54d3addb7c6b38e4001f8bfe14a87`  
		Last Modified: Sat, 16 Oct 2021 02:42:35 GMT  
		Size: 63.1 MB (63067322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbeab3a7555411aa1fc5cc2196f41ba0abcd0974b1ddd8243eb0f81c05ac175`  
		Last Modified: Sat, 16 Oct 2021 02:42:27 GMT  
		Size: 273.4 KB (273368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feff670c1aa58b1e11ed8b369126064e9ced4f8439ff7696e3ce2bdfaca85df7`  
		Last Modified: Sat, 16 Oct 2021 02:42:38 GMT  
		Size: 67.0 MB (67002048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7a003f55f36db1da1751d86c408d72cb2a04485f660ec1362b4af0ca71fe90`  
		Last Modified: Sat, 16 Oct 2021 02:42:53 GMT  
		Size: 10.7 MB (10727909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

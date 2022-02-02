## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:7bf260a3e74409d2f8017588c370e8225f2a5605cd8d216941d93eeb35ff9827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:94454a6efe72337c277e9ea559b9ac597e33de3683bc7831d8e6a1c42f47e873
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212176870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31ad47820a502ca4bb3fc640920ecacd421eed57c84c6ba0ef72ab2fb57d07a`
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
# Wed, 02 Feb 2022 04:38:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 04:38:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 04:38:49 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 04:38:49 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 04:38:49 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Feb 2022 04:42:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:42:05 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 04:42:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 04:42:05 GMT
CMD ["bash"]
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
	-	`sha256:929f30f687751ecac97ac8f7d9e32c1d04529e24dd295260f04d155417727b7c`  
		Last Modified: Wed, 02 Feb 2022 05:17:48 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d9d8c434b05d45d157e4ec317b677d85a52e75270276744b0d14550d3aaba1`  
		Last Modified: Wed, 02 Feb 2022 05:17:48 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5817ec09234ed9ce470545c3acf00e23142dcb516c28aefa40e4744d723ddffe`  
		Last Modified: Wed, 02 Feb 2022 05:18:18 GMT  
		Size: 176.9 MB (176881125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9625910ea1bb19f31d9a8ae9a756206c0e84bb585d9a83b91a42984a29b290`  
		Last Modified: Wed, 02 Feb 2022 05:17:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:a78462b673b8587f7341890f90c3240e321f18022c101c46d2d665ea478f350f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187350115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5ca30f9ece0cdcbbfde22d3bf7182e7a86a841d28a9ca8953997d47e4ae1cf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:13:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:13:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:13:53 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Feb 2022 03:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:16:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:16:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:16:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a00403b45dfef687f4d96b9d93b7f1faa1e085fb7f5399ad1c4d3972e22a33`  
		Last Modified: Wed, 02 Feb 2022 03:38:13 GMT  
		Size: 1.2 MB (1183495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a346b5c6873a995df2c12469d7464f1596cd61c00168c869711d291cca1ec3`  
		Last Modified: Wed, 02 Feb 2022 03:38:12 GMT  
		Size: 4.7 MB (4676856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9e808252a53ad64e27c8579a98ad066591cde96558c55174e369563ff274d9`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dcf23ebea83b29129e099a6c06b92b159629f1a1ccb3e8f6d1c397ab636e60`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dad2830e8dc1eab49942f83118bc7e7a2944da39923442cba83579a95d65800`  
		Last Modified: Wed, 02 Feb 2022 03:40:15 GMT  
		Size: 157.4 MB (157424599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d228b695dfcd78c5d1f360dd4e57b204b5933003cf3f1c8b449f5d8c3d8e40df`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4c0e7b141e6a6d7e73443793d275145846ab2596512057b7493956c7ce48e70d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205010398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6b20560b462e632fcf2ed3e59aa8194628de3161589504f1115625ac7f9ab5`
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
# Wed, 02 Feb 2022 05:16:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 05:17:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 05:17:34 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 05:17:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 05:17:36 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Feb 2022 05:18:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:18:35 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 05:18:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 05:18:37 GMT
CMD ["bash"]
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
	-	`sha256:83a2f7207f32b79e674118d44f43f6951da6385bc09bcdfa423b30caf03fd927`  
		Last Modified: Wed, 02 Feb 2022 05:38:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159a55ffc77aa9a9596ce2e777dbbcc7ad263a994cb975ae786689a942cbf4f7`  
		Last Modified: Wed, 02 Feb 2022 05:38:33 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6576e47debf252e23da516a920a8043c7fa72c40b0bfc64fd9aabe8534da5a0c`  
		Last Modified: Wed, 02 Feb 2022 05:39:03 GMT  
		Size: 171.3 MB (171331745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842cea626079544496a95073e028ec4bf11eafb35dbe41f75cfd2931b24d2f38`  
		Last Modified: Wed, 02 Feb 2022 05:38:33 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

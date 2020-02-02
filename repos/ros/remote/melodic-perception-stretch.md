## `ros:melodic-perception-stretch`

```console
$ docker pull ros@sha256:db21c7e1811e66c9c4b0220c8498fecaaf1b696443eca277b7a2a51cc47c2742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-perception-stretch` - linux; amd64

```console
$ docker pull ros@sha256:e33258ed8aa19e902749ff69ed9934dee913772e34c6d499d45c193eca4be70e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 MB (876296511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db59e3b311d7b80435c2ca0ae65290a0cb073690ea46001b0d7fe7b437aa9a82`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:41 GMT
ADD file:8a9218592e5d736a05a1821a6dd38b205cdd8197c26a5aa33f6fc22fbfaa1c4d in / 
# Sat, 01 Feb 2020 17:23:41 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:49:37 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:49:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 01 Feb 2020 18:49:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 01 Feb 2020 18:50:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:50:37 GMT
ENV LANG=C.UTF-8
# Sat, 01 Feb 2020 18:50:38 GMT
ENV LC_ALL=C.UTF-8
# Sat, 01 Feb 2020 18:50:54 GMT
RUN rosdep init     && rosdep update
# Sat, 01 Feb 2020 18:50:55 GMT
ENV ROS_DISTRO=melodic
# Sat, 01 Feb 2020 18:52:48 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:52:50 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 01 Feb 2020 18:52:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 01 Feb 2020 18:52:51 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:53:59 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:58:15 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3192219afd04f93d90f0af7f89cb527d1af2a16975ea391ea8517c602ad6ddb6`  
		Last Modified: Sat, 01 Feb 2020 17:28:49 GMT  
		Size: 45.4 MB (45380658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a905ca7a93e1f1f1e5a3c9d5dacdf39395a357b216f42962d54cb9f2f2779419`  
		Last Modified: Sat, 01 Feb 2020 18:59:03 GMT  
		Size: 10.5 MB (10476666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39d9067426f73e53072c040a66d4e587fa9badca3da3aed990b6ef8afe8385b`  
		Last Modified: Sat, 01 Feb 2020 18:59:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47253481cad39c6f079e90a602a37b6638204f66869e48320e2d414b8ec82be5`  
		Last Modified: Sat, 01 Feb 2020 18:59:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822fec1fbb983df499d36a4c4325090bc1538e03ea008262104c269ccf6d6dc4`  
		Last Modified: Sat, 01 Feb 2020 18:59:18 GMT  
		Size: 64.8 MB (64771303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa493f6b00dde329976001c9a67f03cb4dcd3052a4d21da4e652a24c37556835`  
		Last Modified: Sat, 01 Feb 2020 18:59:00 GMT  
		Size: 416.2 KB (416167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf08f403c96546a118d22bcb2c270059a7191a4f76e27b5cc75f7698e56c606`  
		Last Modified: Sat, 01 Feb 2020 19:00:04 GMT  
		Size: 270.4 MB (270396217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a46c3d9114d6ebdac21d5007ae9386278d464c9e0047cbb328922103e3d04f`  
		Last Modified: Sat, 01 Feb 2020 18:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b10e6c9cd44f10367aabcd3b0d59f7b642aa09deda5ec6d77d9a7cf0312b6b`  
		Last Modified: Sat, 01 Feb 2020 19:00:40 GMT  
		Size: 108.5 MB (108475015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056a3529705b0d0d35a34e93f56f48182cba59654f8a920169820f62e9a4e279`  
		Last Modified: Sat, 01 Feb 2020 19:02:40 GMT  
		Size: 376.4 MB (376378667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9859240ad05ab9726d487e78c9eaeeaa84e2a138d6d39345329203a6b89a07f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **794.1 MB (794067028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e5a3437a9561926fb5e611f29d47c38ca568f00e32b5724e63960afa0bdcee`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:01 GMT
ADD file:1618e6474dbe6462a610ce7eed99f0bfd087ea37ddfc287bbd69def5c24ede47 in / 
# Sat, 01 Feb 2020 16:43:02 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:44:36 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:44:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sun, 02 Feb 2020 07:44:43 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sun, 02 Feb 2020 07:45:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:45:51 GMT
ENV LANG=C.UTF-8
# Sun, 02 Feb 2020 07:45:52 GMT
ENV LC_ALL=C.UTF-8
# Sun, 02 Feb 2020 07:46:13 GMT
RUN rosdep init     && rosdep update
# Sun, 02 Feb 2020 07:46:14 GMT
ENV ROS_DISTRO=melodic
# Sun, 02 Feb 2020 07:49:39 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:49:50 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sun, 02 Feb 2020 07:49:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sun, 02 Feb 2020 07:49:52 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:51:24 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:58:17 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df3de44c7096ba135556a1e7044f9e1feee3ef713ab96f0416f71fe78422cbf6`  
		Last Modified: Sat, 01 Feb 2020 16:48:40 GMT  
		Size: 43.2 MB (43166749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c33db3715bc6e9bf1a2a078edf3e50c65fa4c60d49ae91fb5933f1ca2b6ba0`  
		Last Modified: Sun, 02 Feb 2020 07:59:22 GMT  
		Size: 9.8 MB (9774849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef236eba576ebb9a25d74c7aabaca4cecfb50c11e85c6f3f3a8ba87e92fdb8c1`  
		Last Modified: Sun, 02 Feb 2020 07:59:20 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78592c06f0a0dcaa5ea7f016f166ea880f0093889e2b6ef20091a6247aa2e8b8`  
		Last Modified: Sun, 02 Feb 2020 07:59:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635f3fb9af5701ab0e946f90c9fcd0e121a3732cd2cde396b5250944ae47a01c`  
		Last Modified: Sun, 02 Feb 2020 07:59:38 GMT  
		Size: 62.1 MB (62086326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98f25735945cf5f207bd1206a8b9bddda32adf01f119085a14c9c5b5a4e3227`  
		Last Modified: Sun, 02 Feb 2020 07:59:17 GMT  
		Size: 416.2 KB (416228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495781d0c78ead4df31eb06bc574f93a43076fddedb913ef4d1479de83550996`  
		Last Modified: Sun, 02 Feb 2020 08:00:31 GMT  
		Size: 224.6 MB (224572825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab723dc821c93ef6a290f2028dcc8391ec9964f5dc49006e2449afaf64fa12f`  
		Last Modified: Sun, 02 Feb 2020 07:59:17 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5fd28ad82f4c31faf9c958ac8a8e400a5c285304e1662c2ad6afa32e72df1e`  
		Last Modified: Sun, 02 Feb 2020 08:01:08 GMT  
		Size: 103.0 MB (102961847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd2e7e210e1b08647d0c41066acf88c47f28056d3687815ba60a9b76535e352`  
		Last Modified: Sun, 02 Feb 2020 08:03:31 GMT  
		Size: 351.1 MB (351086386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

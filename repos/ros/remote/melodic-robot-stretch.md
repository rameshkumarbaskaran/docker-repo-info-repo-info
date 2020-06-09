## `ros:melodic-robot-stretch`

```console
$ docker pull ros@sha256:79aefe433052f5b38d2407644b3a23c716496c3feb0cf829f2965d568ae47f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-robot-stretch` - linux; amd64

```console
$ docker pull ros@sha256:41085b86087bffadaf3aa25a182d21ff18d23544f14d68b2da6e29e7a944ede6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.0 MB (463003832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fddd4cd5232e7c58870093da429b3ecf27bdc5980ba26cc003ef9261e05440b2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 06:33:25 GMT
ADD file:13031623172f5c5857e27de93553adedf17d955fa370882f850bb6ed6fb8cee7 in / 
# Fri, 15 May 2020 06:33:25 GMT
CMD ["bash"]
# Wed, 27 May 2020 00:40:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:40:24 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 May 2020 00:40:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 May 2020 00:40:25 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2020 00:40:25 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 May 2020 00:40:25 GMT
ENV ROS_DISTRO=melodic
# Wed, 27 May 2020 00:41:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:41:55 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 27 May 2020 00:41:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 May 2020 00:41:56 GMT
CMD ["bash"]
# Wed, 27 May 2020 00:42:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:42:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 27 May 2020 00:43:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c6172af85ee14a8db5a3a51d406b768dfa94d196c06d0d06d591507cf8199f0`  
		Last Modified: Fri, 15 May 2020 06:40:31 GMT  
		Size: 45.4 MB (45375207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b28b20c8c413ed647ed74f3f10133be8da4590c9925bf94a9d2319ffb2f7a8f`  
		Last Modified: Wed, 27 May 2020 00:56:31 GMT  
		Size: 6.9 MB (6865154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2a66cab0412b434c4a2500c5cec7decca877232cc612f58d7e4b73609be25b`  
		Last Modified: Wed, 27 May 2020 00:56:29 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeebda54a351b9b0cfeed08f111e7c8499bd2df81854da04d1e381ac5a3d7802`  
		Last Modified: Wed, 27 May 2020 00:56:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef33ca1dc9083382ef51b03efe176f7b62118f29b79b53ec1bcd8826e1539b82`  
		Last Modified: Wed, 27 May 2020 00:57:23 GMT  
		Size: 269.9 MB (269864464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfe8e8aa3afa6faf61324475cebe6fdc50502c69491f443342ba48f33127c1e`  
		Last Modified: Wed, 27 May 2020 00:56:30 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7f72e40487afc172f24e1502e68b3997a0705af028d54062439ae655373c8e`  
		Last Modified: Wed, 27 May 2020 00:57:41 GMT  
		Size: 70.2 MB (70150269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aff17de8219cffc22ee1df7ccc29b1ac3d2f19bdd7a404452d58dde21db6490`  
		Last Modified: Wed, 27 May 2020 00:57:27 GMT  
		Size: 248.1 KB (248106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f117343e149e4c9132c0d85084fc0ca2ee5d8e4ccf367bb179b8891ba0c2a97e`  
		Last Modified: Wed, 27 May 2020 00:57:40 GMT  
		Size: 55.4 MB (55407140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321c4c2ec3be7ad90593a332d84d9b6f1378e43a3ee810c7dd2020fd31f0bb5a`  
		Last Modified: Wed, 27 May 2020 00:57:47 GMT  
		Size: 15.1 MB (15091680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:936f069f3258065de33445a896b6b77b38c7537b576bd30b16fd02f664ef25e8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.9 MB (407862273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d533ed8c9e238e989f7a0e8f55fd6efe1e73a182b800d3281eb3d60d6aa7f198`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:22 GMT
ADD file:5cbf00485aed776e940988cadfad6853c640c13635ae54fb2b00aafccfe81a73 in / 
# Tue, 09 Jun 2020 01:54:25 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 12:53:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 12:53:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 09 Jun 2020 12:53:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 09 Jun 2020 12:53:46 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 12:53:47 GMT
ENV LC_ALL=C.UTF-8
# Tue, 09 Jun 2020 12:53:48 GMT
ENV ROS_DISTRO=melodic
# Tue, 09 Jun 2020 12:56:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 12:56:58 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 09 Jun 2020 12:56:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 09 Jun 2020 12:57:00 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 12:58:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 12:58:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 09 Jun 2020 12:59:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4c4f692ec920eecb1f30d9ef8e50125217decc872d7ada6eeccc36c6dcb49e4d`  
		Last Modified: Tue, 09 Jun 2020 02:00:09 GMT  
		Size: 43.2 MB (43160923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37f88e51d5d4beec1083e08e9be466763532cf657032a2c3c98008435fef6bc`  
		Last Modified: Tue, 09 Jun 2020 13:19:38 GMT  
		Size: 6.4 MB (6437966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe875459741248032e30abc4885c469fed8a4ebc05c8631c30f33195652c661`  
		Last Modified: Tue, 09 Jun 2020 13:19:37 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c097c91b719aef58bd93f194a36cc365038154109f7f7511d360e3d53f89c9`  
		Last Modified: Tue, 09 Jun 2020 13:19:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052064a7c891cb66765fc80001209186d5d9afb261c8827deee3450f5b19602a`  
		Last Modified: Tue, 09 Jun 2020 13:20:42 GMT  
		Size: 225.0 MB (224956393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9498708f5b05239cb64faf42e52aecdcb33660842377e40ff0c61c1c363c996`  
		Last Modified: Tue, 09 Jun 2020 13:19:37 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e0ae3abeeffa83250c21d559f7675cc98e68eec9c2289498f5cbef8bf50160`  
		Last Modified: Tue, 09 Jun 2020 13:21:11 GMT  
		Size: 64.8 MB (64836510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a78fb67949ed4752a3b28d38e6b1aa32964ed4e5cbf0cc723a1d697dc27fde6`  
		Last Modified: Tue, 09 Jun 2020 13:20:53 GMT  
		Size: 248.7 KB (248700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112e9aeec9888117794d0e29ae7786684d6419ee1d6621b83c4cab22730f7d9b`  
		Last Modified: Tue, 09 Jun 2020 13:21:09 GMT  
		Size: 53.6 MB (53580558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0927556bd82a569ca3fc0676a9b37c559ccb9acfc8dbaa08f3d4af4534387026`  
		Last Modified: Tue, 09 Jun 2020 13:21:20 GMT  
		Size: 14.6 MB (14639403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

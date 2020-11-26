## `ros:eloquent-ros1-bridge-bionic`

```console
$ docker pull ros@sha256:54da37873c83edae22a56a02aa61d8cc1cc1c238b8bfd9acb64ca3b48de9f54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros1-bridge-bionic` - linux; amd64

```console
$ docker pull ros@sha256:3f9edd3d3c9b4d3803f577c4808b464f47838481f5be009cb155bfa1baeffe77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.1 MB (504116096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb139dbab55e3da7ef3e91da47dc058b2441efbca7881a56de2d4381173ee890`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:13 GMT
ADD file:6ef542de9959c3061f2d0758adb031e226b221a1a2cd748ff59e6fc13216a1c0 in / 
# Wed, 25 Nov 2020 22:25:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:16 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:17 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 22:59:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:49:04 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:49:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 02:10:03 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 26 Nov 2020 02:10:04 GMT
ENV LANG=C.UTF-8
# Thu, 26 Nov 2020 02:10:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Nov 2020 02:15:24 GMT
ENV ROS_DISTRO=eloquent
# Thu, 26 Nov 2020 02:16:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:16:31 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 26 Nov 2020 02:16:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Nov 2020 02:16:31 GMT
CMD ["bash"]
# Thu, 26 Nov 2020 02:17:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:17:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 26 Nov 2020 02:17:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 26 Nov 2020 02:17:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:17:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 02:17:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 26 Nov 2020 02:17:29 GMT
ENV ROS1_DISTRO=melodic
# Thu, 26 Nov 2020 02:17:30 GMT
ENV ROS2_DISTRO=eloquent
# Thu, 26 Nov 2020 02:18:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:19:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.2-3*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:19:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:19:42 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:f22ccc0b8772d8e1bcb40f137b373686bc27427a70c0e41dd22b38016e09e7e0`  
		Last Modified: Fri, 20 Nov 2020 13:21:30 GMT  
		Size: 26.7 MB (26708056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf8fb62ba5ffb221a2edb2208741346eb4d2d99a174138e4afbb69ce1fd9966`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80c964ece6a3edf0db1cfc72ae0e6f0699fb776bbfcc92b708fbb945b0b9547`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a8092b82e49df7860a001e4452fcbb13b91f571599dc4688933a1138f6b372`  
		Last Modified: Wed, 25 Nov 2020 23:10:00 GMT  
		Size: 839.0 KB (838950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebbce50bab7cc5a89e4b0fd9944d1a04f6624166cf7167f0b95f5996d0ef71b`  
		Last Modified: Thu, 26 Nov 2020 02:28:51 GMT  
		Size: 4.9 MB (4870594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742c8b372e747b17b29d1b06efb74ea9a51cf7ea00f2ed266fc0243518807cf1`  
		Last Modified: Thu, 26 Nov 2020 02:28:49 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492a3104cee6577e8151a449350051d44b30e14814dd70a59f87803ea538acce`  
		Last Modified: Thu, 26 Nov 2020 02:34:35 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d7104a974b2215050f4d47a0f198dc9453bea2b5c5337f84c4b30df526cf5c`  
		Last Modified: Thu, 26 Nov 2020 02:36:47 GMT  
		Size: 183.0 MB (182955476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b03e094228f454ea77fe5acbecc07a8c48b28a4ac001274c0c801a17fa886d`  
		Last Modified: Thu, 26 Nov 2020 02:36:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb29e5b4c1f0844c761d3303eeb94dbf663ee3885bc8fca34916f4d25f869fdd`  
		Last Modified: Thu, 26 Nov 2020 02:37:07 GMT  
		Size: 63.5 MB (63513237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6878511921fe0ce22e9cbd4acf7afe569a35be2c92207a55353d056e40316401`  
		Last Modified: Thu, 26 Nov 2020 02:36:53 GMT  
		Size: 192.5 KB (192451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef9ae38795744051e1db658f5780628b9c0b1966ccc37e154cd74da511320c1`  
		Last Modified: Thu, 26 Nov 2020 02:36:53 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5bc156729922a27cec2b2cf39040d6a9be9fb7b64408cfeeb5e103c21b1d6c`  
		Last Modified: Thu, 26 Nov 2020 02:36:54 GMT  
		Size: 4.6 MB (4581242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c017d70ba840457ebf84122e5d88cf8e344c104a526039309b566e91a6c06d9`  
		Last Modified: Thu, 26 Nov 2020 02:37:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f80d7b094b33a982a4850b6344bead19a3a33f301a652a016644e157a9adec`  
		Last Modified: Thu, 26 Nov 2020 02:37:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c376a5cc84c5079b7cc63b53e5cc35e3333766e551b4bde26127b9f67a4e5fbe`  
		Last Modified: Thu, 26 Nov 2020 02:37:43 GMT  
		Size: 117.7 MB (117744992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ddf5e8f72c7176bfd1d3bf510bcafd1855905424c0c9b856beb829260914b8`  
		Last Modified: Thu, 26 Nov 2020 02:37:39 GMT  
		Size: 102.0 MB (101968194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b11b5fddbe4270a2e2a23d7270a09d682c99795a5e86e16af7449b692ca8914`  
		Last Modified: Thu, 26 Nov 2020 02:37:13 GMT  
		Size: 737.4 KB (737430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb25ad3f4e569b622d12f8b36c619821409947601d0310f601ca7dc3258d1bf`  
		Last Modified: Thu, 26 Nov 2020 02:37:13 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros1-bridge-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:92a7b6a3e3047674fc46d2a41efeb12f9c657a316aa18723f464f7fcfbfd7878
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (429008346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee283721f57cb43f757f288c1c502c715040ac1ad9e40ff6b3c50218a4850442`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:59:22 GMT
ADD file:d8af47cbd4b007e993c6c95352250d91f6bca6e453d7a7d3c98a1d866cb4b6dc in / 
# Wed, 25 Nov 2020 22:59:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:59:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:59:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:59:29 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 00:12:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:12:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 00:47:38 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 26 Nov 2020 00:47:39 GMT
ENV LANG=C.UTF-8
# Thu, 26 Nov 2020 00:47:39 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Nov 2020 00:56:32 GMT
ENV ROS_DISTRO=eloquent
# Thu, 26 Nov 2020 00:59:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:59:36 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 26 Nov 2020 00:59:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Nov 2020 00:59:39 GMT
CMD ["bash"]
# Thu, 26 Nov 2020 01:01:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:01:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 26 Nov 2020 01:01:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 26 Nov 2020 01:01:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:02:20 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 01:02:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 26 Nov 2020 01:02:23 GMT
ENV ROS1_DISTRO=melodic
# Thu, 26 Nov 2020 01:02:23 GMT
ENV ROS2_DISTRO=eloquent
# Thu, 26 Nov 2020 01:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:05:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.2-3*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:05:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:05:55 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:74cafcd4ef026d0cf9395503338bf02bc26e4f71aea4689608583ce51623688c`  
		Last Modified: Fri, 20 Nov 2020 14:58:52 GMT  
		Size: 22.3 MB (22290808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11c6b5e0a0aa52c392c1e7c843789bcf9a676dc15235765db096dd1ef771141`  
		Last Modified: Wed, 25 Nov 2020 23:01:36 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92494e4cae3eeabc9763450a6d57c33e98afa67265764f0113e427942b60e43e`  
		Last Modified: Wed, 25 Nov 2020 23:01:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d66a9d46083da8ba3e471567d4caf82ba22ec39a1025bab50247443a71600d`  
		Last Modified: Thu, 26 Nov 2020 01:09:55 GMT  
		Size: 839.5 KB (839541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c077d1b9d1b3aa28680433f7a30f481ddc8f1c47ec057a55cabdaa7a0924d5c`  
		Last Modified: Thu, 26 Nov 2020 01:09:53 GMT  
		Size: 4.1 MB (4085063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fbfa87749f24159d25ca1a071c58e8cc4802d19383716c27cc8660e1e3c12f`  
		Last Modified: Thu, 26 Nov 2020 01:09:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1120855b32106b086184cae85c2a8c2630d932ae0a779611d9fdb017c84c6ce9`  
		Last Modified: Thu, 26 Nov 2020 01:17:16 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ac75e5a0bc460d93c871bc33607195018d1fade138e375eb51b6d4762666e8`  
		Last Modified: Thu, 26 Nov 2020 01:20:01 GMT  
		Size: 156.6 MB (156581709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8862a613a9a5b4c580bc603dd110c935bdb302782bfe2432cff9a949da28bb6`  
		Last Modified: Thu, 26 Nov 2020 01:19:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb98f30af30e5b4e6f87d1027da5324674bf74238edaf5f3dbc6301b82314d5`  
		Last Modified: Thu, 26 Nov 2020 01:20:21 GMT  
		Size: 47.9 MB (47913182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccc06739c4a373ae8df555f06139ab4f5692eff3c8c93f0d4e5e0e445ac1dd7`  
		Last Modified: Thu, 26 Nov 2020 01:20:09 GMT  
		Size: 192.5 KB (192502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4492312d3958c83d21a9d6ad52fc40507d0bc0bc9a983d0cc94e3bc872069a`  
		Last Modified: Thu, 26 Nov 2020 01:20:09 GMT  
		Size: 2.0 KB (2030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307c5788ada8d100ab76f70738a0d3c3a40c519ca5e713a229ad8f94ba7ee55a`  
		Last Modified: Thu, 26 Nov 2020 01:20:10 GMT  
		Size: 3.5 MB (3492829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5a2cff08177f1643950132ef0273c241f0da5df336cd215cf8aac0b0aa4f88`  
		Last Modified: Thu, 26 Nov 2020 01:20:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8cf3501ecaf5208fcf6fc83d9ad492027db8e9f4dc8688a18107849ea659c4`  
		Last Modified: Thu, 26 Nov 2020 01:20:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f6798c2328e5ce34e71887d890e8b5147626b39e5817c04f06b639a2b3c20b`  
		Last Modified: Thu, 26 Nov 2020 01:21:09 GMT  
		Size: 110.7 MB (110657671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdbed724e89f170e63c627405304f9e0ac3a66559b64a2a77080f1c5a0a616af`  
		Last Modified: Thu, 26 Nov 2020 01:20:58 GMT  
		Size: 82.2 MB (82216125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d416734fce78bbc51f5e9b89de5c23f0b6dd38836124b36350d31a91b868924`  
		Last Modified: Thu, 26 Nov 2020 01:20:30 GMT  
		Size: 733.4 KB (733377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27266da95931f640af6c71b2314ad762ea30ff68dfbb55d61fdecda915f7211a`  
		Last Modified: Thu, 26 Nov 2020 01:20:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros1-bridge-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e70d1ce60a75b49b9b5e10fbdd0207321dd49cedcf99f34220348b69ece3d4b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.1 MB (464062994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2471ea9b3ada13055788487ca0f1b289fe7e6c9decfe88373e326a34c65403f4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:42:53 GMT
ADD file:e5b221023382c9e42b8558f8887f8317fe7e9759f59feb1799548aed9236e99b in / 
# Wed, 25 Nov 2020 22:42:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:42:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:01 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:58:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:58:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:58:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 00:20:15 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 26 Nov 2020 00:20:16 GMT
ENV LANG=C.UTF-8
# Thu, 26 Nov 2020 00:20:17 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Nov 2020 00:28:14 GMT
ENV ROS_DISTRO=eloquent
# Thu, 26 Nov 2020 00:30:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:30:35 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 26 Nov 2020 00:30:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Nov 2020 00:30:46 GMT
CMD ["bash"]
# Thu, 26 Nov 2020 00:32:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:32:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 26 Nov 2020 00:33:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 26 Nov 2020 00:33:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:33:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 00:33:48 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 26 Nov 2020 00:33:50 GMT
ENV ROS1_DISTRO=melodic
# Thu, 26 Nov 2020 00:33:52 GMT
ENV ROS2_DISTRO=eloquent
# Thu, 26 Nov 2020 00:41:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:47:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.2-3*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:47:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:47:38 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:04da93b342eb651d6b94c74a934a3290697573a907fa0a06067b538095601745`  
		Last Modified: Thu, 19 Nov 2020 16:25:04 GMT  
		Size: 23.7 MB (23733196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b235194751dee33624fc154603f7e25ecdfbb02538fb7d55fa796df9afa95fee`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606a67bb8db9a1111022bdc6406442e11c1a66653136c5c777114bf67b61038a`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0829be0ab1546c2197017682a8fa87c2c9bf9d430bb72fa87778f5f0843c64c3`  
		Last Modified: Thu, 26 Nov 2020 01:07:09 GMT  
		Size: 839.6 KB (839595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcaa7dbaa51b95c71b56e7a0030e87a40fb2d5f4a046a05c9247a720a071ad7`  
		Last Modified: Thu, 26 Nov 2020 01:07:09 GMT  
		Size: 4.5 MB (4453176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8dc9620e81d964a23f1b0448c85d69a4123a5cdab77b15a1898429bd1f119f6`  
		Last Modified: Thu, 26 Nov 2020 01:07:05 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57317b10b7bc56973797de6fc7f96d26fcb5138891e793344fc0236282519161`  
		Last Modified: Thu, 26 Nov 2020 01:14:28 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d605280adbf376408b3a2b2f361d389b6f249a2f8438f33462cf790313b824`  
		Last Modified: Thu, 26 Nov 2020 01:17:04 GMT  
		Size: 168.4 MB (168399033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0d75573abfa7a819ff13427f39d08fbedc0ce4662641506cc65e7c7dccb7eb`  
		Last Modified: Thu, 26 Nov 2020 01:16:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e11436f55a8bfa84107ac5033ad17a52911d96d7e4064cde976f54c73ea3bce`  
		Last Modified: Thu, 26 Nov 2020 01:17:29 GMT  
		Size: 56.2 MB (56226731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d97fc8d347d19cce5dc6d5cd856e1e25cf87425002f92a1cdac5bae14e989`  
		Last Modified: Thu, 26 Nov 2020 01:17:16 GMT  
		Size: 192.5 KB (192516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda8dd7dc06c1b460ed5fbd11cf53c3f891716311013e050c40b817cff6ebe56`  
		Last Modified: Thu, 26 Nov 2020 01:17:17 GMT  
		Size: 2.0 KB (2042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf14e6c26c68bfac38ad5cbfce4a565203b79d58859d3063ec2a2a540085c0e`  
		Last Modified: Thu, 26 Nov 2020 01:17:18 GMT  
		Size: 3.9 MB (3932752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc68bbe38861f245579511247483c8e07889cbfd8bf6ffa55899f4ef9e5e377`  
		Last Modified: Thu, 26 Nov 2020 01:17:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c66bb767c80eb4ab77ef094d3d988ef8fb724f9b97c8a74cb63ac58e67da87`  
		Last Modified: Thu, 26 Nov 2020 01:17:41 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796119b633027b8a96a3050e9fddd9b230ed13d2b38962693c273e88cf7dd239`  
		Last Modified: Thu, 26 Nov 2020 01:18:14 GMT  
		Size: 116.7 MB (116702124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df2d5353874930ebed9e2832ad2a13d1a53637cb480d1a981097a459db615a`  
		Last Modified: Thu, 26 Nov 2020 01:18:06 GMT  
		Size: 88.8 MB (88841212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef64af2f56501bb5843d882758fcc74e22d4b8e01c714af38ddc0ac5dd4e4e6`  
		Last Modified: Thu, 26 Nov 2020 01:17:41 GMT  
		Size: 737.1 KB (737107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b5b0d7d16924465ce06d8fb0ea46c78b00bf9eeb4666ca6f272652df69cb5`  
		Last Modified: Thu, 26 Nov 2020 01:17:41 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

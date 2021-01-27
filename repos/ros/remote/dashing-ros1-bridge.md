## `ros:dashing-ros1-bridge`

```console
$ docker pull ros@sha256:f97fb5c2c8afd218b97046a49f38aa7e063343549be5fbdace069f23ffe71c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:63145842527ec1efc594469680f856c48d32e62d4fb95be21f564aa7415bf6a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418358701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fc800656f3e6f5be9acd946b1ca8a3ce2bd5bb1cf7bb1da86f53000c6a82af`
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
# Thu, 26 Nov 2020 02:10:04 GMT
ENV ROS_DISTRO=dashing
# Thu, 26 Nov 2020 02:11:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:11:54 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 26 Nov 2020 02:11:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Nov 2020 02:11:54 GMT
CMD ["bash"]
# Thu, 26 Nov 2020 02:12:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:12:46 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 26 Nov 2020 02:12:50 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 26 Nov 2020 02:12:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 02:13:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 02:13:10 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 26 Nov 2020 02:13:11 GMT
ENV ROS1_DISTRO=melodic
# Thu, 26 Nov 2020 02:13:11 GMT
ENV ROS2_DISTRO=dashing
# Thu, 26 Nov 2020 02:15:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 09 Dec 2020 04:37:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.7-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 09 Dec 2020 04:37:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Wed, 09 Dec 2020 04:37:09 GMT
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
	-	`sha256:4dd6d3a1f29e7befc9c748fd255c3c126e4c5e337c2461311a7b46b719fd4c56`  
		Last Modified: Thu, 26 Nov 2020 02:35:11 GMT  
		Size: 179.1 MB (179099376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef4e2e1ba7366cfc6aef6b879268d3f22ae9152eeb3505c80b98f2c2b610639`  
		Last Modified: Thu, 26 Nov 2020 02:34:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592f4ce441f1ce49165440297ac29c471863c7f72265b2bc2133eef224e854dd`  
		Last Modified: Thu, 26 Nov 2020 02:35:29 GMT  
		Size: 64.2 MB (64164158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657764498e49fc195de959f01c93fbf34b1d1e11418058220be989c4b06f250d`  
		Last Modified: Thu, 26 Nov 2020 02:35:17 GMT  
		Size: 193.2 KB (193210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde5fc09fc48a5dac2cec25054191248aa4d49eab926445db2fc2e878c397696`  
		Last Modified: Thu, 26 Nov 2020 02:35:17 GMT  
		Size: 2.0 KB (2011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7525edf95e0e88fe7f917c09f542f422f985185a9f53a03fc2fda0f425aae9df`  
		Last Modified: Thu, 26 Nov 2020 02:35:18 GMT  
		Size: 4.3 MB (4313423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b066e418cb77ae4a6a9d3daabdef9e07a51778fe9826846a8875e5536e0cea3b`  
		Last Modified: Thu, 26 Nov 2020 02:35:35 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168979282bd7deb2267f8ccfd5eb7800127342aa6a7951c4661fe7e09e572fec`  
		Last Modified: Thu, 26 Nov 2020 02:35:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ceaa3c9dac2f65191f6f195ffec0394aca7d44b248499813b5497338d8a2bc8`  
		Last Modified: Thu, 26 Nov 2020 02:36:03 GMT  
		Size: 117.7 MB (117737192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf486eb2e9f09feb6376fa70c2af42c76a4e28a635d68036eb5787795da35a2`  
		Last Modified: Wed, 09 Dec 2020 04:38:39 GMT  
		Size: 19.8 MB (19788925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4dd5397016bc3e99e15928ebdf38ce9df1f9bb2cc640f2a704380b0b971f51`  
		Last Modified: Wed, 09 Dec 2020 04:38:34 GMT  
		Size: 639.3 KB (639332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dc71c17259b33074f903bf6cd3262562c70c8a66ab19a892a177b99badc5f8`  
		Last Modified: Wed, 09 Dec 2020 04:38:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge` - linux; arm variant v7

```console
$ docker pull ros@sha256:0f417e98c1a7d347abaa09e1e659fe03516bc0620af6800a8198d9eef23a5e6d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.6 MB (354567224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127b3a03f0b0bab1d4b301f4284f13583156722d1fe6797c0bc758753866ab00`
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
# Thu, 26 Nov 2020 00:47:40 GMT
ENV ROS_DISTRO=dashing
# Thu, 26 Nov 2020 00:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:50:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 26 Nov 2020 00:50:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Nov 2020 00:50:59 GMT
CMD ["bash"]
# Thu, 26 Nov 2020 00:52:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:52:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 26 Nov 2020 00:52:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 26 Nov 2020 00:53:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:53:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 00:53:16 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 26 Nov 2020 00:53:17 GMT
ENV ROS1_DISTRO=melodic
# Thu, 26 Nov 2020 00:53:18 GMT
ENV ROS2_DISTRO=dashing
# Thu, 26 Nov 2020 00:55:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 09 Dec 2020 02:52:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.7-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 09 Dec 2020 02:52:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Wed, 09 Dec 2020 02:52:49 GMT
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
	-	`sha256:ef697fe928ff18f9f1665aa9062ae99f9d3145115c31afca83d71209ebbd08e8`  
		Last Modified: Thu, 26 Nov 2020 01:18:00 GMT  
		Size: 153.3 MB (153253553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81669c315b478fb4105f48a165b7e19afc5b76669b3e109a99977f056a099fb5`  
		Last Modified: Thu, 26 Nov 2020 01:17:16 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f646c91b26d3a46227b887e1245028a59f4b5aee22025ebf1a15d709a328e841`  
		Last Modified: Thu, 26 Nov 2020 01:18:21 GMT  
		Size: 48.6 MB (48559136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83c57ee09103d91aa9ac610ea34d226e48ada8b1976a41fcbf8ad27fe7080d9`  
		Last Modified: Thu, 26 Nov 2020 01:18:09 GMT  
		Size: 193.3 KB (193271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e321d96417e1718f40b854df203bb99e148c4db2770bc93d20ccc706a93b10`  
		Last Modified: Thu, 26 Nov 2020 01:18:09 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dba5c406dba1c58dc010cfd708934c575a3eb30b7c57d514de915900b5b7d56`  
		Last Modified: Thu, 26 Nov 2020 01:18:11 GMT  
		Size: 3.3 MB (3250268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbe94d7b784b5a639e63bd74972fa58ab36dc6c18e5d78c0409c6ab1789f79c`  
		Last Modified: Thu, 26 Nov 2020 01:18:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627bd251265af8d5b9cce8918e5ced78ab1af4c91360f8a06c3d5a86fe97569f`  
		Last Modified: Thu, 26 Nov 2020 01:18:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd60e677bcef090deb19cc0fa1750022af62653e671199dfbe214b8198ad144`  
		Last Modified: Thu, 26 Nov 2020 01:19:05 GMT  
		Size: 110.7 MB (110650915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0c58afc4816abab04ebd374684bdf8d8cbee0e76c89eae314fd44a3761f1f1`  
		Last Modified: Wed, 09 Dec 2020 02:53:49 GMT  
		Size: 10.8 MB (10803130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f52503ec1c85cc44c2c8643cc292d46e9ff7e00b5f9f3caded26eb5273ca40d`  
		Last Modified: Wed, 09 Dec 2020 02:53:44 GMT  
		Size: 636.0 KB (635990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8e492582a86ecf9e5d1f2eb0f3f8ffb0847a2142b2e3fbb6be3b377de7d26`  
		Last Modified: Wed, 09 Dec 2020 02:53:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1a5efad13e6de5caafdfaea4838fa50042d11e3cb3864741d2ee061f1edfbc4d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.8 MB (386838285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fdc2e0f697654d8c7c1263efda37a464acf4123619e2481589704e7985ccd3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:23 GMT
ADD file:7d9bc01cf1f3757bf5fa308213a77aeb128883cc13616ff46b3da5b0e65b92f2 in / 
# Thu, 21 Jan 2021 03:49:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:49:32 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 06:35:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:35:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:35:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 06:54:42 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 21 Jan 2021 06:54:42 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 06:54:43 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 06:54:44 GMT
ENV ROS_DISTRO=dashing
# Thu, 21 Jan 2021 06:56:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:56:42 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 21 Jan 2021 06:56:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 06:56:44 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 06:57:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:57:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 06:58:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Jan 2021 06:58:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jan 2021 04:43:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 Jan 2021 04:43:10 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 Jan 2021 04:43:10 GMT
ENV ROS1_DISTRO=melodic
# Wed, 27 Jan 2021 04:43:11 GMT
ENV ROS2_DISTRO=dashing
# Wed, 27 Jan 2021 04:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jan 2021 04:46:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.8-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jan 2021 04:46:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jan 2021 04:46:23 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:64e3fba066352e44a4c1eeb6caedc87c29b46f0a7b31e21a58183fc8370005bd`  
		Last Modified: Tue, 19 Jan 2021 00:25:17 GMT  
		Size: 23.7 MB (23732640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbb433f451339aab734bb52e3df5b34cdea477f3f8e3aa32f7ac060bd852de2`  
		Last Modified: Thu, 21 Jan 2021 03:51:55 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3042a0d94b83caeb29bc20734c197130f58e14e86e8e6cdad8b768052bb563c`  
		Last Modified: Thu, 21 Jan 2021 03:51:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75de3cb7cc851400a98b3f91be110991f7d3e5ef9e3362b2a1feaabe73b663eb`  
		Last Modified: Thu, 21 Jan 2021 07:25:58 GMT  
		Size: 840.9 KB (840945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d872ef396f747e28f1e5d655b4da63120065e5b8c19b451d0fd13ff642a0b99`  
		Last Modified: Thu, 21 Jan 2021 07:25:55 GMT  
		Size: 4.5 MB (4453230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4f3dc2dc6bc64630a22a47f207e4ff99ae9332e157017224e77646d47bfe94`  
		Last Modified: Thu, 21 Jan 2021 07:25:54 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d90ee048de88433b386164e5f1c1d3cc6a3f6a5bffd8ae7b49cccece73ca7`  
		Last Modified: Thu, 21 Jan 2021 07:33:30 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fa291a4c0cb02d41f527e0400681dae5a47d26a4978d751c9cb41b6e94e767`  
		Last Modified: Thu, 21 Jan 2021 07:34:10 GMT  
		Size: 164.8 MB (164786423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ea5f42629191820535fc7a9e272ae9009a9db46a25228c6d63dfa5119a475d`  
		Last Modified: Thu, 21 Jan 2021 07:33:27 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e9b3e95fc2366b746042a58b83ac053b64b28831a684d4472923a17ae84893`  
		Last Modified: Thu, 21 Jan 2021 07:34:33 GMT  
		Size: 56.9 MB (56870047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a066ff136be8981204478f8cc2608b126e39f12d90f274cc10163e927426b05`  
		Last Modified: Thu, 21 Jan 2021 07:34:21 GMT  
		Size: 200.0 KB (200009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72cac45e7a357124861ed0881f1f31ac0d5a4e55f8185ccc71d6b110d6277a`  
		Last Modified: Thu, 21 Jan 2021 07:34:21 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97be147424254a1b85d982aac424029325ebc65437aef6eb059604494c99ac8`  
		Last Modified: Thu, 21 Jan 2021 07:34:21 GMT  
		Size: 3.7 MB (3665396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3883495dda2f2426ac51508f45673d4a258decd27bcfc88fed84ab4eb41afc1c`  
		Last Modified: Wed, 27 Jan 2021 04:48:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee0044a7e5477fe3f562f1c8d9cea672a2d2c47354e4696ac75d40f0aa59c23`  
		Last Modified: Wed, 27 Jan 2021 04:48:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0879dbc1452d12775ad34af965e1a6db444baf96e02754e5bd357b4900fbbd6a`  
		Last Modified: Wed, 27 Jan 2021 04:49:15 GMT  
		Size: 116.7 MB (116689194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163eb18609cd0eefb909a82076c44bc68fc37a9d5a6ce28140a9313c00c8efb0`  
		Last Modified: Wed, 27 Jan 2021 04:48:47 GMT  
		Size: 15.0 MB (14957939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c387e9b4ac63a1bebbb6668301f1bd964feb3bf512fc6221abfd1fc0192f7fad`  
		Last Modified: Wed, 27 Jan 2021 04:48:41 GMT  
		Size: 636.9 KB (636895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18562188c0f485a280c3bc2a88e147fcb3a9405df333da03326212662d8ba4c2`  
		Last Modified: Wed, 27 Jan 2021 04:48:41 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:dashing-ros1-bridge-bionic`

```console
$ docker pull ros@sha256:4f285d6cf49c80f827bcb8aa64ba08a7c8d36bcc67cb0a36dead1b735f63e24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros1-bridge-bionic` - linux; amd64

```console
$ docker pull ros@sha256:eac834b1730550f3ecbb8fa3ee51f20888ce1ed216323cc5c45ac64b89d2c193
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.4 MB (418399396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c11348cd2e8f64edaeb1ec2c2ecc9df288ee68e5e7e1955f2b49b111170765`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:37:59 GMT
ADD file:ef36fee25b0bd1d99979ecb8d54b206cec33d4e8fd2232189f0d8e5ab9754798 in / 
# Thu, 21 Jan 2021 03:38:01 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:05 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:26:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:02:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:02:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 11:24:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 21 Jan 2021 11:24:07 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 11:24:07 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 11:24:08 GMT
ENV ROS_DISTRO=dashing
# Thu, 21 Jan 2021 11:26:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:26:02 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 21 Jan 2021 11:26:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 11:26:03 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 11:26:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:26:56 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 11:27:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Jan 2021 11:27:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jan 2021 06:12:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 Jan 2021 06:12:50 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 Jan 2021 06:12:51 GMT
ENV ROS1_DISTRO=melodic
# Wed, 27 Jan 2021 06:12:51 GMT
ENV ROS2_DISTRO=dashing
# Wed, 27 Jan 2021 06:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jan 2021 06:15:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.8-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jan 2021 06:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jan 2021 06:15:39 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:d519e2592276828ca171d85e0532899cd4f98c70f5c697b45fa2e126e9f9fe49`  
		Last Modified: Thu, 21 Jan 2021 03:40:27 GMT  
		Size: 26.7 MB (26709716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22d2dfcfa9cd230ed3c47defec2670d45081598c721dd85cafc34ea459f970e`  
		Last Modified: Thu, 21 Jan 2021 03:40:17 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3afe92c540b778c64ca316d1e679d55d2d2e812e450f516a808ee591f0c3f77`  
		Last Modified: Thu, 21 Jan 2021 03:40:17 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea992ddb93cee91b21cf19902eb7c0780191f8454157802d68fe834ad6c72d5`  
		Last Modified: Thu, 21 Jan 2021 08:49:44 GMT  
		Size: 840.0 KB (840038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe549b7120b83770f6772179d9e937e479567ac1297ed6808a3c029da14a498`  
		Last Modified: Thu, 21 Jan 2021 11:44:40 GMT  
		Size: 4.9 MB (4870380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3148dcdae1e4da81fc90c6c4dc4ca6a3612c7176d9a53c61cf366eb77428c96`  
		Last Modified: Thu, 21 Jan 2021 11:44:39 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b05bde605617d448eae8a91768817550ef24992dd60f0fb9ae887e07d2860b`  
		Last Modified: Thu, 21 Jan 2021 11:51:08 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b7d0c83dc0a01c8673af090592c965659054a3e9c0c59b9a3c81e01e43b1c0`  
		Last Modified: Thu, 21 Jan 2021 11:51:47 GMT  
		Size: 179.1 MB (179120651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba861fb85dd5af15830d222355ec94584c2a1606158a04911e65af30e3b2ccb`  
		Last Modified: Thu, 21 Jan 2021 11:51:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac35ec9cefdc5c9df657fea3b223185dc4f5eeb61a95972e9c904ae3e5337af2`  
		Last Modified: Thu, 21 Jan 2021 11:52:06 GMT  
		Size: 64.2 MB (64163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f77e8abfd929d6a76a37560825528c3449e9640aa8313c393ddd8113f572204`  
		Last Modified: Thu, 21 Jan 2021 11:51:53 GMT  
		Size: 199.9 KB (199934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e99c486c75018a7b72b4f94919619470e9ea22c1f2acb17768044b9def12985`  
		Last Modified: Thu, 21 Jan 2021 11:51:54 GMT  
		Size: 2.0 KB (2008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9d5bfd6d536197657182a949ef908dffca676860870b6e68f7b5d155e6c1dd`  
		Last Modified: Thu, 21 Jan 2021 11:51:56 GMT  
		Size: 4.3 MB (4313064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a5b10584614beba63190727372b19c43f7e9fe7ccfb9983b82c5ff5941078a`  
		Last Modified: Wed, 27 Jan 2021 06:17:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040db242498c309d6704a659c272cd343dec6c02fff7d76a3b0033d1be512af8`  
		Last Modified: Wed, 27 Jan 2021 06:17:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67275a001d7c5ff20d2c165e996f49938407558534461cdf24f9f2978cd8983c`  
		Last Modified: Wed, 27 Jan 2021 06:18:26 GMT  
		Size: 117.7 MB (117737630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ceb34e4334d3d755f26ba1f179614c79e7e07387beab1845e517374b58e6ad8`  
		Last Modified: Wed, 27 Jan 2021 06:17:59 GMT  
		Size: 19.8 MB (19799708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0f9c40f9a1af0abd5d8f7c7a073c4c5c21a5b36b541974819135783ca0448f`  
		Last Modified: Wed, 27 Jan 2021 06:17:50 GMT  
		Size: 639.0 KB (639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67cab03e750b5378c3515d97cc624388e3c7c643457172a8aca487e3d856a71`  
		Last Modified: Wed, 27 Jan 2021 06:17:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:50f9631fdab86e50c109296b2c7a16b641a1cbfbf06b69b1b087508d2aee58f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.6 MB (354603148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5a8f37e72a30a56f25a571c2eb28200a349d640a410cbe81885dc07816aeb6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:15:18 GMT
ADD file:270f582b851314ab60dfbbc136c8e36ec44a11ecba1448403947ce72b0f9c06a in / 
# Thu, 21 Jan 2021 03:15:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:15:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:15:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:15:27 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:30:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:31:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:31:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 04:52:26 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 21 Jan 2021 04:52:27 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 04:52:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 04:52:28 GMT
ENV ROS_DISTRO=dashing
# Thu, 21 Jan 2021 04:54:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:54:29 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 21 Jan 2021 04:54:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 04:54:31 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 04:55:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:55:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 04:55:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Jan 2021 04:55:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jan 2021 06:25:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 Jan 2021 06:25:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 Jan 2021 06:25:36 GMT
ENV ROS1_DISTRO=melodic
# Wed, 27 Jan 2021 06:25:37 GMT
ENV ROS2_DISTRO=dashing
# Wed, 27 Jan 2021 06:27:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jan 2021 06:28:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.8-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jan 2021 06:28:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jan 2021 06:28:24 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:6d8bd15f2f6189f24e8f1b5dc573a293c963565ab012ca6a42e51a3023e72e7e`  
		Last Modified: Thu, 21 Jan 2021 03:18:06 GMT  
		Size: 22.3 MB (22291204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e961f21c7ea83c265a6de2897b8255e9e03cf1d39b74fb208b4ca936c6a53c5`  
		Last Modified: Thu, 21 Jan 2021 03:18:00 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b017766c8f695603aa5da2f534135bd1fbe253f667ef6faa77a77c66be9ba9f5`  
		Last Modified: Thu, 21 Jan 2021 03:18:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb7679849b59188f62bf017de9112158370c1d2eee07a8d614ba382cf612b62`  
		Last Modified: Thu, 21 Jan 2021 05:12:20 GMT  
		Size: 841.2 KB (841181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd1c8ec76e1cf5b551b2db58eb684cae7c4a3219c7175d85b4bf9ea4e5fe998`  
		Last Modified: Thu, 21 Jan 2021 05:12:19 GMT  
		Size: 4.1 MB (4085304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf27b43dde6748aae4a2d48a18d094192f874983a13d5046c161f02d3e11ab77`  
		Last Modified: Thu, 21 Jan 2021 05:12:16 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26cb5182d75745719bf677aa2f51d17ba9e1bf00013e8a22efd1af4049f56b8`  
		Last Modified: Thu, 21 Jan 2021 05:20:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119a885d4483873c844073a84a7702b2546c921a8de2f4c9e8b0089bab916099`  
		Last Modified: Thu, 21 Jan 2021 05:21:10 GMT  
		Size: 153.3 MB (153282852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2195d45bce19254177ba08c4a418a9fa36deb62bdaa5c5418a348de9c4e66dad`  
		Last Modified: Thu, 21 Jan 2021 05:20:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ceb223ee69badb47930f1d709a920adc4640899d3508aa06037f512bfeb4c85`  
		Last Modified: Thu, 21 Jan 2021 05:21:37 GMT  
		Size: 48.6 MB (48558687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd49b9ffc9116b3b8257a15b65b111c8d1349cba3dab9c64f4af64ae92a000fc`  
		Last Modified: Thu, 21 Jan 2021 05:21:23 GMT  
		Size: 200.0 KB (200007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a3cc5dfc2d7bc8ef83282dd54e2209a46b21a272e5e54860b1a57af76f7cce`  
		Last Modified: Thu, 21 Jan 2021 05:21:23 GMT  
		Size: 2.0 KB (2050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4e0a6f56180e134f67fff31beffe1aa1256b22e5c78af72340bd2d7bcc6085`  
		Last Modified: Thu, 21 Jan 2021 05:21:27 GMT  
		Size: 3.2 MB (3249672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f523e8b699553da63f2fca8fc560d6c8a384c9574f22a3223a5544bc8c066216`  
		Last Modified: Wed, 27 Jan 2021 06:29:43 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66f987dbad626cbe7b930fcd6d5a425628b831494b0b583a07090f042b8dce9`  
		Last Modified: Wed, 27 Jan 2021 06:29:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0114b262344985833ed1bfacdf419caec3f7da37cb01f7457fde0f60c2d23e2d`  
		Last Modified: Wed, 27 Jan 2021 06:30:23 GMT  
		Size: 110.6 MB (110639598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472440e2443d65beede25f54a484a5ad7e641d2f3a4afc08f955dcecc5fe5e29`  
		Last Modified: Wed, 27 Jan 2021 06:29:47 GMT  
		Size: 10.8 MB (10813671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4549046cc45bc8be3bce10902ae2819accba891403b2623dd2969730152ebead`  
		Last Modified: Wed, 27 Jan 2021 06:29:42 GMT  
		Size: 635.4 KB (635416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d83d2616bb5396be2af44cca83ab646f5a9a41b5479244e10dce3a63a1b9a9`  
		Last Modified: Wed, 27 Jan 2021 06:29:41 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge-bionic` - linux; arm64 variant v8

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

## `ros:eloquent-ros-core-bionic`

```console
$ docker pull ros@sha256:1f87fb45c3fb2206a2d0d263bff1d8a1ed98eff95082c8ee31d098a48bc42c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:67728aad1dbf9862a6a22053bffcef42ff9f8867094ec752b871aea638a02a24
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278588058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37edfccaf6b945622788fa59772f36ebecb0add5e67218c8da1635a2bf5c940`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:37:37 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 08:38:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:38:10 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:38:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:38:14 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:39:15 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 08:39:54 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:39:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:39:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:39:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1788b23e27b1dcb9bce2b1984a84b7d31947919c2163f9ade029e5332d53050a`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947606753c8584163c9d0773abc0362654dab6bbbc4b9bfba5a0cb4f2eefe5ff`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc32392bda4b3149fab82011b47af99f0383238ba4b8512e9511a59fa420342`  
		Last Modified: Thu, 19 Dec 2019 08:47:45 GMT  
		Size: 28.4 MB (28396860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb28870019c0bdbda2621f8fb8eebc3e070b190e0081d00161bf4629228b6d66`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 457.2 KB (457226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd6f6f595fb36a05b0ee5a77cefa398fbe69ea89329d7b39e44d014b77ac06a`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3df7937065b6462f187e61fee4bd439fee17b170d67ac8133723ae0ad0bf8d`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 105.6 KB (105619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2771b910aaad0e851dedbe69f2541e1e824ed2aa8f38727952ede7ea89d7f`  
		Last Modified: Thu, 19 Dec 2019 08:48:40 GMT  
		Size: 70.1 MB (70069689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6b8110d43d20db1dd17be79b05a909412d13eadd0e237abf6e919675b7e794`  
		Last Modified: Thu, 19 Dec 2019 08:48:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:3d4c31c77f2e83cc5a95318ffc9ed90067a20144cedb07e63c75da4edfd507d7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233479263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea615de602da4668c67fb0edd21d6812d5ff8ccc9315f37d80ad0d636b20312d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 07:18:11 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 07:19:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:19:27 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:19:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 07:19:39 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 07:22:03 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 07:23:43 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:23:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 07:23:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:23:52 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455981857e9a410797e32fc0c529702018fc148c4f9d0c75e0761a06beca97f`  
		Last Modified: Thu, 19 Dec 2019 07:32:56 GMT  
		Size: 133.5 MB (133544797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c09f8172ff45416a62b29f2e242b4e1dfafebf97a0eb00a45e0987a8e903b57`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be10b58db720b2f091ed57e99a6b8792908ac7fb9a9dae6ea8349fffae5c68`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df52c99895d650c13b1545ee01b48e2f64de5bbd927573c077cdf46a4db7e606`  
		Last Modified: Thu, 19 Dec 2019 07:32:26 GMT  
		Size: 25.4 MB (25369629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd9644484caa92344ef25dc98de15e235a0e0f175c341d825f355e75a7f34ae`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 457.3 KB (457262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8449787a4d7a17919e9d9da626fbeb4ceb08944e85da16c1f2fc3e929852a`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f750c7df1c22431e41df26ec33d7c0ed7ce956e2676d7829c5fc8fb1aa5a33`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 105.8 KB (105758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85320bb83837978f50bbd3baf84dea4b922e0b0218feb192ee0c7421258cc7`  
		Last Modified: Thu, 19 Dec 2019 07:33:33 GMT  
		Size: 50.8 MB (50848227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4350cb886547c239fa13e66d7ad666bcb99708c8af8d8b1971c4c41f8d28798a`  
		Last Modified: Thu, 19 Dec 2019 07:33:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:267c5f54b703e3f2fa98f5555ea89a385017be0639a39c51805fcc13ab0dd4a5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252806848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e787a2aab2a27535f377ff8b689b1fba26ae61da489d7c24f661af218b8beee`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:36:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:36:02 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 09:37:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:37:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:37:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:37:23 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:37:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:37:34 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:39:38 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 09:41:03 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:41:07 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:41:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:41:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe70117b5d6348d6eb41e9752e5bca210f36e6c69d0a7eec87105e51fba6696e`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f1d24107e434232c8d8bfa81445e8130e3e7205bcb5c6b16fb0e07e2fa216f`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c5a73503e8f3989553eea5fc6cf7c1a8b585289912466247d2225e61491144`  
		Last Modified: Thu, 19 Dec 2019 09:50:52 GMT  
		Size: 27.1 MB (27084179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fbd814641bb8462a721a29b7ed9ca4e9652633b42b310e5527bf2306a8be5f`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 457.3 KB (457269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c23284ec32c560e586cdc2f45375ab8f898ecf1111e856dfcd540b06c5f29ea`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d310b2c92d7854ea0c4a842a6bbce7672cc6b6512c4c51095c89b27d05f900`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 105.8 KB (105750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a31c3e5f5c6d7bdff677a1c2ca244f9ed373f0d4abe4742c97676c2dbde2523`  
		Last Modified: Thu, 19 Dec 2019 09:51:43 GMT  
		Size: 57.4 MB (57400446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9c35595f41a6221be1b6d19e20a50234f79967a968819173bcee35c6de7d1c`  
		Last Modified: Thu, 19 Dec 2019 09:51:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

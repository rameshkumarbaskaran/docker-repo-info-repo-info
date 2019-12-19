## `ros:melodic`

```console
$ docker pull ros@sha256:53622f114bb197d282d214d6174e19c243d5ee8d5c605cb5ee9aba301567ca1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic` - linux; amd64

```console
$ docker pull ros@sha256:56b12ce9ab14a158b56336d7fbbf1de011d87cda514b0f32fd77827df42f8a8c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.4 MB (419392123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b23b8327e0c6d9af7ce96796e4a0554d1710236fe9c1fc5e75247e424c0f254`
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
# Thu, 19 Dec 2019 08:22:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:22:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:23:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:23:37 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:23:38 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 08:26:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:26:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:26:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:26:23 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:27:43 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:d27c5773ef4faea2ab4bb067f34730723b5e4e4e5124526e52f046d4fda6ff93`  
		Last Modified: Thu, 19 Dec 2019 08:43:29 GMT  
		Size: 6.8 MB (6776450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5aab8a595911e0f910e5bbc45fbaba1872d9b2ff7ddf0b8596fe487e6b35ed`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a691a8db646c53d5a2c1bc8133de575f671497f29ba26550912c360fe7c92e84`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224950fdddc8e9a7e0642acd70f24e007e024605e33623bd88fa78c701d7e738`  
		Last Modified: Thu, 19 Dec 2019 08:43:40 GMT  
		Size: 55.1 MB (55078634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b544deac8ac028cca15755fe7f73466c66453367d47613d71723e888966206`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 450.8 KB (450831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfeeeabb29071b671ff85ced5fe96a930389986cdb960d654b253f4cc981292`  
		Last Modified: Thu, 19 Dec 2019 08:44:19 GMT  
		Size: 261.2 MB (261186116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32130377944b2d86d62bf74958bd8765a6db237ce408848f094f9012bfd55da7`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f4332440558d0adb9cfebba043639b1cf26d2a5b0741c27295cd15f4bbcd27`  
		Last Modified: Thu, 19 Dec 2019 08:44:40 GMT  
		Size: 68.3 MB (68334967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm variant v7

```console
$ docker pull ros@sha256:ccfe308c17a0e677ecc384052b23e469680d809e45f2aa635d45ffabf6da2a6c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.2 MB (372218761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d463c5c602806461c174727773f1f51c9e8cc6bf7e8ef9df0efcbf0eed86e211`
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
# Thu, 19 Dec 2019 06:59:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:59:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 07:00:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:00:51 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:00:53 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 07:08:29 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:08:33 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 07:08:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:08:37 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:09:54 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:f74cc414b82f13364c01a11f261e8dfed1c196857c6ff34fb70f0ae05cdadfe5`  
		Last Modified: Thu, 19 Dec 2019 07:28:34 GMT  
		Size: 5.6 MB (5627378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df074ca58e1db5e1711022ecb5cdd76a220b6bcdad705ae5f2b4097dcea2525c`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b10ee1dff6220bba3f0494edd98e32dae244100726ac1d65948bcab451571`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8b3b5e870295ae6e91943a63475637fb09bd851a8b97e5d6538c2e8d5d02bb`  
		Last Modified: Thu, 19 Dec 2019 07:28:54 GMT  
		Size: 50.1 MB (50110869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005c3125f47e1a15eeb61825c4016a74ef84c311e2ebe39ecfdaa069d25c3d9b`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 450.8 KB (450781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09cdd58271001701d29f1fb4b54a02439e03b240e48983b5c3a314c47bf3b2`  
		Last Modified: Thu, 19 Dec 2019 07:29:37 GMT  
		Size: 232.6 MB (232619513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43581541e27c972fc18c3282a8cd3c06be9ee0e2ac22cac04e534064b4b5822f`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d810dbfbec2f7a9860a8d74cf4595e10a606f9c6c5b36b1b5fff09e4498bce2`  
		Last Modified: Thu, 19 Dec 2019 07:30:05 GMT  
		Size: 60.3 MB (60258526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cc6647386c614121fb5a83d73135ec42dfd021d68232451d1cbf1b601de3cd9d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 MB (395850107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b1f1f4aeb2e8fc3b3d375fc521f707f54d81076199339adfba7ea9857aaf48`
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
# Thu, 19 Dec 2019 09:18:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:18:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:19:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:19:35 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:19:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:19:53 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:19:54 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 09:22:38 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:22:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:22:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:22:52 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:23:59 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7031f0dfe1a04190bd784e5140bfe7a474f680cb88e49c049b6a2d371157dc0d`  
		Last Modified: Thu, 19 Dec 2019 09:45:57 GMT  
		Size: 6.1 MB (6093647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9585186791b7513d0e7887faa2eda00c150730fa9d288e256287ba4f707523`  
		Last Modified: Thu, 19 Dec 2019 09:45:55 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11f78613907751037733fccddc9dc67a836dd5b544bbf0b2c8923d21c01acac`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc647a64f2557054880db6223f6f3db4ff16b7bb70d6134c12db30f9e832725`  
		Last Modified: Thu, 19 Dec 2019 09:46:13 GMT  
		Size: 52.9 MB (52924497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a00593d29483a6884bc23393ee1795cfa7a81f65260cfe008652fccbd45e1c`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 450.9 KB (450888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccdbbaf4322fbc1f325853bb8914640a8811d91977624dee8288ac558140ca`  
		Last Modified: Thu, 19 Dec 2019 09:47:04 GMT  
		Size: 248.9 MB (248945060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db7cb2524131c6a2ce80bdff4abf63cb47681674f1f9ac63006daddf3cb5f8`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd098fc5b3755d3c0b1a3a95eff7e7379b198075d3da50b35407d6988d8cf004`  
		Last Modified: Thu, 19 Dec 2019 09:47:30 GMT  
		Size: 62.8 MB (62841501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

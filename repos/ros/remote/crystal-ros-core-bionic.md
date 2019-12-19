## `ros:crystal-ros-core-bionic`

```console
$ docker pull ros@sha256:657b0f5372752f0caf1b7990257bfb00f9e3016004950898d1be51bafa8f988e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:crystal-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:7f35c16542988c0ef1ac8aeb535e00342d8987532f53fc1462e350835dfd3a90
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259123447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e8cdce41b460e131c938105da9232e4ee08cc8aa49e80d42537a5f5b151590`
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
# Thu, 19 Dec 2019 08:35:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Thu, 19 Dec 2019 08:35:41 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Thu, 19 Dec 2019 08:36:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:36:30 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Thu, 19 Dec 2019 08:36:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:36:35 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:36:35 GMT
ENV ROS_DISTRO=crystal
# Thu, 19 Dec 2019 08:37:12 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:12 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:37:13 GMT
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
	-	`sha256:a86030d638550e81441f6da252a39797dab06865ce8ae14d463520e39e559649`  
		Last Modified: Thu, 19 Dec 2019 08:46:54 GMT  
		Size: 2.8 KB (2817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece8d38b909fe9607211392b727e7abee82002662332dc24c59bd968262065ab`  
		Last Modified: Thu, 19 Dec 2019 08:46:54 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310b73e844c0bae862a60484f39bb21b8c75356859ce082b30a682d1ef26e2b0`  
		Last Modified: Thu, 19 Dec 2019 08:47:02 GMT  
		Size: 28.4 MB (28396283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c13ac15ca13fc9b9d483336787f1035fe6b8836045b7a74cf5cc24bed939a7`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 1.0 MB (1002074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6ac3372c0d80649a253ece5234d2d9bfae4edb579505f69cc9f07a078ccd61`  
		Last Modified: Thu, 19 Dec 2019 08:46:52 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafe2728baa9ac7688525ff6c0fe0f0dded176856dbbdcabb28f67f1bf7a32af`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 105.6 KB (105620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1cd2a45d530f0795cf310a6e2438d26760a22940b1ed713409c4f0009d5664`  
		Last Modified: Thu, 19 Dec 2019 08:47:12 GMT  
		Size: 50.1 MB (50059390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015dc116ee4bc9e060c26794661883b9d1869733d94d4a2fe53ba8c6824bd4b4`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:crystal-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:afef2b896e27833f74529f2fc0b22e87a693965c256cb4f7e7fbc648d7218f94
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235485435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfab838c40e7efdbe85d7784ee019e8915a9bb0629c148ec6c4614993f711da`
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
# Thu, 19 Dec 2019 09:32:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Thu, 19 Dec 2019 09:32:27 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Thu, 19 Dec 2019 09:33:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:33:26 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:33:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:34:05 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Thu, 19 Dec 2019 09:34:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:34:15 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:34:16 GMT
ENV ROS_DISTRO=crystal
# Thu, 19 Dec 2019 09:35:26 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:35:30 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:35:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:35:31 GMT
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
	-	`sha256:ddaad5616b153dafb9a1cece2bd1880697bfd9f89a4531619040669a22459adc`  
		Last Modified: Thu, 19 Dec 2019 09:49:46 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf9be4f838e5862dc76bf33c2d24a0a9b2d176dd2d4c5491b59d98f01506d14`  
		Last Modified: Thu, 19 Dec 2019 09:49:47 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20055ce1eeea4c2d78a23b5f2b4909d8a7e6ff15440cb5147600c1fecf62a2ae`  
		Last Modified: Thu, 19 Dec 2019 09:49:54 GMT  
		Size: 27.1 MB (27081012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f6068b42c17866001a64eb7b6d46cf01eb5722f3609342507f5efa8f8e5c83`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 1.0 MB (1002139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77a0280efc0979acb8b1955435e585d751968599d740568d671bbe02a6d860`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0788190750103e17a53267e42e2cfe2bb81c9e9fee4931bd11a9f4c9d2c8b734`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 105.8 KB (105751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a50324387b00b8e5b96f1f213f45d6266df3fadf4a04d22307e8ffa36ded85`  
		Last Modified: Thu, 19 Dec 2019 09:50:00 GMT  
		Size: 39.5 MB (39535906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb418d6d36d90e7c0bbab69f5f4dd6f504fa6f6dddbdb5786e86986716064c7`  
		Last Modified: Thu, 19 Dec 2019 09:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:kinetic-ros-base-xenial`

```console
$ docker pull ros@sha256:f0ba349754fbfb28ea273a202032a691f650348bb1cd96335b21d843046a74d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-ros-base-xenial` - linux; amd64

```console
$ docker pull ros@sha256:5bf8d73481a3be996cba1f449cdb9ee611c86ffb6098f46d9d1518ee8bb28fb8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.4 MB (385362973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c2b2abbe31bd6239f97d00b57cb7491635d0ccb4a6b4b67824278ad80fef2c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:12:20 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:12:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:12:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:13:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:13:08 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:13:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:13:18 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:13:18 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 08:15:12 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:15:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:15:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:15:14 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:16:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457aec0e6396b59c9e392c1756f39b2b16eb4ec642ee9a245fa6be156e84fdcd`  
		Last Modified: Thu, 19 Dec 2019 08:40:28 GMT  
		Size: 6.9 MB (6938120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d003c6fb07330daa4bab99fc349a9e9c1ee91e901bdf12f937f4c57ce8abe53`  
		Last Modified: Thu, 19 Dec 2019 08:40:26 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26c6e39341421afd15b05b54468ad0588a45bb8baf5b09aa423d645cd9d2bd`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc96488ffb5e99fa546e5907bc1dace89168ad9711f3908be178fe24c491eaf9`  
		Last Modified: Thu, 19 Dec 2019 08:40:41 GMT  
		Size: 54.8 MB (54776706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc49700f647fe9094f423ff327d7eda8f4eaf317dde051ee8908c3138022a183`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529abb518cdf8d1e75141dca5c706d8a5e89944cac45b886fe844805d35ba5a`  
		Last Modified: Thu, 19 Dec 2019 08:41:10 GMT  
		Size: 193.5 MB (193541433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b27f5c340563860d4de224aea7cbaa86d27ef8124169500eded483af45ba0`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab15a38df195254a32dddf96ea9f512cf642931e5b6473721f49382f664eb5d8`  
		Last Modified: Thu, 19 Dec 2019 08:41:38 GMT  
		Size: 85.5 MB (85517553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-base-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:883106104357072e4011916e99987243b724d24ef59237c780d365dc3b9d7c9b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336647680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46c93cd10743885e0475a762078bed4e9d0b46679b0faf540c74c4a3de7dfc5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:13:48 GMT
ADD file:1eb3c4071d32b0a8303ba31b94ccbe4e41eeb6f7bd63e421422b6ec57189510f in / 
# Thu, 19 Dec 2019 06:13:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:14:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:14:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:14:16 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:41:13 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:41:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:41:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 06:42:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:42:55 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 06:42:56 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 06:43:17 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 06:43:20 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 06:46:06 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:46:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 06:46:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 06:46:12 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 06:48:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9254c1ab1fb38e9ae02953d2c8a3049d31856bab7053e388f23cef210597bbe`  
		Last Modified: Mon, 16 Dec 2019 15:43:26 GMT  
		Size: 38.8 MB (38831502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8a4af221588d688f657274b15fea720573656acf9ece94a8510b1488318419`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaefd48a3cde2542d0443d4731a3b7074e41344bb62c8327297c61293398164`  
		Last Modified: Thu, 19 Dec 2019 06:16:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d3331f5ad1f67a66c9fa286fc830645fa2e844e3e2cc1d60522c436fd72205`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2b81ce07a861e3a76db0d541986a49a354ef54454ff21d24bf645e67fde13a`  
		Last Modified: Thu, 19 Dec 2019 07:24:52 GMT  
		Size: 5.7 MB (5702275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07255d05e2ac7c0f25c2d22f1e93030a378e873c66223e96f2a65d09258f6d76`  
		Last Modified: Thu, 19 Dec 2019 07:24:48 GMT  
		Size: 13.1 KB (13104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0768a4e7c85d399dca304c025c827c978b1bcbb05e169d5e80ea777b76c8bdb1`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800347818d646ad2df8d6e1a34ac1dbf389baac9807e9431b22bfe71278380c8`  
		Last Modified: Thu, 19 Dec 2019 07:25:08 GMT  
		Size: 50.3 MB (50348758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b767d331b13e63935e560445c037945b0c0aa0c74a025bd89c2755f8ed3142`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 450.8 KB (450788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aeee38c540e19a6a1d2fe06d366d70fbdf94076ff4975fb8e805951ab205a0`  
		Last Modified: Thu, 19 Dec 2019 07:25:44 GMT  
		Size: 165.0 MB (164971334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567b050311edafb3addc3b75044375077583f5c4d2be8da079ccb578ca6ca150`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93dcb7dc9e66913c87f9984e99144e1f72b2d1c4e5ecaeb35a1b7c944cb1ee`  
		Last Modified: Thu, 19 Dec 2019 07:26:14 GMT  
		Size: 76.3 MB (76327967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-base-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c614530517115569e9ae3f0044d6a421ebbd13ac383f336764f90dd7b4a53f3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350416724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e990888d3b78dd7adb0ad00f1e21db0d501a066cbb1d53c31ccd133119d6c17f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:56 GMT
ADD file:ef40ad352b3111bab843b916e802c7cb18aeccc96a65fe9a7a5330572431e7c7 in / 
# Thu, 19 Dec 2019 03:54:59 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 03:55:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:55:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:55:11 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 09:07:10 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:07:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:07:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:08:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:08:45 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:08:46 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 09:10:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:10:48 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:10:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:10:51 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:12:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b8d9a83fac1745f67aed1e924445fc9a89cd885fe70d0e1e335cbe4791f490b5`  
		Last Modified: Thu, 19 Dec 2019 03:57:28 GMT  
		Size: 39.9 MB (39875399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b9cc76ef947c73adaf3c9e2dd2f8da166e815b37d431b9baae7aebe84096fe`  
		Last Modified: Thu, 19 Dec 2019 03:57:19 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d286195ea15592986e2820cc7366deda87cc2802b6cfe82a6f5388aceb4a4`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120fa5dd162f3d2fa3a1452a4d909074c6ffcba06016d39e5781581ec1ec5f88`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df16651e3000bf2b6ae3cc1a8de5b7bde1ca91f2aad31aeb231f24ccf0621c10`  
		Last Modified: Thu, 19 Dec 2019 09:42:09 GMT  
		Size: 6.0 MB (5959610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76792d633ca9466c8e705ff4072fc431f386601da8441f84320f135fa15f177`  
		Last Modified: Thu, 19 Dec 2019 09:42:07 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a02948fb7dd58f67c357b01591ed9a5340d4569b8af575f92538c569993d59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e98ef3031817ddbe31b799a64b5e4bd9292394da1ca7e29cd7a6c004d15d8a1`  
		Last Modified: Thu, 19 Dec 2019 09:42:23 GMT  
		Size: 52.1 MB (52072413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c9ea297fd5aadfda1a295cae5f39632d3547eab77874341a70adc4d25bd59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 450.9 KB (450886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7ce4c6453b3968056ea13fd280e8ce590d9140c330ccd73152d4a89fa919fd`  
		Last Modified: Thu, 19 Dec 2019 09:42:58 GMT  
		Size: 174.2 MB (174224631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d922cb7a8f5abf9067bfd287531cd8808086a55c8aa5d11e24fb2f2f52335930`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19c43c9a069a6b32b2f9d9a0f2a7d2440dc58dd7dead223863bd4df11bcc96d`  
		Last Modified: Thu, 19 Dec 2019 09:43:29 GMT  
		Size: 77.8 MB (77818771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

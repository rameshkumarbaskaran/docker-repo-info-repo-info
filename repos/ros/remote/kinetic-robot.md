## `ros:kinetic-robot`

```console
$ docker pull ros@sha256:cc474e6bef4a9b53199b9772e61fa26272b8cb85c5d273776ddc51b3d8fd39f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:7ac94b16f762910c5170fcead08ae38b8982d85a24109360a715b52d96e19631
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.4 MB (379371709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764c8f1e40c9c917db8cd8acdd1b6f7c58742297a5a95bc9147e0492e6ff35bc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Apr 2020 01:08:29 GMT
ADD file:4fe14d9555e739e4d006eecb273a2f4a53e6dbe93bd0db26d5f999168b5d4114 in / 
# Fri, 24 Apr 2020 01:08:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 01:08:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:08:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:08:35 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2020 00:20:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:20:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 May 2020 00:20:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 May 2020 00:20:29 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2020 00:20:29 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 May 2020 00:20:29 GMT
ENV ROS_DISTRO=kinetic
# Wed, 27 May 2020 00:22:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:22:55 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 27 May 2020 00:22:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 May 2020 00:22:56 GMT
CMD ["bash"]
# Wed, 27 May 2020 00:23:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:23:46 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 27 May 2020 00:24:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:25:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e92ed755c008afc1863a616a5ba743b670c09c1698f7328f05591932452a425f`  
		Last Modified: Fri, 27 Mar 2020 14:20:10 GMT  
		Size: 44.2 MB (44247132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fd7cb1ff8f489cf082781b0e1fe0c13b840e20147e8fc8204b4592da7c2f70`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee690f2d57a128744cf4c5b52646ad0ba7a5af113d9d7e0e02b62c06d35fd14c`  
		Last Modified: Fri, 24 Apr 2020 01:09:45 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3366ec435596bed2563cc882ba47ec25df6be2b1027e3243e83589c667c1e`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe397fd4c1e77566498dcb90332692256b0920178db8a904ae083b626769532`  
		Last Modified: Wed, 27 May 2020 00:50:50 GMT  
		Size: 5.4 MB (5361626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd84aa41becf728df631156197d9b172bf93b09e757aefd3e758137fdb12cafc`  
		Last Modified: Wed, 27 May 2020 00:50:49 GMT  
		Size: 13.1 KB (13103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37784db706b30a2c43426aa060b920d870b15cb4109db9129a5a989974176523`  
		Last Modified: Wed, 27 May 2020 00:50:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e1aadf03f91251743541ccd356da185cab6107033a6a92266427969535582b`  
		Last Modified: Wed, 27 May 2020 00:51:33 GMT  
		Size: 187.2 MB (187179519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f69e1993e08b26edf7d15b861dc5686bc5cdab0e541ab4490ac74ce7c00328`  
		Last Modified: Wed, 27 May 2020 00:50:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cc7e3cb0fc78d1dddbdb7f276cc883c0fbe2b041964d70c35b84991b758ce0`  
		Last Modified: Wed, 27 May 2020 00:52:07 GMT  
		Size: 57.2 MB (57240848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee4f03e90226efb806224e9545e910ddad9952ffc3064b623840ab0af2e3b2a`  
		Last Modified: Wed, 27 May 2020 00:51:38 GMT  
		Size: 257.1 KB (257121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ac50bd113c0fc610ef6618f4d5defd434934f4c45b4a69832d47fa09f6847d`  
		Last Modified: Wed, 27 May 2020 00:51:52 GMT  
		Size: 63.6 MB (63572631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d423847a7ca574457ed967c81e4d423126219e10589d4ac242755883a0dd8404`  
		Last Modified: Wed, 27 May 2020 00:52:35 GMT  
		Size: 21.5 MB (21497760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:3e9a5a68beb9611e1e6e128b591138d10da66592300ce96a5d2c3ab15f28d916
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330490838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82b36103c544aa6a6b3c8612f2650398f25d402ced3e4638dba28675fecb08`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Jun 2020 02:04:31 GMT
ADD file:6cc12f5b0908f30b9097dd8947a769888e2fed5c2a25671d1e4cd93ac0ef7a2a in / 
# Wed, 17 Jun 2020 02:04:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:04:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 02:05:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 02:05:12 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:10:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:10:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 17 Jun 2020 03:10:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 17 Jun 2020 03:10:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jun 2020 03:10:08 GMT
ENV LC_ALL=C.UTF-8
# Wed, 17 Jun 2020 03:10:09 GMT
ENV ROS_DISTRO=kinetic
# Wed, 17 Jun 2020 03:13:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:13:16 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 17 Jun 2020 03:13:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Jun 2020 03:13:18 GMT
CMD ["bash"]
# Wed, 17 Jun 2020 03:14:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:14:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 17 Jun 2020 03:15:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:16:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:964b1ad4ea33c6edf524b0fba723b83aa90e37a66419cf5e514392304bd73309`  
		Last Modified: Mon, 18 May 2020 15:50:57 GMT  
		Size: 39.0 MB (38964390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b1c0566b01f5b9247bdf23fee3adfd14071d248058523063939ce8c482863c`  
		Last Modified: Wed, 17 Jun 2020 02:05:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5534a4581c7bc4061f7f3c35130d6daa15345f5791fe5c4c90cbe06def252991`  
		Last Modified: Wed, 17 Jun 2020 02:05:53 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0db3772af551e10afa4bced33b87cf3a0716943e901e4a9da41b1caac84b55`  
		Last Modified: Wed, 17 Jun 2020 02:05:53 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b88d1e1f8eaab795890a44aba254120710460cd3c229c81d2cb305a5ef9c219`  
		Last Modified: Wed, 17 Jun 2020 03:52:39 GMT  
		Size: 4.6 MB (4614611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e8cecde1e2d564293841b0d9d6b26c76fa0aa603f9ad1883d43f11436879c0`  
		Last Modified: Wed, 17 Jun 2020 03:52:37 GMT  
		Size: 13.1 KB (13104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9136828cd2351f794e02e625555b17588dbd52b1a4b35e3f7e26122b4d56aae9`  
		Last Modified: Wed, 17 Jun 2020 03:52:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0858d8df7908efcf17daa7a718f5ef97381d0c3faa4411b28faa8f71692d73ce`  
		Last Modified: Wed, 17 Jun 2020 03:53:36 GMT  
		Size: 168.0 MB (167990816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac4d3368b30a5de5b79fd1b2be37bb3c6429704537df5b4d285d9d0e019172`  
		Last Modified: Wed, 17 Jun 2020 03:52:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07868dd899caa834aa89cbe99dbe455161839e250dc222109b94d7d8b9e4750`  
		Last Modified: Wed, 17 Jun 2020 03:53:58 GMT  
		Size: 42.9 MB (42891228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f65b34e704ea516b44679fd2cabb7606d59e98ddf086d3446a28de21d744d0`  
		Last Modified: Wed, 17 Jun 2020 03:53:44 GMT  
		Size: 258.0 KB (258033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176c25b3453cfdf8cdb2a0e3128187e22f604c3076e4bd1b99ee7835fbdcf368`  
		Last Modified: Wed, 17 Jun 2020 03:53:59 GMT  
		Size: 55.5 MB (55499848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb57a2a0fe505fbbfd3993e3dd8917ff746d4e2fa7241f8a220acffe8d9aea69`  
		Last Modified: Wed, 17 Jun 2020 03:54:12 GMT  
		Size: 20.3 MB (20256859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c143efdeb2c0d6947d52bcb30809a6326e4b2bfcad906fe3f806f641ea2fbc3e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344864016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0668839d46db3c46876ebcc52a48f5e62ddb0b19ffac3fc427fd773c704dc2c1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Apr 2020 00:20:42 GMT
ADD file:24038b6c5a9bab991785fab56202fc43de85e0749e57fcfc361de8aeff302309 in / 
# Fri, 24 Apr 2020 00:20:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:20:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:20:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:20:58 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2020 00:41:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:41:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 May 2020 00:41:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 May 2020 00:41:20 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2020 00:41:20 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 May 2020 00:41:21 GMT
ENV ROS_DISTRO=kinetic
# Wed, 27 May 2020 00:43:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:43:43 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 27 May 2020 00:43:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 May 2020 00:43:45 GMT
CMD ["bash"]
# Wed, 27 May 2020 00:44:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:44:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 27 May 2020 00:45:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 00:46:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca96533948cdaf1fc84922a44248fcf915a3f526b46555bb96090bed658b00d7`  
		Last Modified: Mon, 30 Mar 2020 15:49:17 GMT  
		Size: 40.0 MB (39968791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72780e1c95403020a1883a1054d9d48b7a5ad2d940ba2d57ae211369a19685`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d962f0171bca79269769ac242507e3f65f2dcbb86de35ecaf164d37b8a89c9d`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179f057dc5a95fd6368cf61fa48d9e2d85af21b750813b8dd17b7ad44752c342`  
		Last Modified: Fri, 24 Apr 2020 00:22:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93023f2f216c169a5941011eb6b2957949ec380108783c274564c708f65788b1`  
		Last Modified: Wed, 27 May 2020 01:25:37 GMT  
		Size: 4.8 MB (4819497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2969a52a11c9abfa753477caab284294b10931bcb9b0f829fd63bbaf9e3f861d`  
		Last Modified: Wed, 27 May 2020 01:25:36 GMT  
		Size: 13.1 KB (13106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8b3ad5c344821edc0e405d07130908553f76becc77e2a9eb24c635b4a1b31a`  
		Last Modified: Wed, 27 May 2020 01:25:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d73153c6002fbc045a5f9eb1554dd220df3c4564631283a5a0f50eed745e7a`  
		Last Modified: Wed, 27 May 2020 01:26:35 GMT  
		Size: 176.0 MB (176049755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8c55c82142a5b720f4fcae77c69d419f39dcb79517290fb7c85d65853ac993`  
		Last Modified: Wed, 27 May 2020 01:25:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1436081de1709d4d59b56419e5ea1580d115747f72ea73df7f1a9863cd761af2`  
		Last Modified: Wed, 27 May 2020 01:26:56 GMT  
		Size: 46.0 MB (45952763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043d41252c8ff4c3f358e0fa5208fbb98c448fa0ae29f594ad93f1a140dfddbd`  
		Last Modified: Wed, 27 May 2020 01:26:43 GMT  
		Size: 257.2 KB (257172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e81ab65b65a6d8de9094038e94336fa9e8e5886ab7b301d72df382226a72c`  
		Last Modified: Wed, 27 May 2020 01:26:59 GMT  
		Size: 57.3 MB (57285053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c8c9e80a27f8388d2c1ddcb60478dca502a2e8d93c418c17e3f7a5dc6e8fe2`  
		Last Modified: Wed, 27 May 2020 01:27:16 GMT  
		Size: 20.5 MB (20515963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

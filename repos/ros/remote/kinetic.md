## `ros:kinetic`

```console
$ docker pull ros@sha256:636ce2f45e378a94defeb7018eaf56f36fc436c84b034f8f911f3dd833f1279f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic` - linux; amd64

```console
$ docker pull ros@sha256:93a496e827d067811ba72da0f484a6a3d14930e4f9989ec2b38df8b9cc0eec8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.2 MB (360158904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de84e9adf03c169a1f98474a23d53f64488f9850d25b565fa8ea5ebf62e62ec3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:06 GMT
ADD file:4dd75f16753c9c921fd05b1d0ed5b425d74d87405a76a0b3afcbf9723a50d1ce in / 
# Thu, 17 Jun 2021 23:32:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:32:08 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:32:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:32:09 GMT
CMD ["/bin/bash"]
# Fri, 18 Jun 2021 01:36:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:36:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Jun 2021 01:36:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Jun 2021 01:36:23 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jun 2021 01:36:23 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Jun 2021 01:36:23 GMT
ENV ROS_DISTRO=kinetic
# Fri, 18 Jun 2021 01:37:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:37:55 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 18 Jun 2021 01:37:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Jun 2021 01:37:56 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:38:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:38:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Jun 2021 01:39:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:61e03ba1d4149ac4eb681c6bf75aef8ac4b3f0d6fbb08e9623c4089889396fc8`  
		Last Modified: Sat, 12 Jun 2021 00:25:16 GMT  
		Size: 46.5 MB (46496785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb39f216bd4e336f9b78584bae0f6bcb77150107471d8d67d3b8abfbdea46a`  
		Last Modified: Thu, 17 Jun 2021 23:34:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489abdc9f902f737bfef2c0c7ff5c35ca9b3ca11e73405a472f31a25f2dcc69`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999fff7bcc2450fcf1210182802f3907e35cd7cf7569568bd2a179b9144d9c57`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dee46e5af810171e31b4b35e27558f45782fb006de122f2546e5ac6223e0a55`  
		Last Modified: Fri, 18 Jun 2021 02:21:24 GMT  
		Size: 5.4 MB (5364295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dea51cd413c41fe30940f98c9baa08e19ec842e9f047b9aca8e4cff5594cbf`  
		Last Modified: Fri, 18 Jun 2021 02:21:23 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d10f41c924f2a8459161d7db16e0657b6c3fca53699a511a34e7d41b0df092`  
		Last Modified: Fri, 18 Jun 2021 02:21:22 GMT  
		Size: 15.3 KB (15292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1d8faebb89e33cd353f0212c76e77bbffd7f078890661ce66d648965b3d203`  
		Last Modified: Fri, 18 Jun 2021 02:22:03 GMT  
		Size: 187.2 MB (187160978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21703352205d9f4266473491592b343f90e15750898a6b4756df99776a075241`  
		Last Modified: Fri, 18 Jun 2021 02:21:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bec23c64ab5c7890c60f3e104df58d70f818a843277b74ca16e0dc07013955`  
		Last Modified: Fri, 18 Jun 2021 02:22:24 GMT  
		Size: 57.3 MB (57250445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88bc24d70588b116ae88f6966a6a202f306d9b1a988deac2d177d083b2da7bc`  
		Last Modified: Fri, 18 Jun 2021 02:22:14 GMT  
		Size: 293.1 KB (293144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1257fbf5f818f022eadb79421d2d94b22361a983a18a4578be8ba508cb0392c0`  
		Last Modified: Fri, 18 Jun 2021 02:22:26 GMT  
		Size: 63.6 MB (63575994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:3514be578da03c4dae04da89772514ce66ebb45680157843aa74927236bb2f07
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311669266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b3f2625f655d8f2dcde3d4508d2825c9cda5df1613740cc93b479b0980ff45`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:33:04 GMT
ADD file:ef24ce1c15acdd071b2d61cd27d2840f1fa5eda4937dfe8746997eb677b1451b in / 
# Thu, 17 Jun 2021 23:33:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:33:06 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:33:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:33:07 GMT
CMD ["/bin/bash"]
# Fri, 18 Jun 2021 00:29:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:29:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Jun 2021 00:29:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Jun 2021 00:29:47 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jun 2021 00:29:47 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Jun 2021 00:29:48 GMT
ENV ROS_DISTRO=kinetic
# Fri, 18 Jun 2021 00:30:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:30:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 18 Jun 2021 00:30:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Jun 2021 00:30:53 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:31:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:31:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Jun 2021 00:31:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bee35c084ef2789f844b87c031d55b07186255622024a15b526838f71500485a`  
		Last Modified: Thu, 17 Jun 2021 23:36:42 GMT  
		Size: 40.3 MB (40312433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f4e7436b523284825c35db6cb48a7c20c8d5388815695277126f528b2b4537`  
		Last Modified: Thu, 17 Jun 2021 23:36:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5c9e5711d0203aa41ec7750be25bd3bdd00b90388fde5a0d603523354eff4e`  
		Last Modified: Thu, 17 Jun 2021 23:36:34 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d1eba314dc97cbd3e70e1b857a42881405eefe61a235d56722dbf0df809d73`  
		Last Modified: Thu, 17 Jun 2021 23:36:34 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5930f6d7c7ccb8bd3795bd0d94af884f0a9f95c6b699e47ebf41c41e3001a858`  
		Last Modified: Fri, 18 Jun 2021 00:45:34 GMT  
		Size: 4.6 MB (4615682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c89ce215aaca078da4221c4d14714d8cd4134d2aeec0c05e3ce3af98c55c037`  
		Last Modified: Fri, 18 Jun 2021 00:45:33 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790ddb7cdf85392eba956848eb9f90f6cd0ca3a1b90cf3f279547a64be4ae34c`  
		Last Modified: Fri, 18 Jun 2021 00:45:33 GMT  
		Size: 15.3 KB (15292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b2dcfe56a94dffc7fde73d7ac3536506f30a2f8ea201701cd36d414c965319`  
		Last Modified: Fri, 18 Jun 2021 00:46:17 GMT  
		Size: 168.0 MB (168034337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d572520c93feba7cb3ee2b4b1a8ed6de5c311bd81f582c33f73507653a1e4603`  
		Last Modified: Fri, 18 Jun 2021 00:45:33 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d7072639f5c50d212ecab0d5ca3145790aa875e642fd60fbd879f2aa534da5`  
		Last Modified: Fri, 18 Jun 2021 00:46:39 GMT  
		Size: 42.9 MB (42894646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cb378cb5724d93bd55641fed615e4b4566eda5100a5c87351ef984eead43bd`  
		Last Modified: Fri, 18 Jun 2021 00:46:31 GMT  
		Size: 293.2 KB (293166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc747c100009636799f3daaa7f5f7fb1200075cab4c30e48e73b31431f045ddc`  
		Last Modified: Fri, 18 Jun 2021 00:46:42 GMT  
		Size: 55.5 MB (55501753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:09b05820d670dc4a265f6dcc4f643ce4fc33949fc364725a8de6d0248882665c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325640560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb793f4cd7b170dd3ef8d9a40eba73da2010db223506a5b4cd96ab048e662512`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:54:40 GMT
ADD file:2675f90ace0ec88b2cdadc737d15d701b544bf2113480e898d0014a79dca13c7 in / 
# Thu, 17 Jun 2021 23:54:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:54:42 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:54:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:54:43 GMT
CMD ["/bin/bash"]
# Fri, 18 Jun 2021 01:08:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:08:47 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Jun 2021 01:08:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Jun 2021 01:08:48 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jun 2021 01:08:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Jun 2021 01:08:49 GMT
ENV ROS_DISTRO=kinetic
# Fri, 18 Jun 2021 01:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:09:46 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 18 Jun 2021 01:09:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Jun 2021 01:09:47 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:10:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:10:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Jun 2021 01:10:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e2a24739a48e2c634f94c2cb69ead6b0ff1c84cedd9624eb29560b83c3eb6e0e`  
		Last Modified: Sat, 12 Jun 2021 00:25:19 GMT  
		Size: 41.2 MB (41239907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6732798425e9389fa6bd92caa59cd7de853b4cf01a7166724e26a430ec7211f`  
		Last Modified: Thu, 17 Jun 2021 23:57:28 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0af2bd04c3cb9d221318d494c05b29dd4b7c46886de97baee11fbd40723ab8`  
		Last Modified: Thu, 17 Jun 2021 23:57:28 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835469060484e7130eb258c8dfae8e4b1f8035c63bba23ab6e4f3e9b53a6cf1e`  
		Last Modified: Thu, 17 Jun 2021 23:57:28 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6c5516d91222e4ab20e59131499e0e6634037398137ff5e8fafe63f23745db`  
		Last Modified: Fri, 18 Jun 2021 01:30:44 GMT  
		Size: 4.8 MB (4821026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b73a6369b56463a3ab8668ab07fc1ae8aa54551838987cf3acd46f7dae243c6`  
		Last Modified: Fri, 18 Jun 2021 01:30:43 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd90311091e07444c6bec45b5ecce522ae94d527d4350d05e21bd3479911613a`  
		Last Modified: Fri, 18 Jun 2021 01:30:43 GMT  
		Size: 15.3 KB (15293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add027dfbb07933e127e94649626c0d2c6696337cdf8eea05e781db7e9face50`  
		Last Modified: Fri, 18 Jun 2021 01:31:22 GMT  
		Size: 176.0 MB (176018919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03a6c62ff8157895ea7ef3e763fa3049b55594e2db3ce47f2ec757f68852cb1`  
		Last Modified: Fri, 18 Jun 2021 01:30:43 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4501fb1e4cd87f53e7a8521f086c0b97e7a8ef2cad72e5bc3c2451e60a2aaaa`  
		Last Modified: Fri, 18 Jun 2021 01:31:46 GMT  
		Size: 46.0 MB (45953207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704173447f2d9215e352c7a94ab1b4f74076c8ef610d00b584e036a0c3a10ed7`  
		Last Modified: Fri, 18 Jun 2021 01:31:39 GMT  
		Size: 293.1 KB (293147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc12bdc4eaaabdc09276e817282b107e4fd13c106239317845f9399c92c38459`  
		Last Modified: Fri, 18 Jun 2021 01:31:49 GMT  
		Size: 57.3 MB (57297149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

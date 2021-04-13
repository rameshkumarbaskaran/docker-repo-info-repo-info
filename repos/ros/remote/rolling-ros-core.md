## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:67dfafadb29f894ceb346c7a606c1c1070e70707c10fd7f76bb855fdf3cadbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:2c9344f3fdc56061232fc54e05fe01597fd25c4449d8100e4336a5fb7a3fcab0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139674197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682eb6b487d181171b5ce8692b34df2f1c38f2b2a6bbb003f8885a0e3965d191`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 03 Apr 2021 00:53:06 GMT
ADD file:27277aee655dd263ee698d1f2fe17f0b1dbba740615bcac8642723a6ac0d62be in / 
# Sat, 03 Apr 2021 00:53:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 00:53:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 00:53:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 00:53:09 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 02:08:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 02:20:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 02:20:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 03 Apr 2021 02:33:42 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 03 Apr 2021 02:33:42 GMT
ENV LANG=C.UTF-8
# Sat, 03 Apr 2021 02:33:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 03 Apr 2021 02:36:34 GMT
ENV ROS_DISTRO=rolling
# Mon, 12 Apr 2021 19:00:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 12 Apr 2021 19:00:12 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Mon, 12 Apr 2021 19:00:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 12 Apr 2021 19:00:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a70d879fa5984474288d52009479054b8bb2993de2a1859f43b5480600cecb24`  
		Last Modified: Thu, 01 Apr 2021 15:20:06 GMT  
		Size: 28.6 MB (28569016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4394a92d1f8760cf7d17fee0bcee732c94c5b858dd8d19c7ff02beecf3b4e83`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6159c56c084c858f5de2416454ac0a49ddda47b764e4379c5d5a147c9bf5f`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7c5d2d7a6606006c3c9ad68491e77516419c59fceb2f4c04ca5580c96d8501`  
		Last Modified: Sat, 03 Apr 2021 02:40:16 GMT  
		Size: 1.2 MB (1182070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccd2266e6deaba5ba5682d19318df74543102cf36e0b3e2be8240cbd58404eb`  
		Last Modified: Sat, 03 Apr 2021 02:40:15 GMT  
		Size: 5.5 MB (5547325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2974076651535b81ed47daec0c9ac8a8a614de3b86c54d48a04c89ad19e07559`  
		Last Modified: Sat, 03 Apr 2021 02:40:13 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcd05d1e076faa0694af18a98a932e308a61016ec9d22d17a4a5d09ee624c5b`  
		Last Modified: Sat, 03 Apr 2021 02:43:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa1e95a491e1011c05bd5d893107c47f4bf45b9d273494616573b09db4a24ff`  
		Last Modified: Mon, 12 Apr 2021 19:05:48 GMT  
		Size: 104.4 MB (104372912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ff6e26da947927b44192b6354522593f1f6d60a2b2923599c528da51496d59`  
		Last Modified: Mon, 12 Apr 2021 19:05:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:80418768e2a25913814f1f428ef29aa89f80b36a4dd4f7d8b692472ece9cebba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134679220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4417d97545006d4c8028e52546f6bf13f73e62ec186dbd954ba469434de970d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 03 Apr 2021 04:10:04 GMT
ADD file:5a9b188c70f1f07ae9d68f3eb7aa18a1683faf50d5ff20eda1b04db3255877b9 in / 
# Sat, 03 Apr 2021 04:10:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 04:10:11 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 04:10:13 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 04:10:14 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 06:25:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 06:26:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 06:26:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 03 Apr 2021 06:35:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 03 Apr 2021 06:35:56 GMT
ENV LANG=C.UTF-8
# Sat, 03 Apr 2021 06:35:57 GMT
ENV LC_ALL=C.UTF-8
# Sat, 03 Apr 2021 06:41:20 GMT
ENV ROS_DISTRO=rolling
# Mon, 12 Apr 2021 18:37:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 12 Apr 2021 18:37:30 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Mon, 12 Apr 2021 18:37:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 12 Apr 2021 18:37:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2b20d1a80822f7dbd2175f235caa068029e82a265d0924d4f4d39c1bf9dc7f9b`  
		Last Modified: Thu, 01 Apr 2021 08:25:41 GMT  
		Size: 27.2 MB (27176807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e993c4ee9ad2dd0f069e7c34bbf137c835c5a2c2cc3f111e37fba05c79c1d7`  
		Last Modified: Sat, 03 Apr 2021 04:11:51 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2befefc5146bc156f83e891873a69526513f1e942e3d2bf68129f1e2fa17613`  
		Last Modified: Sat, 03 Apr 2021 04:11:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b425e160ecdc1ce2e8f2c9394df0bf787e591ab7983fa386fa029ed26a92c1`  
		Last Modified: Sat, 03 Apr 2021 06:48:05 GMT  
		Size: 1.2 MB (1183308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19dbee98155e4cab1ca612d6d81cf3e8713fb2f87fc42d92530e2635fd1ba8f`  
		Last Modified: Sat, 03 Apr 2021 06:48:04 GMT  
		Size: 5.5 MB (5513345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874fc4821a261dd3d76266f77f06518b341b2bea50a79bd0dbc4fd367823c520`  
		Last Modified: Sat, 03 Apr 2021 06:48:03 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c452bc5faf1f1e451a20172334f340dd4489b450beb68b361113cbb662c759`  
		Last Modified: Sat, 03 Apr 2021 06:52:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0ab3c512753b244538a8ab37fab37708be74125f14fd61ffbe824570feacef`  
		Last Modified: Mon, 12 Apr 2021 18:43:19 GMT  
		Size: 100.8 MB (100802871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff110debec88d4efc22b471c583e4d003b48447246d2b20184c57cb87516c98`  
		Last Modified: Mon, 12 Apr 2021 18:42:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

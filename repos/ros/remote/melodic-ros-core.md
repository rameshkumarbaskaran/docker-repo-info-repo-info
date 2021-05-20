## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:6a4f62ca13b7d2db437fe06471e7b053fbfd80c5639bb93c903857c93e2a2b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:b86016700133750bb5277e97aaee1062496639ccafa02625016bf2e0cbf8bbc4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291837350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edad2de99c6a4f745980c0c51a241d9a200d421170b496f602a5785e9b29bc8e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:35:57 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:49:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:49:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 19 May 2021 21:49:30 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 19 May 2021 21:49:30 GMT
ENV LANG=C.UTF-8
# Wed, 19 May 2021 21:49:30 GMT
ENV LC_ALL=C.UTF-8
# Wed, 19 May 2021 21:49:30 GMT
ENV ROS_DISTRO=melodic
# Wed, 19 May 2021 21:53:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:53:11 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 19 May 2021 21:53:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 19 May 2021 21:53:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1270d8e5a641a61675efd742287bbc693c243ab17fd4886a7550878d186f2565`  
		Last Modified: Wed, 19 May 2021 22:11:29 GMT  
		Size: 841.4 KB (841350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8ca49cb51a84fa2a9f93d1c7107f0d2aef6eba8e6373200924e7ed48f92b25`  
		Last Modified: Wed, 19 May 2021 22:11:28 GMT  
		Size: 4.9 MB (4872908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16393a6ac7473d1c49944336fa197f4dd193e6738e769c9485c31fcb6912e55a`  
		Last Modified: Wed, 19 May 2021 22:11:27 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80c0dce95dfa514f52400e92207fd1d9212c4559045417362fd1fbb1cfd9959`  
		Last Modified: Wed, 19 May 2021 22:11:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c63b15b621280a1708465afda54dd4a65958c0137ec8468f7b65bcc56d930fe`  
		Last Modified: Wed, 19 May 2021 22:12:02 GMT  
		Size: 259.4 MB (259423911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53084d069511c20e45c9ee1b0bd1678c40f6879b3f43122c7fd127082e5964e3`  
		Last Modified: Wed, 19 May 2021 22:11:27 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:fa0f971221382d71b147ad10d0a4a580aa34220a9bf7a82093558d9c6ad721d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266155433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1377d06cdb9b9132b49ea1cb58a5958db46653ab68d809e73d1d196711c3b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 May 2021 20:21:52 GMT
ADD file:c990710d70105be91eebcea7dfdf28e2212d37ea9279eb2dfd0071e9ed2fd4f1 in / 
# Wed, 19 May 2021 20:21:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 20:21:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 20:22:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 20:22:00 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:45:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:45:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:45:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 19 May 2021 21:45:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 19 May 2021 21:45:42 GMT
ENV LANG=C.UTF-8
# Wed, 19 May 2021 21:45:42 GMT
ENV LC_ALL=C.UTF-8
# Wed, 19 May 2021 21:45:43 GMT
ENV ROS_DISTRO=melodic
# Wed, 19 May 2021 21:48:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:48:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 19 May 2021 21:48:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 19 May 2021 21:48:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c61ae1d5a3957b8a0838e053004a2ddf56e395d58ee3b63baa7b1c865a6383b9`  
		Last Modified: Wed, 19 May 2021 20:23:59 GMT  
		Size: 22.3 MB (22292007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ceff6e604f05b8d76ca10ab8fd06e21e9edb719c243d7a204cd6fd6321a0aa`  
		Last Modified: Wed, 19 May 2021 20:23:54 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5399193bfffbb95297aa486ca4b2fa0207207d9a9e4c53f6bfbbcb85c76a678`  
		Last Modified: Wed, 19 May 2021 20:23:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86a43f70e1d6fdccefdc57cc27f65edb46f0ceaecea8cfcf1d7ae1388cb9599`  
		Last Modified: Wed, 19 May 2021 22:09:20 GMT  
		Size: 841.1 KB (841122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965b3833e81b3c9899613a0e75def4ee1f02a378883e4ddfc26a1dd98aa86744`  
		Last Modified: Wed, 19 May 2021 22:09:19 GMT  
		Size: 4.1 MB (4085596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137bc13cb481399d36861c580a816a55f50ae993abf7a10cfeeda72fe4c5ff52`  
		Last Modified: Wed, 19 May 2021 22:09:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2da0f8cfe83fc2042e6a1608a64ac9a08f928eba02a2cfe9042c950d82ff3bd`  
		Last Modified: Wed, 19 May 2021 22:09:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7875a717241269d5286cd4745541bb34ad7ce39c16cb4095a4badb18e69510bc`  
		Last Modified: Wed, 19 May 2021 22:10:32 GMT  
		Size: 238.9 MB (238933827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f49385f95dd6f565e9f242959781bed0470ad0a7125c59f7f20750993f4c88d`  
		Last Modified: Wed, 19 May 2021 22:09:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:247acc2264be6a68aaf69b7e249230115f150063d3c3b98e3c42b9306689e10a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281330358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48e3a44d38d62523bdd85092362665077a9497d4de3bd070f3ca096ae9494e0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:47:15 GMT
ADD file:5f7cb4b44f843eaef6ae7ddb75dfc228a33d20cd974074ca23c1bb2cad7f77ad in / 
# Fri, 23 Apr 2021 22:47:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:47:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:47:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:47:24 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:23:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:23:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:23:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 24 Apr 2021 00:23:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 24 Apr 2021 00:23:46 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 00:23:47 GMT
ENV LC_ALL=C.UTF-8
# Sat, 24 Apr 2021 00:23:48 GMT
ENV ROS_DISTRO=melodic
# Sat, 24 Apr 2021 00:26:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:27:07 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 24 Apr 2021 00:27:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 24 Apr 2021 00:27:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:673aeee5c81c892477834e2b5e55575f16bfd52d9b841a1d8c524fb3805ee960`  
		Last Modified: Fri, 16 Apr 2021 16:25:11 GMT  
		Size: 23.7 MB (23703698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018b2790219d2003c0d437e634927887ee5cc3d8f985d7459adc5b2ff62d003f`  
		Last Modified: Fri, 23 Apr 2021 22:49:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509c77ce92ade89fbf09fe03b167023be51bf5a0c14c00487fa7a9ee33b55fc3`  
		Last Modified: Fri, 23 Apr 2021 22:49:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4d7949f503cfae35d1e4072cc9f714f7f8080ddc5b9c1a01a837bd00682493`  
		Last Modified: Sat, 24 Apr 2021 01:23:29 GMT  
		Size: 841.2 KB (841190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ffbacc392e75d546f657a3c5ccfb65077a82acaaf78fd4ee3e380b95ef811f`  
		Last Modified: Sat, 24 Apr 2021 01:23:26 GMT  
		Size: 4.5 MB (4453794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476ab02969bb3ddd3e04ec5657467e4e747f59f5e3e02c4af893ad380c8c6cfb`  
		Last Modified: Sat, 24 Apr 2021 01:23:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f27d4607596697345ce0405a6ce36d38a3f1eacd4efffdd67b6eee075298c4d`  
		Last Modified: Sat, 24 Apr 2021 01:23:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1400f4e9bf4ad77d4ec4f3e600f380ae67ed173f30586bcdbba70fe42c4038f1`  
		Last Modified: Sat, 24 Apr 2021 01:25:40 GMT  
		Size: 252.3 MB (252328798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bcb83d73f0b6752b4761e171477c587baafae5998cf39a98d63bb5be62ca37`  
		Last Modified: Sat, 24 Apr 2021 01:23:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:dashing-ros-core-bionic`

```console
$ docker pull ros@sha256:7998e8644a6bfe9194558d3ea85187c6f8d3a74d5751bfc7a12a4a6c7b2f22dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:6a458be70571f18d2f2e98a6ec117d62953eae441eb79451721b01ec3d1bc144
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211891119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b6059b46e67fa51d6425f315329121480b316e4e021ea1c5d5023045d62fd7`
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
# Wed, 19 May 2021 22:02:52 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 19 May 2021 22:02:53 GMT
ENV LANG=C.UTF-8
# Wed, 19 May 2021 22:02:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 19 May 2021 22:02:53 GMT
ENV ROS_DISTRO=dashing
# Wed, 19 May 2021 22:04:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 22:04:04 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 19 May 2021 22:04:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 19 May 2021 22:04:04 GMT
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
	-	`sha256:9af7786db6953ff9b0956663127b915dfd9785175f7c4ce5bac8ed4d3a42f8df`  
		Last Modified: Wed, 19 May 2021 22:14:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec365ca7e984d2ff7d826de9f5efc9702c243acab79e24fa5bbd1f5a6ea25fb`  
		Last Modified: Wed, 19 May 2021 22:14:40 GMT  
		Size: 179.5 MB (179477674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f783967af3598098ade1e69491938767a83726f3bd0e884f68493a1b0543995`  
		Last Modified: Wed, 19 May 2021 22:14:11 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:c63d436d166fae6797cd67104be092772c8d7e617875bb89fe15cc897a66da46
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180810378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e743df19e0cc6656ba9b4813ec8fda4ca67695220c271859a1966aac715d76`
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
# Wed, 19 May 2021 21:55:36 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 19 May 2021 21:55:37 GMT
ENV LANG=C.UTF-8
# Wed, 19 May 2021 21:55:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 19 May 2021 21:55:38 GMT
ENV ROS_DISTRO=dashing
# Wed, 19 May 2021 21:57:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:57:54 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 19 May 2021 21:57:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 19 May 2021 21:57:56 GMT
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
	-	`sha256:48fad5a9655b359e8b409167a2b0c389cc7a6f69fd2066bf75a6d8c1202e98d3`  
		Last Modified: Wed, 19 May 2021 22:12:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5b8ffc55f2b394ea94e1b84445901585c7540588af86343631e43f09973be0`  
		Last Modified: Wed, 19 May 2021 22:13:41 GMT  
		Size: 153.6 MB (153588768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299980aa2384569e5ac6a3cb79dbe037dea1922163648418872c7136aea1747c`  
		Last Modified: Wed, 19 May 2021 22:12:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:570a9f99d664a36a1bdbd6f4000b665615c45dbadaf7633a3dba348453675df3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 MB (194086287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6e04a23aa49f7eb7e110484953a76ad709ebd63ddb70baa27b814c60cf5f01`
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
# Sat, 24 Apr 2021 00:46:16 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 24 Apr 2021 00:46:17 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 00:46:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 24 Apr 2021 00:46:20 GMT
ENV ROS_DISTRO=dashing
# Sat, 24 Apr 2021 00:48:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:48:34 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 24 Apr 2021 00:48:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 24 Apr 2021 00:48:37 GMT
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
	-	`sha256:9a2ca8bca9319a705f62ad9a055c3c031669e45715063fe23a399dc70e087705`  
		Last Modified: Sat, 24 Apr 2021 01:34:06 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adf08fb5b90b52af6b256933f72b2da13942e3ade84fb585ea596819f75fdf2`  
		Last Modified: Sat, 24 Apr 2021 01:35:26 GMT  
		Size: 165.1 MB (165084725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77055f56a634a7319b39c0385893dbd785dc118c58eff975f1580d46b47bc19`  
		Last Modified: Sat, 24 Apr 2021 01:34:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

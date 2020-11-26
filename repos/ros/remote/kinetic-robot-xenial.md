## `ros:kinetic-robot-xenial`

```console
$ docker pull ros@sha256:3bf16ca0581c83f952ef19d82411a4a28d74eeae423bc24043fa25c60a3c7e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-robot-xenial` - linux; amd64

```console
$ docker pull ros@sha256:6e54582229ddcc57eb84153dfc02b2157418360a624b1ea3cd8ea4d5d3e3b189
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.0 MB (380972782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78e0bde2fc341eaeac30bd2a0809ff17e4cc8a6e1c962ffa5dff5d58b5f885d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:42:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:42:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 01:42:02 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 26 Nov 2020 01:42:02 GMT
ENV LANG=C.UTF-8
# Thu, 26 Nov 2020 01:42:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Nov 2020 01:42:02 GMT
ENV ROS_DISTRO=kinetic
# Thu, 26 Nov 2020 01:43:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:44:00 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 26 Nov 2020 01:44:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Nov 2020 01:44:00 GMT
CMD ["bash"]
# Thu, 26 Nov 2020 01:44:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:44:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 26 Nov 2020 01:45:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94cf6b01927532a24fecba2e88d5aa3e553f087fcf3b5de780ace06aaeca5a1`  
		Last Modified: Thu, 26 Nov 2020 02:26:19 GMT  
		Size: 5.4 MB (5362832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24686782e46b88375ad4ddd74396a1f29ccf5dd34d192a9724dcc476d4a77e3`  
		Last Modified: Thu, 26 Nov 2020 02:26:19 GMT  
		Size: 14.7 KB (14744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c37fb3954cf62deb7dd81f675735869a0bfb0b6f5821763a1591c9993e2f8a`  
		Last Modified: Thu, 26 Nov 2020 02:26:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6cd7524ada3336e2ca6610dead776b5982446e32d02bca2057be7a594c227b`  
		Last Modified: Thu, 26 Nov 2020 02:27:03 GMT  
		Size: 187.2 MB (187160759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79339e65150375f52bc82fc8585d2ff3cdad20ce09cf9a7b43fb374e1389a68`  
		Last Modified: Thu, 26 Nov 2020 02:26:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4b1997f7870278eab9254a04bf7c7e4aef578e84aa657fa472f8aba82e3274`  
		Last Modified: Thu, 26 Nov 2020 02:27:20 GMT  
		Size: 57.2 MB (57241289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510c2b9981f0432cdb311fe06615409c9d547109fff43992714f785752b59d53`  
		Last Modified: Thu, 26 Nov 2020 02:27:08 GMT  
		Size: 268.9 KB (268855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3811d0d7221d9b4e4d255788076cfacf0a250474a133f8dfb9d9e016e1edbea9`  
		Last Modified: Thu, 26 Nov 2020 02:27:23 GMT  
		Size: 63.6 MB (63577748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ae5f50db28bf6cab04eb89c32d38f8add7884c82da096720234378085a39b4`  
		Last Modified: Thu, 26 Nov 2020 02:27:33 GMT  
		Size: 21.5 MB (21506317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:ea285e58858d797c77360807606bd204c424c1fa7677cadd8d60026a8f1419e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331511249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf84dcb52e677bb21f8505f7f119bab0608194b0f4bdd5c30a8ad01fa94a0a63`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 25 Nov 2020 23:01:00 GMT
ADD file:0947a09b11d2a3286469b4ddf6d3d58881839b8c4377d343e475d0e66eef9b7d in / 
# Wed, 25 Nov 2020 23:01:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 23:01:07 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:01:10 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 23:01:12 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 00:01:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:01:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 00:01:55 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 26 Nov 2020 00:01:56 GMT
ENV LANG=C.UTF-8
# Thu, 26 Nov 2020 00:01:59 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Nov 2020 00:02:00 GMT
ENV ROS_DISTRO=kinetic
# Thu, 26 Nov 2020 00:04:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:04:49 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 26 Nov 2020 00:04:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Nov 2020 00:04:51 GMT
CMD ["bash"]
# Thu, 26 Nov 2020 00:05:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:05:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 26 Nov 2020 00:07:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:08:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9bc86a2fe0a9b47f715e84e5bd1286da57dd7a79808c3da3571e7545fbb90af7`  
		Last Modified: Mon, 02 Nov 2020 23:20:03 GMT  
		Size: 39.9 MB (39902208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adf0a70ddb4a67405dcca7eecf8c4f56d13faa0de2f12a5cdfc5ee63d72a681`  
		Last Modified: Wed, 25 Nov 2020 23:02:40 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5475b6908bf78ed05b18766116eaeb7fbce1ffeee65c72b2f7bfdf420097cf6`  
		Last Modified: Wed, 25 Nov 2020 23:02:39 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed78ff2520e3b2a6193c0dccf58ab7b2adcb9bd51165f163021650e823ab0a3`  
		Last Modified: Wed, 25 Nov 2020 23:02:39 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8d7167c262fee184b690ddaaaa36f74accf49367d841ec614677e386671cab`  
		Last Modified: Thu, 26 Nov 2020 01:06:33 GMT  
		Size: 4.6 MB (4615075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ae19f7a2781c0f4501007baa969545ec9a431cd9a42edb067ceb5609cf8fed`  
		Last Modified: Thu, 26 Nov 2020 01:06:31 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad72b5255dcd2bd45b8fb55efb9527cfc69329e8e7467c9c1d9e000d7706801`  
		Last Modified: Thu, 26 Nov 2020 01:06:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81d94c0bb6a7b5c6ee98ed32b19d7e66ac343a326e28029377ac8cd6c2954b6`  
		Last Modified: Thu, 26 Nov 2020 01:07:31 GMT  
		Size: 168.1 MB (168052966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb2ba32400064d1c993d9cb1298e0b1ab4336f1dc86962ab4563f48de01ec7f`  
		Last Modified: Thu, 26 Nov 2020 01:06:31 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa280c4eb10e8d699199b4336dad187219d59c5f7ef44455a7faba6aee862949`  
		Last Modified: Thu, 26 Nov 2020 01:08:00 GMT  
		Size: 42.9 MB (42892583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc052190a86d8804cae67f64c16f18130556e5efc6565c96a1377c7121b563f3`  
		Last Modified: Thu, 26 Nov 2020 01:07:40 GMT  
		Size: 269.0 KB (268958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd96cd1f3a28fff7b34af7b9b69724991babc1fbb28431b168f6f9c6046067a`  
		Last Modified: Thu, 26 Nov 2020 01:07:58 GMT  
		Size: 55.5 MB (55504255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339585caa0d54759038906e204ab65b011e779e941c900c0ae7fc28638f8f0df`  
		Last Modified: Thu, 26 Nov 2020 01:08:15 GMT  
		Size: 20.3 MB (20258498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c7e14db1961168d0776074c321ec17a09ef36d7dd95b01efb60177ed379d23a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345728985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28722d806562dba47f8694537f9c9f29e561495c1857ec074c16a7b53296a261`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:44:18 GMT
ADD file:a360b1e1db1ae9973dac11dfe4e549f6416e278f53c42eb5e98b3b3da8d2a5ae in / 
# Wed, 25 Nov 2020 22:44:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:44:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:44:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:44:26 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:49:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:49:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 25 Nov 2020 23:49:34 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 25 Nov 2020 23:49:35 GMT
ENV LANG=C.UTF-8
# Wed, 25 Nov 2020 23:49:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 25 Nov 2020 23:49:37 GMT
ENV ROS_DISTRO=kinetic
# Wed, 25 Nov 2020 23:52:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:52:43 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 25 Nov 2020 23:52:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 25 Nov 2020 23:52:45 GMT
CMD ["bash"]
# Wed, 25 Nov 2020 23:53:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:53:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 25 Nov 2020 23:54:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:55:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e30c5e4609ac16f9e19faa3800699e28c77aadcfcbde2ddd5954606f80fa170`  
		Last Modified: Sat, 31 Oct 2020 00:25:13 GMT  
		Size: 40.8 MB (40826105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be82da0c7e998c509a8e86338f139501b62fde0df3908dd489a8249380ea3441`  
		Last Modified: Wed, 25 Nov 2020 22:45:42 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf04dffef88e5257b2388d643e5fb03a812316de0737ce92e3888a6722cea5e`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624f7934929e6e67f81a9becb317179367648ec1236d644e9bf3a00d3fe3772`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fcd8c88b81ce1d2014f2eb69aaab1bc6a43960f2bb541599f95364f321154dc`  
		Last Modified: Thu, 26 Nov 2020 01:03:54 GMT  
		Size: 4.8 MB (4820331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8577196a9ddabebca148188e299af2498816d078cb0216b79df969f5667f260`  
		Last Modified: Thu, 26 Nov 2020 01:03:53 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ba2ccc0d2f632b253e7332accd9d84f2ed32f50a82134983f585bf9e7dbc05`  
		Last Modified: Thu, 26 Nov 2020 01:03:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3a269cf6a9c0ba408a1f77dac4e7568b1f7017c6ed6a0ad2ae23f74801a6c6`  
		Last Modified: Thu, 26 Nov 2020 01:04:45 GMT  
		Size: 176.0 MB (176025998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca44a362de8e65b18999bc0b7b13fa0fe54b2c5b6cb4e9c042f555a46fb50b18`  
		Last Modified: Thu, 26 Nov 2020 01:03:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6ed45fc6b0d4222cae599c87c4993ee9e8a2e9423239ad253ad23a7e45f89f`  
		Last Modified: Thu, 26 Nov 2020 01:05:07 GMT  
		Size: 46.0 MB (45953476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a8b665df2168cbe4bc65dbb617c06b38dc04bfd2fa668933eb0c8455e6a261`  
		Last Modified: Thu, 26 Nov 2020 01:04:55 GMT  
		Size: 268.9 KB (268918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c5ef18da559def44f4cb7b0151a5a1d95888450beaaabe8a15a9331cf6e9db`  
		Last Modified: Thu, 26 Nov 2020 01:05:10 GMT  
		Size: 57.3 MB (57298744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7912dd0b411a060d1a91cdf0e8daf2c27ccc3a7531c4148385a565b3c1bba2f`  
		Last Modified: Thu, 26 Nov 2020 01:05:29 GMT  
		Size: 20.5 MB (20518755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

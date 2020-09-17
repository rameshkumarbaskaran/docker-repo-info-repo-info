## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:2c8eae543bc085096c8587bccfa83e0b39068b5c5b49f6a56c249a808751bbe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:8296664d213f388dea64492052d066e8c7afacad062a09bac2a03739a085c680
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154655462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e498d99f0620b2a52de2f71cb3f274625e4795ac2a23ad9c9d12abae54bf6090`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:23 GMT
ADD file:1b4ec50586b9f0621095f51ee6baecc00a7f6d95b4a04e3bedc5393b28bc8a54 in / 
# Wed, 16 Sep 2020 22:20:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:25 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:37:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:34:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:34:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 01:55:03 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 17 Sep 2020 01:55:03 GMT
ENV LANG=C.UTF-8
# Thu, 17 Sep 2020 01:55:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Sep 2020 01:55:03 GMT
ENV ROS_DISTRO=foxy
# Thu, 17 Sep 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:56:36 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 17 Sep 2020 01:56:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Sep 2020 01:56:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e6ca3592b14484be6a9719617680e0c810e0107d89c437162c75d2401637c72c`  
		Last Modified: Wed, 16 Sep 2020 15:19:59 GMT  
		Size: 28.6 MB (28557166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534a5505201da9ddb334b5b2fcb3cec45fcafccd8e91b93ad4852e1a1bb318c1`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 839.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990916bd23bbbf9c30d202dad557e813562d028f3076bf57904830c69d4cde83`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd43f844b454143fefb276b0d47a08c31858e330ffeceef21130f4f907c2691e`  
		Last Modified: Thu, 17 Sep 2020 00:52:12 GMT  
		Size: 1.2 MB (1176444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25929632fd5b65202802f96157aaae95b55bcb587a77c708a4d63e5d2100db09`  
		Last Modified: Thu, 17 Sep 2020 02:08:15 GMT  
		Size: 5.5 MB (5547001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa5e6421658a99911cb295c7f31b4f12e6a3f61860c7814b87cddc1a985e215`  
		Last Modified: Thu, 17 Sep 2020 02:08:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b62c6d955edf0b3d12ec0e851b2c8e6901c44cc4798da5c77c35bef01209da`  
		Last Modified: Thu, 17 Sep 2020 02:14:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2b66304789e3439a1a20d7b92034ea5374768eaf73ae3e04753c003723f421`  
		Last Modified: Thu, 17 Sep 2020 02:15:26 GMT  
		Size: 119.4 MB (119372008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8699c1a075cf2f62a951eeceb18b4ce20fda71db84ea44010eb43b048e05395`  
		Last Modified: Thu, 17 Sep 2020 02:14:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:38c31cebaa6115f11cdb97dff9b03367db888926e40bec7b86b8d9e4d2e2903d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137446600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad554c70a9c60bc06b630bc50bbdc8571f9f38523cb4015193c7d8ec03bcb8ec`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Sep 2020 23:16:56 GMT
ADD file:063d9d9577619d2eeb19bbc784fecf567039a314d8f741500841f6b4f3c847b3 in / 
# Wed, 16 Sep 2020 23:17:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 23:17:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 23:17:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 23:17:04 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 01:44:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:44:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:45:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 02:13:08 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 17 Sep 2020 02:13:08 GMT
ENV LANG=C.UTF-8
# Thu, 17 Sep 2020 02:13:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Sep 2020 02:13:10 GMT
ENV ROS_DISTRO=foxy
# Thu, 17 Sep 2020 02:14:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:15:08 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 17 Sep 2020 02:15:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Sep 2020 02:15:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:33c9bf8777b52e6bc989f3a77a8a680861b9a7f7385e2d5ee02fdede89acf606`  
		Last Modified: Wed, 16 Sep 2020 08:25:33 GMT  
		Size: 27.2 MB (27158462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1900e162114f589f3e78ba5b26957f2b6ec38c8aaa6efdd8afbfaf5d9e8841`  
		Last Modified: Wed, 16 Sep 2020 23:18:40 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53c8a81c25472b52dd428e136c84a1f407ce933911cab5910676d1a7b7a4df3`  
		Last Modified: Wed, 16 Sep 2020 23:18:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694ddde6856911f795c55f1e3e7d0658aa1d457594dbf63fd18f6cbc10fd0658`  
		Last Modified: Thu, 17 Sep 2020 02:36:11 GMT  
		Size: 1.2 MB (1177642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3c413801c3e32051187650ead158523b1424776c96e4f3d3410b393309dc4`  
		Last Modified: Thu, 17 Sep 2020 02:36:03 GMT  
		Size: 5.5 MB (5513389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe76cc3db355f14c9557f875c35c68fbbd7d00a458bbc2ab91a3dd10ae61464b`  
		Last Modified: Thu, 17 Sep 2020 02:36:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd035db57351467e95400554c075d902030a7049744862ceb593f9fe9f3d4eed`  
		Last Modified: Thu, 17 Sep 2020 02:49:17 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6486f66e843c2d0fa9f8b67886198175a38db9b12b600c24419d605194ceaec4`  
		Last Modified: Thu, 17 Sep 2020 02:50:31 GMT  
		Size: 103.6 MB (103594229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d38132067b4812cb0aeae56852e8f528befce4d1a0303b9c6557e85c4559df`  
		Last Modified: Thu, 17 Sep 2020 02:49:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

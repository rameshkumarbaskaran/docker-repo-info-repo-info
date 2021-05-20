## `ros:kinetic-robot`

```console
$ docker pull ros@sha256:212ffaa0094abb3a803b0cc99923a4dfebadeb98cec6231b2ef218a09b80e946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:82d48aad891af810d59a8f4af6379bd470560a13777eb7dcdde6890b59d3b719
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386563619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d0ebd6f1ec59bcef29d0f48875f2096119090eff72f267cad26d75684d9fd3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:39:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:39:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 19 May 2021 21:39:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 19 May 2021 21:39:28 GMT
ENV LANG=C.UTF-8
# Wed, 19 May 2021 21:39:28 GMT
ENV LC_ALL=C.UTF-8
# Wed, 19 May 2021 21:39:28 GMT
ENV ROS_DISTRO=kinetic
# Wed, 19 May 2021 21:42:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:42:17 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 19 May 2021 21:42:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 19 May 2021 21:42:17 GMT
CMD ["bash"]
# Wed, 19 May 2021 21:42:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:42:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 19 May 2021 21:43:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:44:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14684ba412c39757a989fb7fe7e1858ffaecf276e3190ccd4765dabe7a1e8b11`  
		Last Modified: Wed, 19 May 2021 22:09:00 GMT  
		Size: 5.4 MB (5364316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d57d18c871aa3698dca1c280246f6e78f80e39a8c306763750d9fdce93efff`  
		Last Modified: Wed, 19 May 2021 22:09:00 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea861d8af8441bf794d8e6e8770d22b11cec75699560edff78932dce34e29a83`  
		Last Modified: Wed, 19 May 2021 22:08:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39413ca8ec49abf567b8c4497755073cb268ea3568fbe548b86f454849e3566d`  
		Last Modified: Wed, 19 May 2021 22:09:30 GMT  
		Size: 192.1 MB (192075126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3d8fde9915f7333a8aa902f390231c5576b7f801aff8f872367f5531572170`  
		Last Modified: Wed, 19 May 2021 22:08:59 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da38743f7f0589daee248db97589a070b938c027b9759bcc15c4106da225b0c1`  
		Last Modified: Wed, 19 May 2021 22:09:50 GMT  
		Size: 57.3 MB (57252738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7e211bc1889df4ae714743757913cf5a0224dcbf36913330f42e26e09a904a`  
		Last Modified: Wed, 19 May 2021 22:09:41 GMT  
		Size: 291.4 KB (291407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cb1b82e308266626f8151c9d9590de87e82cfc2e423fade7cab95840290d76`  
		Last Modified: Wed, 19 May 2021 22:09:52 GMT  
		Size: 63.6 MB (63577704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda506da9f33e3aec35a7062b4b0864f9707bb54b6b167f06a3781a5cf9759f3`  
		Last Modified: Wed, 19 May 2021 22:10:10 GMT  
		Size: 21.5 MB (21523838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:9ee311d72b1c39bf1ada942c81a1face645e919ae959812a0de1652672f264df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.9 MB (335877644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2c2ae257d6438f9e4b4e6ec510204f268561d67b62cf649aad41e2ccdc28a2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 May 2021 20:23:21 GMT
ADD file:7e5c1f0262200ed290a61913d7f2c3b2b064c9b02aa1a55a818e38ab1316bbda in / 
# Wed, 19 May 2021 20:23:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 20:23:26 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 20:23:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 20:23:29 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:36:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 19 May 2021 21:36:30 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 19 May 2021 21:36:31 GMT
ENV LANG=C.UTF-8
# Wed, 19 May 2021 21:36:31 GMT
ENV LC_ALL=C.UTF-8
# Wed, 19 May 2021 21:36:32 GMT
ENV ROS_DISTRO=kinetic
# Wed, 19 May 2021 21:39:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:39:19 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 19 May 2021 21:39:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 19 May 2021 21:39:21 GMT
CMD ["bash"]
# Wed, 19 May 2021 21:40:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:40:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 19 May 2021 21:41:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:42:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ae1370da0037e05eb3f24cd486c49ee3a450840763c7d31deef8274cb9abfd86`  
		Last Modified: Wed, 19 May 2021 20:24:51 GMT  
		Size: 40.3 MB (40292258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452bc1820a9d9923cac2a73df110a9ad72318825a2ff4807ed5e89708052cea5`  
		Last Modified: Wed, 19 May 2021 20:24:39 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1217aa77f4015a99b17bec638b9f07cdf319ff342015b6c42800a588797d54a7`  
		Last Modified: Wed, 19 May 2021 20:24:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f84e209d76ee2a0ef7c673bb433398f6e5765eed483d8f68f8015126a1d3ce5`  
		Last Modified: Wed, 19 May 2021 20:24:39 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164c3db7dcdcac754553ea86686fcc95bc07e7392fadeb3f99c2aea178bf935`  
		Last Modified: Wed, 19 May 2021 22:06:02 GMT  
		Size: 4.6 MB (4615806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7409c8424ff6b9fd94d5c415d3bddc1cb64174188a06d52977835626b7a9b902`  
		Last Modified: Wed, 19 May 2021 22:06:01 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2eeece880ab5bbe4d3baa5a29cb7352f6f99279cb45e963d343a787558af2da`  
		Last Modified: Wed, 19 May 2021 22:06:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5e692414d21de96856c9d60746bf0f9ea5af6b23d768a9cde0363da4af0a52`  
		Last Modified: Wed, 19 May 2021 22:06:58 GMT  
		Size: 172.0 MB (171978318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce8569c046903740bbd689c1855b3ea7ce1c0cd821e645ccf46ef7fb65595f3`  
		Last Modified: Wed, 19 May 2021 22:06:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0849801ba980926a0098c28410f630ad85b05bb3267131df46fc466aae33326b`  
		Last Modified: Wed, 19 May 2021 22:07:17 GMT  
		Size: 42.9 MB (42897783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e60c17feee27e380d9a846e99f4c2788fb8f0e117891ee90172463844684ed1`  
		Last Modified: Wed, 19 May 2021 22:07:05 GMT  
		Size: 291.4 KB (291435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792b56a7140aec33ae47878ddd79e07b63a2f436ec7f4b44439426dacc7b93c6`  
		Last Modified: Wed, 19 May 2021 22:07:22 GMT  
		Size: 55.5 MB (55505757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a8d3193d2859519c562da008ac7484e1771e41d1580818aa0ef067ddc15d39`  
		Last Modified: Wed, 19 May 2021 22:07:37 GMT  
		Size: 20.3 MB (20279588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2e75416d05414cbac158a1b43f815dae02dc2a9af97d4e04d1daf6acaf718444
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.9 MB (345942899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5453577db089496612fb35e139957c89dddc5557b88ca20ecdff4ddf681d0de`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:49:13 GMT
ADD file:f7933af6e4e3a52794ae852310c5fd423b1afeb32576f8e3c3bc695db17d34e4 in / 
# Fri, 23 Apr 2021 22:49:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:49:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:49:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:49:24 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:13:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:13:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 24 Apr 2021 00:13:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 24 Apr 2021 00:13:29 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 00:13:30 GMT
ENV LC_ALL=C.UTF-8
# Sat, 24 Apr 2021 00:13:31 GMT
ENV ROS_DISTRO=kinetic
# Sat, 24 Apr 2021 00:16:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:16:17 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 24 Apr 2021 00:16:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 24 Apr 2021 00:16:20 GMT
CMD ["bash"]
# Sat, 24 Apr 2021 00:17:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:17:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 24 Apr 2021 00:18:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:19:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea68ed57e24afe569fc149143e2b3c46c597abcbb61449c3652998e4bb1b5440`  
		Last Modified: Sat, 17 Apr 2021 00:25:08 GMT  
		Size: 41.0 MB (41026756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12a5b59372be005e03800813e52c56f42f21410e07162424afb9662a5620f7c`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d46388e3f6c8bd0bdd7d2079370426b00565c4fffac3f138c26af2408de2`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af45b45bb6a5e3119ffb671a33eb4a934675de944eee38f1aba43f3967c533`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef091df1ad3b49c777e51fcbdbef24b7a792d400584b31ffd16e771e1c09d7c9`  
		Last Modified: Sat, 24 Apr 2021 01:17:48 GMT  
		Size: 4.8 MB (4820634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dce1815ff82daa6b03af2100a095b9a5c3e2dfbd30442adfbe66a06ee9df5e5`  
		Last Modified: Sat, 24 Apr 2021 01:17:45 GMT  
		Size: 14.7 KB (14749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442c97bda99730a3a0034634612cfb5a799e8ccb1666e3f834a87699b974ec6c`  
		Last Modified: Sat, 24 Apr 2021 01:17:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf5408c0eb281fed7aa611c1331b0f4151887b838d7c45baa1657da2029aaaa`  
		Last Modified: Sat, 24 Apr 2021 01:19:33 GMT  
		Size: 176.0 MB (176021723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88cff5bdb08e16f518885da7949f063f4bdeb59f313bcb790922e7a60899df6`  
		Last Modified: Sat, 24 Apr 2021 01:17:45 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227e3d5739d14ea70647c8f71a41062e3538d6353b8f0a2efc88df369bdcc49b`  
		Last Modified: Sat, 24 Apr 2021 01:20:02 GMT  
		Size: 46.0 MB (45953079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be931fbac577bd32681c67f33ac30f6f43f8e773306787d5ad5195af28017d2`  
		Last Modified: Sat, 24 Apr 2021 01:19:43 GMT  
		Size: 280.2 KB (280211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e0f2ef7eabb94ba855a03a7217873d5eff015bd51b5297c05c4c3e1fc82cbb`  
		Last Modified: Sat, 24 Apr 2021 01:20:09 GMT  
		Size: 57.3 MB (57297623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f90af7701137c7100d35bcdc4da1dccf43bfb85d39e416f535ac7473a43b511`  
		Last Modified: Sat, 24 Apr 2021 01:20:33 GMT  
		Size: 20.5 MB (20526212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

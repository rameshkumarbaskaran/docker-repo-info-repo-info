<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.2.2`](#r-base422)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.2.2`

```console
$ docker pull r-base@sha256:8887ec4c0d3f13925b9b039d462d6e8a67ddbd14a30eef9e8d60e5b9f35a4aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `r-base:4.2.2` - linux; amd64

```console
$ docker pull r-base@sha256:94ba89c4503af7c69dca11e855c24f30af8e21c43399d664a68ef8ae05a9f5a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.1 MB (347114704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de1ef2039fbd2fcbaf609da402d6b2a94fee892755cc7bb074fa26b8738ce0b`
-	Default Command: `["R"]`

```dockerfile
# Tue, 25 Oct 2022 01:45:19 GMT
ADD file:7b3c3912d73330bfbb6eb18f8cba6491e0c4b2be59bc6b846a4a0cde39b1ad27 in / 
# Tue, 25 Oct 2022 01:45:19 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:31:53 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 01 Nov 2022 20:20:27 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& adduser docker staff
# Tue, 01 Nov 2022 20:20:41 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Nov 2022 20:20:44 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 01 Nov 2022 20:20:44 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 01 Nov 2022 20:20:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Nov 2022 20:20:44 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 01 Nov 2022 20:20:45 GMT
ENV R_BASE_VERSION=4.2.2
# Tue, 01 Nov 2022 20:22:02 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Nov 2022 20:22:04 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ebbe46658ae1eddd748e3222cbc9dd7109f9fd7f279a4b2f9d6a32d0a58b4c16`  
		Last Modified: Tue, 25 Oct 2022 01:50:50 GMT  
		Size: 51.3 MB (51261759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8780930e7e7b18116589a863916682a85c45bec3c738dab17f8740830988b5`  
		Last Modified: Tue, 01 Nov 2022 20:22:25 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f11b798771daf119baa7f2f3d5b9c4363b0aec5d12e488fbb2e07a0cf0be79`  
		Last Modified: Tue, 01 Nov 2022 20:22:28 GMT  
		Size: 31.3 MB (31262096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced6bc7d0fb644dbcbeecc374d4904ae5df8f303707c30aa60514e3d929fd644`  
		Last Modified: Tue, 01 Nov 2022 20:22:25 GMT  
		Size: 865.8 KB (865843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e2154a522a29fd10fe63922ee826f4d42e1e474ad08bc2f8c71e811e7f0127`  
		Last Modified: Tue, 01 Nov 2022 20:22:25 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a417257f633cd58de6c3b59ec8c55c5bb04296fa387da3daa9cc1cba037116`  
		Last Modified: Tue, 01 Nov 2022 20:22:56 GMT  
		Size: 263.7 MB (263723342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.2.2` - linux; ppc64le

```console
$ docker pull r-base@sha256:00c5f4bd44a731ea9e54c15551de11320873ea0514c92075ec51dee2e69d229d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349276445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f65a8f46aff0802e727d707c91f6c8cf3ca514e45ec7964683c029cabe817b9`
-	Default Command: `["R"]`

```dockerfile
# Tue, 25 Oct 2022 03:15:17 GMT
ADD file:eb3294b440b1de7e5e420328a146136657392ed0568fcc54a574e171e31558a1 in / 
# Tue, 25 Oct 2022 03:15:20 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:22:11 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 01 Nov 2022 20:16:58 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& adduser docker staff
# Tue, 01 Nov 2022 20:17:27 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Nov 2022 20:17:31 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 01 Nov 2022 20:17:31 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 01 Nov 2022 20:17:32 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Nov 2022 20:17:33 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 01 Nov 2022 20:17:33 GMT
ENV R_BASE_VERSION=4.2.2
# Tue, 01 Nov 2022 20:19:49 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Nov 2022 20:19:56 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e78937113e3c6d6902831ab5c7cb1ac7b54dd956b0a882adb2b81160f0cd0833`  
		Last Modified: Tue, 25 Oct 2022 03:21:41 GMT  
		Size: 55.3 MB (55338729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5679eb3d089f0e8d73f918282d14a084a9a9cbbca09b815338bc0f6dd45f5af`  
		Last Modified: Tue, 01 Nov 2022 20:20:14 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bd54906b11b2c0da1d2a093a48fb9c4d28579887eb80c9d8efcae81c0b4400`  
		Last Modified: Tue, 01 Nov 2022 20:20:21 GMT  
		Size: 32.5 MB (32513844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ad140f98059823bf264e52df961c09c3eaf48d985d6c30021cb745a6f44858`  
		Last Modified: Tue, 01 Nov 2022 20:20:15 GMT  
		Size: 865.8 KB (865845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f557e8c51657e421ddb6d1b40d1bffa7fb99c5a637e7ac73226e92cd3c6b0e77`  
		Last Modified: Tue, 01 Nov 2022 20:20:14 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c1a2e0d7266eb6822feaefc1a3583b2950dcbe8d440e4c87b77961d816e795`  
		Last Modified: Tue, 01 Nov 2022 20:21:09 GMT  
		Size: 260.6 MB (260556361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:04ceeaa4c20b61f42804419a946f0351b84aa325e0d15f39ab19bba1f4d2a0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:94ba89c4503af7c69dca11e855c24f30af8e21c43399d664a68ef8ae05a9f5a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.1 MB (347114704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de1ef2039fbd2fcbaf609da402d6b2a94fee892755cc7bb074fa26b8738ce0b`
-	Default Command: `["R"]`

```dockerfile
# Tue, 25 Oct 2022 01:45:19 GMT
ADD file:7b3c3912d73330bfbb6eb18f8cba6491e0c4b2be59bc6b846a4a0cde39b1ad27 in / 
# Tue, 25 Oct 2022 01:45:19 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:31:53 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 01 Nov 2022 20:20:27 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& adduser docker staff
# Tue, 01 Nov 2022 20:20:41 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Nov 2022 20:20:44 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 01 Nov 2022 20:20:44 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 01 Nov 2022 20:20:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Nov 2022 20:20:44 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 01 Nov 2022 20:20:45 GMT
ENV R_BASE_VERSION=4.2.2
# Tue, 01 Nov 2022 20:22:02 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Nov 2022 20:22:04 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ebbe46658ae1eddd748e3222cbc9dd7109f9fd7f279a4b2f9d6a32d0a58b4c16`  
		Last Modified: Tue, 25 Oct 2022 01:50:50 GMT  
		Size: 51.3 MB (51261759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8780930e7e7b18116589a863916682a85c45bec3c738dab17f8740830988b5`  
		Last Modified: Tue, 01 Nov 2022 20:22:25 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f11b798771daf119baa7f2f3d5b9c4363b0aec5d12e488fbb2e07a0cf0be79`  
		Last Modified: Tue, 01 Nov 2022 20:22:28 GMT  
		Size: 31.3 MB (31262096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced6bc7d0fb644dbcbeecc374d4904ae5df8f303707c30aa60514e3d929fd644`  
		Last Modified: Tue, 01 Nov 2022 20:22:25 GMT  
		Size: 865.8 KB (865843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e2154a522a29fd10fe63922ee826f4d42e1e474ad08bc2f8c71e811e7f0127`  
		Last Modified: Tue, 01 Nov 2022 20:22:25 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a417257f633cd58de6c3b59ec8c55c5bb04296fa387da3daa9cc1cba037116`  
		Last Modified: Tue, 01 Nov 2022 20:22:56 GMT  
		Size: 263.7 MB (263723342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:73b2225b46c24a9946810e3806d517f1ea56efed7dd96e6950fe37164a8a75f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329563928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbcf7f59685085aa8a9b00e89a1f4ddee6213db929743e5d3eff1e7da29ad7bf`
-	Default Command: `["R"]`

```dockerfile
# Tue, 12 Jul 2022 00:42:26 GMT
ADD file:52b0a411bbddbc5a40d2288e5189606bd2fb03bdba9ab2dfa0b29ee90195a43b in / 
# Tue, 12 Jul 2022 00:42:26 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 12:56:21 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 12 Jul 2022 12:56:22 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 12 Jul 2022 12:56:33 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:56:35 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 12 Jul 2022 12:56:36 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 12 Jul 2022 12:56:37 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Jul 2022 12:56:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 12 Jul 2022 12:56:39 GMT
ENV R_BASE_VERSION=4.2.1
# Tue, 12 Jul 2022 12:57:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:57:39 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:370af700e1ed84d7809745357ae1357e57448bf6e682ad1ff1a41f20c19fe232`  
		Last Modified: Tue, 12 Jul 2022 00:49:31 GMT  
		Size: 52.1 MB (52128630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e0503232cefb48c17cd3ec0bf77b8af8d657c40fe798a76613a1e006bc782c`  
		Last Modified: Tue, 12 Jul 2022 12:57:55 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311e48a7138a5ae6011c273a586f7c769f0d7af33668ce2e5a796ba2c722b73d`  
		Last Modified: Tue, 12 Jul 2022 12:57:58 GMT  
		Size: 28.9 MB (28927889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7efd61bb74bd6091d62d90398ce43ec0b82958e7dc7415e7d0b2b58b323649a`  
		Last Modified: Tue, 12 Jul 2022 12:57:55 GMT  
		Size: 864.6 KB (864612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e3bf773dc950db2099b5feda63d9ba2aacad7d39afb3ef3e43ab14ecb4ee54`  
		Last Modified: Tue, 12 Jul 2022 12:57:54 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ce92fcfcd656f3277ed2137f5689b99f35d54cc449cd2da4707eb8b8a1a773`  
		Last Modified: Tue, 12 Jul 2022 12:58:23 GMT  
		Size: 247.6 MB (247640621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:00c5f4bd44a731ea9e54c15551de11320873ea0514c92075ec51dee2e69d229d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349276445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f65a8f46aff0802e727d707c91f6c8cf3ca514e45ec7964683c029cabe817b9`
-	Default Command: `["R"]`

```dockerfile
# Tue, 25 Oct 2022 03:15:17 GMT
ADD file:eb3294b440b1de7e5e420328a146136657392ed0568fcc54a574e171e31558a1 in / 
# Tue, 25 Oct 2022 03:15:20 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:22:11 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 01 Nov 2022 20:16:58 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& adduser docker staff
# Tue, 01 Nov 2022 20:17:27 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Nov 2022 20:17:31 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 01 Nov 2022 20:17:31 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 01 Nov 2022 20:17:32 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Nov 2022 20:17:33 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 01 Nov 2022 20:17:33 GMT
ENV R_BASE_VERSION=4.2.2
# Tue, 01 Nov 2022 20:19:49 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Nov 2022 20:19:56 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e78937113e3c6d6902831ab5c7cb1ac7b54dd956b0a882adb2b81160f0cd0833`  
		Last Modified: Tue, 25 Oct 2022 03:21:41 GMT  
		Size: 55.3 MB (55338729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5679eb3d089f0e8d73f918282d14a084a9a9cbbca09b815338bc0f6dd45f5af`  
		Last Modified: Tue, 01 Nov 2022 20:20:14 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bd54906b11b2c0da1d2a093a48fb9c4d28579887eb80c9d8efcae81c0b4400`  
		Last Modified: Tue, 01 Nov 2022 20:20:21 GMT  
		Size: 32.5 MB (32513844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ad140f98059823bf264e52df961c09c3eaf48d985d6c30021cb745a6f44858`  
		Last Modified: Tue, 01 Nov 2022 20:20:15 GMT  
		Size: 865.8 KB (865845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f557e8c51657e421ddb6d1b40d1bffa7fb99c5a637e7ac73226e92cd3c6b0e77`  
		Last Modified: Tue, 01 Nov 2022 20:20:14 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c1a2e0d7266eb6822feaefc1a3583b2950dcbe8d440e4c87b77961d816e795`  
		Last Modified: Tue, 01 Nov 2022 20:21:09 GMT  
		Size: 260.6 MB (260556361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:19ce5a4259f37ec86afb53b9bbe0df42ad3de8f115655b235bf8907026bed753
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304654790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e013ac029b70301a95c97f975841cf2f3ccc9026c956c701122eab96aade9706`
-	Default Command: `["R"]`

```dockerfile
# Tue, 12 Jul 2022 00:48:02 GMT
ADD file:d73eeeaa444d7c8255cd2ca31c00a952231237fc5487b1e6772c5f70cafd440a in / 
# Tue, 12 Jul 2022 00:48:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 15:57:02 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 12 Jul 2022 15:57:04 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 12 Jul 2022 15:57:24 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 15:57:31 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 12 Jul 2022 15:57:32 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 12 Jul 2022 15:57:32 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Jul 2022 15:57:34 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 12 Jul 2022 15:57:34 GMT
ENV R_BASE_VERSION=4.2.1
# Tue, 12 Jul 2022 15:58:51 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 15:59:11 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:80dbf564ccdb8d822debfb926a7eaccbc64bd2365e4541f63e07fdf1295dd5f1`  
		Last Modified: Tue, 12 Jul 2022 00:56:09 GMT  
		Size: 51.6 MB (51554124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4f9750ccdde4a2eee8fe83af10652df4b4e09aa5d167ffce19965fc601d91a`  
		Last Modified: Tue, 12 Jul 2022 15:59:30 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e44adcd44a265a413e928872bdb2af58b6c4b5212d6ef80afd8a5cb6241855f`  
		Last Modified: Tue, 12 Jul 2022 15:59:33 GMT  
		Size: 28.8 MB (28777403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76be77f169060dfb6600e29050f687a74147ef1392433d2527787dab1e83ce3`  
		Last Modified: Tue, 12 Jul 2022 15:59:30 GMT  
		Size: 920.2 KB (920187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d9c9251f1adcf26b6675d65bce6a035fdb4db50f40ba49be2e83b9e3c66200`  
		Last Modified: Tue, 12 Jul 2022 15:59:30 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544d937d2544e701d2c38ec4ae49f357a4fd0822ddb66c13d0d486101188dc7b`  
		Last Modified: Tue, 12 Jul 2022 15:59:53 GMT  
		Size: 223.4 MB (223400849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

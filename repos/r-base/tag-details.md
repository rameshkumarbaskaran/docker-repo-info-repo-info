<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.2.0`](#r-base420)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.2.0`

```console
$ docker pull r-base@sha256:59b849d7103807b9d3985f0e4daeafa3ab309777059bb19fff3058db001dcc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.2.0` - linux; amd64

```console
$ docker pull r-base@sha256:42c5988e209690d334d3d0117bbabd932a33106f726603642a8612b584de8644
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338995163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ef3904a475479319438e3051acda0df03e8cf21e55c01158db9ff45cf6c09c`
-	Default Command: `["R"]`

```dockerfile
# Wed, 11 May 2022 01:22:25 GMT
ADD file:281fd73718c53fc59c1102594f7f1e885886403980fd1b7ca7f5c96a97f4332b in / 
# Wed, 11 May 2022 01:22:25 GMT
CMD ["bash"]
# Wed, 11 May 2022 09:19:40 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 11 May 2022 09:19:41 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 11 May 2022 09:19:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 09:19:52 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 11 May 2022 09:19:52 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 11 May 2022 09:19:52 GMT
ENV LANG=en_US.UTF-8
# Wed, 11 May 2022 09:19:53 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 11 May 2022 09:19:53 GMT
ENV R_BASE_VERSION=4.2.0
# Wed, 11 May 2022 09:20:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 09:20:40 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bb3baf4f16d6f037d735d8dffacf29da8066f489b61bffeceeda9f6403aadeb6`  
		Last Modified: Wed, 11 May 2022 01:29:18 GMT  
		Size: 52.9 MB (52944486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2111bbc5433eca944ee5c72112d8dd0af3c8b58166cf253c4a5962277136738`  
		Last Modified: Wed, 11 May 2022 09:20:56 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6451c42a423dde0eed7dc0aa6fff44f13861522677fb4850d30f098c833e0634`  
		Last Modified: Wed, 11 May 2022 09:21:00 GMT  
		Size: 27.8 MB (27800969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3824ae840517ec001011ec0e868cbc8d2cd8ba5457a6bb4e903cab3b2c7468`  
		Last Modified: Wed, 11 May 2022 09:20:57 GMT  
		Size: 864.6 KB (864611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee0c53da2944e8e539b17a8a8c6c970799212392a92aef659a948f7c5914f21`  
		Last Modified: Wed, 11 May 2022 09:20:56 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f757280e14ccf7c5dd0a7420b3783aafb1f68f1e5571f27681dbd743c7e6731a`  
		Last Modified: Wed, 11 May 2022 09:21:26 GMT  
		Size: 257.4 MB (257382871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.2.0` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:36f7035f4161f786a8ae9d2b3b98dd0f8288f19933cf5ea2d0e502613bb13d9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327853136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5d684fc95bac273700dd892beab84bee25e1349af4b29e5e8b13688a29600d`
-	Default Command: `["R"]`

```dockerfile
# Sat, 28 May 2022 00:43:11 GMT
ADD file:936ad327dc97009e77bbb7d1d1874d55f3d251b8a641269356e5caabe860a8cf in / 
# Sat, 28 May 2022 00:43:12 GMT
CMD ["bash"]
# Sat, 28 May 2022 09:18:04 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sat, 28 May 2022 09:18:05 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Sat, 28 May 2022 09:18:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:18:22 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 28 May 2022 09:18:23 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 28 May 2022 09:18:24 GMT
ENV LANG=en_US.UTF-8
# Sat, 28 May 2022 09:18:25 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Sat, 28 May 2022 09:18:26 GMT
ENV R_BASE_VERSION=4.2.0
# Sat, 28 May 2022 09:19:27 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:19:28 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:75fd77c03641c04273179a599ef54dea600d22da8b30160003b50fa90a397f43`  
		Last Modified: Sat, 28 May 2022 00:52:12 GMT  
		Size: 52.0 MB (52042837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33d38e7acd282b4f4c9cb92b6f028dd29443682ba6a66cda3282159201230a3`  
		Last Modified: Sat, 28 May 2022 09:19:55 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ccff95214eb6a1eefdca7f10b2a4eb330f587eb1042778a324ce55ace4aa50`  
		Last Modified: Sat, 28 May 2022 09:19:58 GMT  
		Size: 27.6 MB (27648798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a5fba3f3d5a304ab34e1bc9b8f8fd02ec2e56ead25afdb420cf4b5832cee8e`  
		Last Modified: Sat, 28 May 2022 09:19:55 GMT  
		Size: 864.6 KB (864615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01843724a21b04fc6e35add1bc074c7befaad8cd29e62c5954140bf0492e04ab`  
		Last Modified: Sat, 28 May 2022 09:19:55 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d030a8569b5e70d4a0c25825e58f54e8ea04281f4e882af204790359dbee32`  
		Last Modified: Sat, 28 May 2022 09:20:23 GMT  
		Size: 247.3 MB (247294709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.2.0` - linux; ppc64le

```console
$ docker pull r-base@sha256:d266c044dd0f202c934c2bc142cb9f79ea8cef5be99a4f8e01dbcaab22e88d3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.0 MB (338005034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2d9d80cfbcca22786705d63f7a61951e1e522d26391403457475ac30240bbb`
-	Default Command: `["R"]`

```dockerfile
# Wed, 11 May 2022 01:36:50 GMT
ADD file:8824d2629598c6f5c70db2488623b2873dd8496f2765f9a16b931e62ebe1d2ca in / 
# Wed, 11 May 2022 01:36:58 GMT
CMD ["bash"]
# Wed, 11 May 2022 14:08:04 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 11 May 2022 14:08:17 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 11 May 2022 14:09:57 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:10:07 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 11 May 2022 14:10:12 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 11 May 2022 14:10:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 11 May 2022 14:10:22 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 11 May 2022 14:10:26 GMT
ENV R_BASE_VERSION=4.2.0
# Wed, 11 May 2022 14:16:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:16:53 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f847dd78355ff75879dd0f1ed43325b24a1351e2cb0038f2cf60d5e061b5b866`  
		Last Modified: Wed, 11 May 2022 01:46:57 GMT  
		Size: 57.2 MB (57150570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b12b755287361006c0528870d3b56ef447c99483b78d29f9f27f5363578bcae`  
		Last Modified: Wed, 11 May 2022 14:17:22 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab95c5ea7c946a7f5fec117da0e8b1b44c13cbfabe434e074368791be39e18`  
		Last Modified: Wed, 11 May 2022 14:17:26 GMT  
		Size: 28.1 MB (28116508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cbf74157feaae7eccad2e1bed24736b304ca1226ab3d655e05a6d3d3d01d4d`  
		Last Modified: Wed, 11 May 2022 14:17:23 GMT  
		Size: 864.6 KB (864616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bd0c005890cf6815eb421cec6728504e3b018800cfc617117994810c1dd42b`  
		Last Modified: Wed, 11 May 2022 14:17:22 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ea9d64f7741d05c0855435f54474042e8c7a19fa4c22ee11ac13afd8768663`  
		Last Modified: Wed, 11 May 2022 14:18:00 GMT  
		Size: 251.9 MB (251871101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.2.0` - linux; s390x

```console
$ docker pull r-base@sha256:ad911df2fb08e45bb78edaa2b5132acfb3c29a561f920de30f09509218117bbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303172603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009a7af67a6581ac856d7b45ed7a6d339166e7e49f0931e734b15128359c4d72`
-	Default Command: `["R"]`

```dockerfile
# Sat, 28 May 2022 00:45:48 GMT
ADD file:430aae00218790907570f298b5f5c4e47453d9297090e8d006c5169e5e9ee56f in / 
# Sat, 28 May 2022 00:45:52 GMT
CMD ["bash"]
# Sat, 28 May 2022 14:09:44 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sat, 28 May 2022 14:09:47 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Sat, 28 May 2022 14:10:16 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 14:10:22 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 28 May 2022 14:10:23 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 28 May 2022 14:10:23 GMT
ENV LANG=en_US.UTF-8
# Sat, 28 May 2022 14:10:25 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Sat, 28 May 2022 14:10:25 GMT
ENV R_BASE_VERSION=4.2.0
# Sat, 28 May 2022 14:12:29 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 14:12:55 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:33ada038def02ed9f3f9762c43feeaf3a66329f979154e6d3dca5e1ac4f04893`  
		Last Modified: Sat, 28 May 2022 00:51:52 GMT  
		Size: 51.5 MB (51490267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40a861a5b04c2f9889f2481238dada12e05ef5844db1f03ea5de352d22e3de3`  
		Last Modified: Sat, 28 May 2022 14:13:14 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fed479b3faef6d091cca289e8173d1a92762ec6a1768240402b5807e63bd73`  
		Last Modified: Sat, 28 May 2022 14:13:17 GMT  
		Size: 27.5 MB (27505490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14758b183e8702560c5dce06f1b61d392a37f125018ffc195e752540236143cc`  
		Last Modified: Sat, 28 May 2022 14:13:14 GMT  
		Size: 920.2 KB (920190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1038de2e612076d08cd18dc92b28c954cfb3f1b144a68cb80632b4127c1077d3`  
		Last Modified: Sat, 28 May 2022 14:13:14 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0e8d52a9bc82a685f859ebb220b2279417a7e47ccbb4acbaec63e528c7a869`  
		Last Modified: Sat, 28 May 2022 14:13:36 GMT  
		Size: 223.3 MB (223254421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:59b849d7103807b9d3985f0e4daeafa3ab309777059bb19fff3058db001dcc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:42c5988e209690d334d3d0117bbabd932a33106f726603642a8612b584de8644
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338995163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ef3904a475479319438e3051acda0df03e8cf21e55c01158db9ff45cf6c09c`
-	Default Command: `["R"]`

```dockerfile
# Wed, 11 May 2022 01:22:25 GMT
ADD file:281fd73718c53fc59c1102594f7f1e885886403980fd1b7ca7f5c96a97f4332b in / 
# Wed, 11 May 2022 01:22:25 GMT
CMD ["bash"]
# Wed, 11 May 2022 09:19:40 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 11 May 2022 09:19:41 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 11 May 2022 09:19:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 09:19:52 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 11 May 2022 09:19:52 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 11 May 2022 09:19:52 GMT
ENV LANG=en_US.UTF-8
# Wed, 11 May 2022 09:19:53 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 11 May 2022 09:19:53 GMT
ENV R_BASE_VERSION=4.2.0
# Wed, 11 May 2022 09:20:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 09:20:40 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bb3baf4f16d6f037d735d8dffacf29da8066f489b61bffeceeda9f6403aadeb6`  
		Last Modified: Wed, 11 May 2022 01:29:18 GMT  
		Size: 52.9 MB (52944486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2111bbc5433eca944ee5c72112d8dd0af3c8b58166cf253c4a5962277136738`  
		Last Modified: Wed, 11 May 2022 09:20:56 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6451c42a423dde0eed7dc0aa6fff44f13861522677fb4850d30f098c833e0634`  
		Last Modified: Wed, 11 May 2022 09:21:00 GMT  
		Size: 27.8 MB (27800969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3824ae840517ec001011ec0e868cbc8d2cd8ba5457a6bb4e903cab3b2c7468`  
		Last Modified: Wed, 11 May 2022 09:20:57 GMT  
		Size: 864.6 KB (864611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee0c53da2944e8e539b17a8a8c6c970799212392a92aef659a948f7c5914f21`  
		Last Modified: Wed, 11 May 2022 09:20:56 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f757280e14ccf7c5dd0a7420b3783aafb1f68f1e5571f27681dbd743c7e6731a`  
		Last Modified: Wed, 11 May 2022 09:21:26 GMT  
		Size: 257.4 MB (257382871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:36f7035f4161f786a8ae9d2b3b98dd0f8288f19933cf5ea2d0e502613bb13d9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327853136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5d684fc95bac273700dd892beab84bee25e1349af4b29e5e8b13688a29600d`
-	Default Command: `["R"]`

```dockerfile
# Sat, 28 May 2022 00:43:11 GMT
ADD file:936ad327dc97009e77bbb7d1d1874d55f3d251b8a641269356e5caabe860a8cf in / 
# Sat, 28 May 2022 00:43:12 GMT
CMD ["bash"]
# Sat, 28 May 2022 09:18:04 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sat, 28 May 2022 09:18:05 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Sat, 28 May 2022 09:18:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:18:22 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 28 May 2022 09:18:23 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 28 May 2022 09:18:24 GMT
ENV LANG=en_US.UTF-8
# Sat, 28 May 2022 09:18:25 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Sat, 28 May 2022 09:18:26 GMT
ENV R_BASE_VERSION=4.2.0
# Sat, 28 May 2022 09:19:27 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:19:28 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:75fd77c03641c04273179a599ef54dea600d22da8b30160003b50fa90a397f43`  
		Last Modified: Sat, 28 May 2022 00:52:12 GMT  
		Size: 52.0 MB (52042837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33d38e7acd282b4f4c9cb92b6f028dd29443682ba6a66cda3282159201230a3`  
		Last Modified: Sat, 28 May 2022 09:19:55 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ccff95214eb6a1eefdca7f10b2a4eb330f587eb1042778a324ce55ace4aa50`  
		Last Modified: Sat, 28 May 2022 09:19:58 GMT  
		Size: 27.6 MB (27648798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a5fba3f3d5a304ab34e1bc9b8f8fd02ec2e56ead25afdb420cf4b5832cee8e`  
		Last Modified: Sat, 28 May 2022 09:19:55 GMT  
		Size: 864.6 KB (864615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01843724a21b04fc6e35add1bc074c7befaad8cd29e62c5954140bf0492e04ab`  
		Last Modified: Sat, 28 May 2022 09:19:55 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d030a8569b5e70d4a0c25825e58f54e8ea04281f4e882af204790359dbee32`  
		Last Modified: Sat, 28 May 2022 09:20:23 GMT  
		Size: 247.3 MB (247294709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:d266c044dd0f202c934c2bc142cb9f79ea8cef5be99a4f8e01dbcaab22e88d3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.0 MB (338005034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2d9d80cfbcca22786705d63f7a61951e1e522d26391403457475ac30240bbb`
-	Default Command: `["R"]`

```dockerfile
# Wed, 11 May 2022 01:36:50 GMT
ADD file:8824d2629598c6f5c70db2488623b2873dd8496f2765f9a16b931e62ebe1d2ca in / 
# Wed, 11 May 2022 01:36:58 GMT
CMD ["bash"]
# Wed, 11 May 2022 14:08:04 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 11 May 2022 14:08:17 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 11 May 2022 14:09:57 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:10:07 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 11 May 2022 14:10:12 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 11 May 2022 14:10:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 11 May 2022 14:10:22 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 11 May 2022 14:10:26 GMT
ENV R_BASE_VERSION=4.2.0
# Wed, 11 May 2022 14:16:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:16:53 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f847dd78355ff75879dd0f1ed43325b24a1351e2cb0038f2cf60d5e061b5b866`  
		Last Modified: Wed, 11 May 2022 01:46:57 GMT  
		Size: 57.2 MB (57150570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b12b755287361006c0528870d3b56ef447c99483b78d29f9f27f5363578bcae`  
		Last Modified: Wed, 11 May 2022 14:17:22 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab95c5ea7c946a7f5fec117da0e8b1b44c13cbfabe434e074368791be39e18`  
		Last Modified: Wed, 11 May 2022 14:17:26 GMT  
		Size: 28.1 MB (28116508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cbf74157feaae7eccad2e1bed24736b304ca1226ab3d655e05a6d3d3d01d4d`  
		Last Modified: Wed, 11 May 2022 14:17:23 GMT  
		Size: 864.6 KB (864616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bd0c005890cf6815eb421cec6728504e3b018800cfc617117994810c1dd42b`  
		Last Modified: Wed, 11 May 2022 14:17:22 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ea9d64f7741d05c0855435f54474042e8c7a19fa4c22ee11ac13afd8768663`  
		Last Modified: Wed, 11 May 2022 14:18:00 GMT  
		Size: 251.9 MB (251871101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:ad911df2fb08e45bb78edaa2b5132acfb3c29a561f920de30f09509218117bbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303172603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009a7af67a6581ac856d7b45ed7a6d339166e7e49f0931e734b15128359c4d72`
-	Default Command: `["R"]`

```dockerfile
# Sat, 28 May 2022 00:45:48 GMT
ADD file:430aae00218790907570f298b5f5c4e47453d9297090e8d006c5169e5e9ee56f in / 
# Sat, 28 May 2022 00:45:52 GMT
CMD ["bash"]
# Sat, 28 May 2022 14:09:44 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sat, 28 May 2022 14:09:47 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Sat, 28 May 2022 14:10:16 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 14:10:22 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 28 May 2022 14:10:23 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 28 May 2022 14:10:23 GMT
ENV LANG=en_US.UTF-8
# Sat, 28 May 2022 14:10:25 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Sat, 28 May 2022 14:10:25 GMT
ENV R_BASE_VERSION=4.2.0
# Sat, 28 May 2022 14:12:29 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 14:12:55 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:33ada038def02ed9f3f9762c43feeaf3a66329f979154e6d3dca5e1ac4f04893`  
		Last Modified: Sat, 28 May 2022 00:51:52 GMT  
		Size: 51.5 MB (51490267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40a861a5b04c2f9889f2481238dada12e05ef5844db1f03ea5de352d22e3de3`  
		Last Modified: Sat, 28 May 2022 14:13:14 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fed479b3faef6d091cca289e8173d1a92762ec6a1768240402b5807e63bd73`  
		Last Modified: Sat, 28 May 2022 14:13:17 GMT  
		Size: 27.5 MB (27505490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14758b183e8702560c5dce06f1b61d392a37f125018ffc195e752540236143cc`  
		Last Modified: Sat, 28 May 2022 14:13:14 GMT  
		Size: 920.2 KB (920190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1038de2e612076d08cd18dc92b28c954cfb3f1b144a68cb80632b4127c1077d3`  
		Last Modified: Sat, 28 May 2022 14:13:14 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0e8d52a9bc82a685f859ebb220b2279417a7e47ccbb4acbaec63e528c7a869`  
		Last Modified: Sat, 28 May 2022 14:13:36 GMT  
		Size: 223.3 MB (223254421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

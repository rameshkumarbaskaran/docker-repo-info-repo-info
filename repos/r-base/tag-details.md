<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.2.3`](#r-base423)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.2.3`

```console
$ docker pull r-base@sha256:367f92974af1f708671351a6749af8c6b9715256276fb88f48a3814a982aacd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.2.3` - linux; amd64

```console
$ docker pull r-base@sha256:c79844fdc8bfcd92d4557fadcae3712259baabcc70433b98a5befcdb057003da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338196915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9051ce66400b983d100f7aba3c2fff73e59822728d32945f61f0a1a4bc747`
-	Default Command: `["R"]`

```dockerfile
# Wed, 01 Mar 2023 04:11:42 GMT
ADD file:74681cecd762b2ba7998f4db71254724112eeeb0a1801289e92e9be9986fab3e in / 
# Wed, 01 Mar 2023 04:11:43 GMT
CMD ["bash"]
# Wed, 15 Mar 2023 23:07:39 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 15 Mar 2023 23:07:40 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 15 Mar 2023 23:07:53 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 15 Mar 2023 23:07:55 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 15 Mar 2023 23:07:55 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 15 Mar 2023 23:07:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Mar 2023 23:07:56 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 15 Mar 2023 23:07:56 GMT
ENV R_BASE_VERSION=4.2.3
# Wed, 15 Mar 2023 23:07:56 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Wed, 15 Mar 2023 23:09:49 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 15 Mar 2023 23:09:51 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bbf0dc8a79b520e97bfc1897d4020969033cda033c141208013b60015a6334e5`  
		Last Modified: Wed, 01 Mar 2023 04:16:58 GMT  
		Size: 49.2 MB (49237268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bc0f45ebb23c8eb4010742705a54946ee078f9a2cb4c820cc59fbf11591ceb`  
		Last Modified: Wed, 15 Mar 2023 23:10:10 GMT  
		Size: 3.4 KB (3365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a774c8a7797545685aeaffbd3942dbb68558ff4bc8b2fa188fc76d9fd2d3d62`  
		Last Modified: Wed, 15 Mar 2023 23:10:15 GMT  
		Size: 25.1 MB (25111955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9041e14cd651d64159da5dc34102d1fbbbb1ffb18cb50f9060c1755241593ab`  
		Last Modified: Wed, 15 Mar 2023 23:10:08 GMT  
		Size: 865.9 KB (865852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b90e55cf6c065a8f00ec8bb5ed42f7d2be8eaa0593d9cbb66fc4004ac5809a`  
		Last Modified: Wed, 15 Mar 2023 23:10:08 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8146bb0258390a77b9bcf31ed59d9de0ab0221b66dd2029ef3e1d6274e8836a`  
		Last Modified: Wed, 15 Mar 2023 23:10:08 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbaea0691e6fb2570baf94bd3f77c5ddf9e47bacf2551b42daa9de35a1a5951`  
		Last Modified: Wed, 15 Mar 2023 23:10:39 GMT  
		Size: 263.0 MB (262977829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.2.3` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:6a394e4e2663159b36a5931d23a4abd0fe8fa2667f4389fda09242d144796b8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321610915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b86c7ad3d89cec4878a64a0a612bfd199ff3cc5f06b440305fc4a862ee981a`
-	Default Command: `["R"]`

```dockerfile
# Thu, 23 Mar 2023 00:46:10 GMT
ADD file:659cb8b541c9a906fe60747ea4b6ec72bb4e3525e53ed5e749127f0d9cb21a15 in / 
# Thu, 23 Mar 2023 00:46:11 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:10:08 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 23 Mar 2023 06:10:09 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 23 Mar 2023 06:10:22 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:10:24 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 23 Mar 2023 06:10:24 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 23 Mar 2023 06:10:24 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Mar 2023 06:10:25 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 23 Mar 2023 06:10:25 GMT
ENV R_BASE_VERSION=4.2.3
# Thu, 23 Mar 2023 06:10:25 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Thu, 23 Mar 2023 06:12:19 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:12:23 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e8c9f32eb3a01effeef152afae1272c7a3054f6070bca27f29886acb89e6b19b`  
		Last Modified: Thu, 23 Mar 2023 00:50:32 GMT  
		Size: 49.3 MB (49328258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400c9bc51053750a398519b87fda1fc4782636f9a17b8256ea9f975426a5832b`  
		Last Modified: Thu, 23 Mar 2023 06:12:37 GMT  
		Size: 3.4 KB (3361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d91570e7beecddb8c4e45b35bf81b0f91919f5999aa67b2410697c1501c56f`  
		Last Modified: Thu, 23 Mar 2023 06:12:38 GMT  
		Size: 24.9 MB (24943783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e412b4a8bd48a317a1a9d887a9f38a8e059fc1f77fd62fca43c9a3064ff0c6d`  
		Last Modified: Thu, 23 Mar 2023 06:12:36 GMT  
		Size: 865.9 KB (865852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbeb20f6a7a3d5501dcb2f22676d1a1881706b036b57b1b7fcf93c088f87ad4`  
		Last Modified: Thu, 23 Mar 2023 06:12:35 GMT  
		Size: 347.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f661049c6a25a29eec4fb85919cf17873b8a6a6a5bdcf8f6714949674d584c`  
		Last Modified: Thu, 23 Mar 2023 06:12:35 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efa7d293b586eafb0cf2ab5c7e9450e208dcb303f6bd6fc4ad56ee5560dc586`  
		Last Modified: Thu, 23 Mar 2023 06:12:56 GMT  
		Size: 246.5 MB (246469021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.2.3` - linux; ppc64le

```console
$ docker pull r-base@sha256:5bbba68a87fde58385c91321cc39b88138378f3d55e4d350c04366470464355c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340890392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82694c6cb1cf9d8dda0357e098bc13ef5a648b0f6aaf51792f8f56b78932598f`
-	Default Command: `["R"]`

```dockerfile
# Wed, 01 Mar 2023 04:49:21 GMT
ADD file:802564bd8f691b73ccc068cc3c339c6a4c178bcf8383008e4f87a3774cb308b9 in / 
# Wed, 01 Mar 2023 04:49:24 GMT
CMD ["bash"]
# Wed, 15 Mar 2023 22:34:41 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 15 Mar 2023 22:34:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 15 Mar 2023 22:35:12 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 15 Mar 2023 22:35:17 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 15 Mar 2023 22:35:18 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 15 Mar 2023 22:35:19 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Mar 2023 22:35:21 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 15 Mar 2023 22:35:22 GMT
ENV R_BASE_VERSION=4.2.3
# Wed, 15 Mar 2023 22:35:23 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Wed, 15 Mar 2023 22:39:13 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 15 Mar 2023 22:39:16 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:adcb4bfc20e2eddc047aac97edc102514767c0f2b64f4f281f2e71651d1a97a9`  
		Last Modified: Wed, 01 Mar 2023 04:56:03 GMT  
		Size: 53.3 MB (53250177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedfba3727b0e2481a72b4c5aaa6a213881ba512ff6a1d028af1e8b3f81dfc30`  
		Last Modified: Wed, 15 Mar 2023 22:39:30 GMT  
		Size: 3.4 KB (3368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb5fcec2a4c12bb7a3877120fbcbd43e02d93c579b4ec23a7c0e3c24d034fc1`  
		Last Modified: Wed, 15 Mar 2023 22:39:33 GMT  
		Size: 25.5 MB (25513339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96945dc0c5c32df80886b134ea7800be68cdb966b65a2bc3082c7ab0e155c3f8`  
		Last Modified: Wed, 15 Mar 2023 22:39:29 GMT  
		Size: 865.9 KB (865853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ade3cdc38a2299b70a9d6872515835e21db995a3e780b27e520208c7fc83d0`  
		Last Modified: Wed, 15 Mar 2023 22:39:28 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530812c100b22df2c2bbe4d721158af28a0dc4bc9713f90be312024ed5adf3ae`  
		Last Modified: Wed, 15 Mar 2023 22:39:28 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1f24e1acd62e26949c7606c065ef3e61fb4117829f8b9cccbeedef4fad83c7`  
		Last Modified: Wed, 15 Mar 2023 22:40:21 GMT  
		Size: 261.3 MB (261257009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.2.3` - linux; s390x

```console
$ docker pull r-base@sha256:52e8693051a20a597ee32b15e92010aec71ddd23f9155d2fc8179e366a90c87e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296708416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6c245f70a07cae74bce941333cae7299361d25fb7565b5d6af2ffa3e71ba12`
-	Default Command: `["R"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:12 GMT
ADD file:a96b8cacbcadb2068e0368c020589f4d2eae9fabb0965b387d5d9fc94831a1a5 in / 
# Thu, 23 Mar 2023 00:45:16 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 10:51:36 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 23 Mar 2023 10:51:37 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 23 Mar 2023 10:51:46 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:51:48 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 23 Mar 2023 10:51:48 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 23 Mar 2023 10:51:48 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Mar 2023 10:51:49 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 23 Mar 2023 10:51:49 GMT
ENV R_BASE_VERSION=4.2.3
# Thu, 23 Mar 2023 10:51:50 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Thu, 23 Mar 2023 10:52:53 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:53:04 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:57560ce693355ef04b6283597b61cd71f7e8b7d7357b218eab0c8979bce7812e`  
		Last Modified: Thu, 23 Mar 2023 00:48:17 GMT  
		Size: 47.7 MB (47671021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80793af67a69232cadace34e10b9ef46d1ba6f3755a4614ccbfb7a911f055a9`  
		Last Modified: Thu, 23 Mar 2023 10:53:16 GMT  
		Size: 3.4 KB (3357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399fe0d57620fc4b657bb26fc130a45cf377513e271deb6fa7b2430a78ed54e3`  
		Last Modified: Thu, 23 Mar 2023 10:53:17 GMT  
		Size: 24.8 MB (24801489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4f7d7095b671f7050cb36cce96b79401ba687ff33672f032f5bddf44ecab9b`  
		Last Modified: Thu, 23 Mar 2023 10:53:15 GMT  
		Size: 921.0 KB (921009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4593aadb093cfdef343d4697cdbe74987731c5b65b563859b94321451ccda65`  
		Last Modified: Thu, 23 Mar 2023 10:53:15 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3069e7378cf84ce8edecd9a388442fd79d6a305de51d312c72859f4a652685`  
		Last Modified: Thu, 23 Mar 2023 10:53:15 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b341b8c60321724abfbc967e97de155e9a198bb86c525745b76bc63085e26bfd`  
		Last Modified: Thu, 23 Mar 2023 10:53:39 GMT  
		Size: 223.3 MB (223310900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:367f92974af1f708671351a6749af8c6b9715256276fb88f48a3814a982aacd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:c79844fdc8bfcd92d4557fadcae3712259baabcc70433b98a5befcdb057003da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338196915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9051ce66400b983d100f7aba3c2fff73e59822728d32945f61f0a1a4bc747`
-	Default Command: `["R"]`

```dockerfile
# Wed, 01 Mar 2023 04:11:42 GMT
ADD file:74681cecd762b2ba7998f4db71254724112eeeb0a1801289e92e9be9986fab3e in / 
# Wed, 01 Mar 2023 04:11:43 GMT
CMD ["bash"]
# Wed, 15 Mar 2023 23:07:39 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 15 Mar 2023 23:07:40 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 15 Mar 2023 23:07:53 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 15 Mar 2023 23:07:55 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 15 Mar 2023 23:07:55 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 15 Mar 2023 23:07:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Mar 2023 23:07:56 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 15 Mar 2023 23:07:56 GMT
ENV R_BASE_VERSION=4.2.3
# Wed, 15 Mar 2023 23:07:56 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Wed, 15 Mar 2023 23:09:49 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 15 Mar 2023 23:09:51 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bbf0dc8a79b520e97bfc1897d4020969033cda033c141208013b60015a6334e5`  
		Last Modified: Wed, 01 Mar 2023 04:16:58 GMT  
		Size: 49.2 MB (49237268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bc0f45ebb23c8eb4010742705a54946ee078f9a2cb4c820cc59fbf11591ceb`  
		Last Modified: Wed, 15 Mar 2023 23:10:10 GMT  
		Size: 3.4 KB (3365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a774c8a7797545685aeaffbd3942dbb68558ff4bc8b2fa188fc76d9fd2d3d62`  
		Last Modified: Wed, 15 Mar 2023 23:10:15 GMT  
		Size: 25.1 MB (25111955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9041e14cd651d64159da5dc34102d1fbbbb1ffb18cb50f9060c1755241593ab`  
		Last Modified: Wed, 15 Mar 2023 23:10:08 GMT  
		Size: 865.9 KB (865852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b90e55cf6c065a8f00ec8bb5ed42f7d2be8eaa0593d9cbb66fc4004ac5809a`  
		Last Modified: Wed, 15 Mar 2023 23:10:08 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8146bb0258390a77b9bcf31ed59d9de0ab0221b66dd2029ef3e1d6274e8836a`  
		Last Modified: Wed, 15 Mar 2023 23:10:08 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbaea0691e6fb2570baf94bd3f77c5ddf9e47bacf2551b42daa9de35a1a5951`  
		Last Modified: Wed, 15 Mar 2023 23:10:39 GMT  
		Size: 263.0 MB (262977829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:6a394e4e2663159b36a5931d23a4abd0fe8fa2667f4389fda09242d144796b8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321610915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b86c7ad3d89cec4878a64a0a612bfd199ff3cc5f06b440305fc4a862ee981a`
-	Default Command: `["R"]`

```dockerfile
# Thu, 23 Mar 2023 00:46:10 GMT
ADD file:659cb8b541c9a906fe60747ea4b6ec72bb4e3525e53ed5e749127f0d9cb21a15 in / 
# Thu, 23 Mar 2023 00:46:11 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:10:08 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 23 Mar 2023 06:10:09 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 23 Mar 2023 06:10:22 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:10:24 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 23 Mar 2023 06:10:24 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 23 Mar 2023 06:10:24 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Mar 2023 06:10:25 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 23 Mar 2023 06:10:25 GMT
ENV R_BASE_VERSION=4.2.3
# Thu, 23 Mar 2023 06:10:25 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Thu, 23 Mar 2023 06:12:19 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:12:23 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e8c9f32eb3a01effeef152afae1272c7a3054f6070bca27f29886acb89e6b19b`  
		Last Modified: Thu, 23 Mar 2023 00:50:32 GMT  
		Size: 49.3 MB (49328258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400c9bc51053750a398519b87fda1fc4782636f9a17b8256ea9f975426a5832b`  
		Last Modified: Thu, 23 Mar 2023 06:12:37 GMT  
		Size: 3.4 KB (3361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d91570e7beecddb8c4e45b35bf81b0f91919f5999aa67b2410697c1501c56f`  
		Last Modified: Thu, 23 Mar 2023 06:12:38 GMT  
		Size: 24.9 MB (24943783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e412b4a8bd48a317a1a9d887a9f38a8e059fc1f77fd62fca43c9a3064ff0c6d`  
		Last Modified: Thu, 23 Mar 2023 06:12:36 GMT  
		Size: 865.9 KB (865852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbeb20f6a7a3d5501dcb2f22676d1a1881706b036b57b1b7fcf93c088f87ad4`  
		Last Modified: Thu, 23 Mar 2023 06:12:35 GMT  
		Size: 347.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f661049c6a25a29eec4fb85919cf17873b8a6a6a5bdcf8f6714949674d584c`  
		Last Modified: Thu, 23 Mar 2023 06:12:35 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efa7d293b586eafb0cf2ab5c7e9450e208dcb303f6bd6fc4ad56ee5560dc586`  
		Last Modified: Thu, 23 Mar 2023 06:12:56 GMT  
		Size: 246.5 MB (246469021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:5bbba68a87fde58385c91321cc39b88138378f3d55e4d350c04366470464355c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340890392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82694c6cb1cf9d8dda0357e098bc13ef5a648b0f6aaf51792f8f56b78932598f`
-	Default Command: `["R"]`

```dockerfile
# Wed, 01 Mar 2023 04:49:21 GMT
ADD file:802564bd8f691b73ccc068cc3c339c6a4c178bcf8383008e4f87a3774cb308b9 in / 
# Wed, 01 Mar 2023 04:49:24 GMT
CMD ["bash"]
# Wed, 15 Mar 2023 22:34:41 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 15 Mar 2023 22:34:43 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 15 Mar 2023 22:35:12 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 15 Mar 2023 22:35:17 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 15 Mar 2023 22:35:18 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 15 Mar 2023 22:35:19 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Mar 2023 22:35:21 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 15 Mar 2023 22:35:22 GMT
ENV R_BASE_VERSION=4.2.3
# Wed, 15 Mar 2023 22:35:23 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Wed, 15 Mar 2023 22:39:13 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 15 Mar 2023 22:39:16 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:adcb4bfc20e2eddc047aac97edc102514767c0f2b64f4f281f2e71651d1a97a9`  
		Last Modified: Wed, 01 Mar 2023 04:56:03 GMT  
		Size: 53.3 MB (53250177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedfba3727b0e2481a72b4c5aaa6a213881ba512ff6a1d028af1e8b3f81dfc30`  
		Last Modified: Wed, 15 Mar 2023 22:39:30 GMT  
		Size: 3.4 KB (3368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb5fcec2a4c12bb7a3877120fbcbd43e02d93c579b4ec23a7c0e3c24d034fc1`  
		Last Modified: Wed, 15 Mar 2023 22:39:33 GMT  
		Size: 25.5 MB (25513339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96945dc0c5c32df80886b134ea7800be68cdb966b65a2bc3082c7ab0e155c3f8`  
		Last Modified: Wed, 15 Mar 2023 22:39:29 GMT  
		Size: 865.9 KB (865853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ade3cdc38a2299b70a9d6872515835e21db995a3e780b27e520208c7fc83d0`  
		Last Modified: Wed, 15 Mar 2023 22:39:28 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530812c100b22df2c2bbe4d721158af28a0dc4bc9713f90be312024ed5adf3ae`  
		Last Modified: Wed, 15 Mar 2023 22:39:28 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1f24e1acd62e26949c7606c065ef3e61fb4117829f8b9cccbeedef4fad83c7`  
		Last Modified: Wed, 15 Mar 2023 22:40:21 GMT  
		Size: 261.3 MB (261257009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:52e8693051a20a597ee32b15e92010aec71ddd23f9155d2fc8179e366a90c87e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296708416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6c245f70a07cae74bce941333cae7299361d25fb7565b5d6af2ffa3e71ba12`
-	Default Command: `["R"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:12 GMT
ADD file:a96b8cacbcadb2068e0368c020589f4d2eae9fabb0965b387d5d9fc94831a1a5 in / 
# Thu, 23 Mar 2023 00:45:16 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 10:51:36 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 23 Mar 2023 10:51:37 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 23 Mar 2023 10:51:46 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:51:48 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 23 Mar 2023 10:51:48 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 23 Mar 2023 10:51:48 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Mar 2023 10:51:49 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 23 Mar 2023 10:51:49 GMT
ENV R_BASE_VERSION=4.2.3
# Thu, 23 Mar 2023 10:51:50 GMT
RUN echo "deb http://deb.debian.org/debian experimental main" > /etc/apt/sources.list.d/experimental.list     && echo "deb [trusted=yes] https://eddelbuettel.github.io/ppaR400 ./" > /etc/apt/sources.list.d/edd-r4.list
# Thu, 23 Mar 2023 10:52:53 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:53:04 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:57560ce693355ef04b6283597b61cd71f7e8b7d7357b218eab0c8979bce7812e`  
		Last Modified: Thu, 23 Mar 2023 00:48:17 GMT  
		Size: 47.7 MB (47671021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80793af67a69232cadace34e10b9ef46d1ba6f3755a4614ccbfb7a911f055a9`  
		Last Modified: Thu, 23 Mar 2023 10:53:16 GMT  
		Size: 3.4 KB (3357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399fe0d57620fc4b657bb26fc130a45cf377513e271deb6fa7b2430a78ed54e3`  
		Last Modified: Thu, 23 Mar 2023 10:53:17 GMT  
		Size: 24.8 MB (24801489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4f7d7095b671f7050cb36cce96b79401ba687ff33672f032f5bddf44ecab9b`  
		Last Modified: Thu, 23 Mar 2023 10:53:15 GMT  
		Size: 921.0 KB (921009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4593aadb093cfdef343d4697cdbe74987731c5b65b563859b94321451ccda65`  
		Last Modified: Thu, 23 Mar 2023 10:53:15 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3069e7378cf84ce8edecd9a388442fd79d6a305de51d312c72859f4a652685`  
		Last Modified: Thu, 23 Mar 2023 10:53:15 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b341b8c60321724abfbc967e97de155e9a198bb86c525745b76bc63085e26bfd`  
		Last Modified: Thu, 23 Mar 2023 10:53:39 GMT  
		Size: 223.3 MB (223310900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

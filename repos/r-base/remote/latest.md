## `r-base:latest`

```console
$ docker pull r-base@sha256:5d4e2bb2c39c498bc5646d9d63d42137f9c7fe16318e6536e1b1dfcc3d938e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:385aab62163cc49a38acc3bf4514b2ba8a1c045d8110c78aaa8b543f290d8bf5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339621927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2931a1428b2039d448015ef081c8df6642fd3e4a045fde3995d386c886312688`
-	Default Command: `["R"]`

```dockerfile
# Wed, 01 Nov 2023 00:23:10 GMT
ADD file:490136e40a0d35b152441fda2b93822007355ecd4d486c38c8155e8b91bd5184 in / 
# Wed, 01 Nov 2023 00:23:10 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:40:08 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 01 Nov 2023 00:40:09 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 01 Nov 2023 00:40:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 00:40:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 01 Nov 2023 00:40:21 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 01 Nov 2023 00:40:21 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Nov 2023 00:40:22 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 01 Nov 2023 00:40:22 GMT
ENV R_BASE_VERSION=4.3.2
# Wed, 01 Nov 2023 00:41:18 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 00:41:19 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:cc0e49fb24dacf25e2f403d80c5af0757c0d2ac2e78f76919d7076074002f56b`  
		Last Modified: Wed, 01 Nov 2023 00:29:34 GMT  
		Size: 49.5 MB (49486907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410abd4a91fd7387d1f66faa2a588982a807b9f26d378ff3e5e8f0c445813eb2`  
		Last Modified: Wed, 01 Nov 2023 00:41:37 GMT  
		Size: 3.4 KB (3359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb26c87e9fc6326ec5e5b7c29cb5d715b84d07c4dce832ee5c976fb7d53e80d`  
		Last Modified: Wed, 01 Nov 2023 00:41:40 GMT  
		Size: 25.5 MB (25519450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe3157a71a2494ebd437258d9164723f30275d64bd12646e4d7b66cc4b96b6f`  
		Last Modified: Wed, 01 Nov 2023 00:41:38 GMT  
		Size: 866.3 KB (866330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bd4eedb218124b1068662b290842ee5b11765db1aa2823a8bd64262464b922`  
		Last Modified: Wed, 01 Nov 2023 00:41:37 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80350fda693b432675e367b8ed58e192afdebdd3fee2332a72730c19a9a4e6e`  
		Last Modified: Wed, 01 Nov 2023 00:42:05 GMT  
		Size: 263.7 MB (263745533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:9ce83b19f25216bb44b8556c3dc1fc48b6e48efef9751f18bd68bcdcdad61e14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325944778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e14965ac7b024c5785809324f70ada888648462ed1616a3128e422a293b29d`
-	Default Command: `["R"]`

```dockerfile
# Wed, 01 Nov 2023 00:41:12 GMT
ADD file:422607799f7f9a353c26d961c9d74341ac8915480afc1832e0a10b1e0bae871e in / 
# Wed, 01 Nov 2023 00:41:13 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:26:00 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 01 Nov 2023 11:26:01 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 01 Nov 2023 11:26:10 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:26:12 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 01 Nov 2023 11:26:12 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 01 Nov 2023 11:26:12 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Nov 2023 11:26:13 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 01 Nov 2023 11:26:13 GMT
ENV R_BASE_VERSION=4.3.2
# Wed, 01 Nov 2023 11:26:57 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:27:01 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e920ac680f72fa3419c6aa8862ff3df12d1f7f9eea6e98da5486f89f1e356e27`  
		Last Modified: Wed, 01 Nov 2023 00:46:43 GMT  
		Size: 49.5 MB (49495234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8316b8807a973cb3913b3ffda87ee32da648e2257beec36a27393e60a3650`  
		Last Modified: Wed, 01 Nov 2023 11:27:15 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7f0ec8b0020c6675a22eca0e073a7d6de2045b92a65065afdb931f9153f5c3`  
		Last Modified: Wed, 01 Nov 2023 11:27:17 GMT  
		Size: 25.4 MB (25361518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9bcd0297cc232cf337d25ad3dc3057a95729183e1a313238982aadad2f86cd`  
		Last Modified: Wed, 01 Nov 2023 11:27:15 GMT  
		Size: 866.3 KB (866336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41c09d66286b3059a0eb0dc13f83d51b7bea7c6da20f618ff77ed5ca16520dd`  
		Last Modified: Wed, 01 Nov 2023 11:27:15 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a095c9b65f89ed035808761d21dbf074cbaab237dccf242952a150f0b825a07a`  
		Last Modified: Wed, 01 Nov 2023 11:27:35 GMT  
		Size: 250.2 MB (250217981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:eceee8385138c77362bdf6669ab5c291719cd11f1a4a89280f0d3c36f49e60a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338345161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2706e4c3e0506ab6e4e4d14b3a79e365f0bc862a8ea4217eeaac5515ab364db0`
-	Default Command: `["R"]`

```dockerfile
# Tue, 21 Nov 2023 04:26:21 GMT
ADD file:71d427bbf9540f83121632225a69e48179f2f39399ea9fd6fecee1c14a31ccfd in / 
# Tue, 21 Nov 2023 04:26:24 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:46:08 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 21 Nov 2023 12:46:10 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 21 Nov 2023 12:46:27 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:46:31 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 21 Nov 2023 12:46:31 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 21 Nov 2023 12:46:32 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Nov 2023 12:46:33 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 21 Nov 2023 12:46:33 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 21 Nov 2023 12:48:04 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:48:12 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:98137b81bb887133d8b0852640651013383090ed775e3e79027ef2fcdd4c97ec`  
		Last Modified: Tue, 21 Nov 2023 04:32:02 GMT  
		Size: 53.4 MB (53437880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c5fc34f7461465714ff64c9677c9f6180a66dfb8c8c84e491ecd02f15eee53`  
		Last Modified: Tue, 21 Nov 2023 12:48:23 GMT  
		Size: 3.4 KB (3361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f1bace27bc6c9d2206d944a5fa5c16c19d4d7b62d6371581130944a8a1b402`  
		Last Modified: Tue, 21 Nov 2023 12:48:26 GMT  
		Size: 25.9 MB (25913869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c3b0b8501a31bb280bc0967c3546e5ffe2c8be0ec75c664429578e66462560`  
		Last Modified: Tue, 21 Nov 2023 12:48:23 GMT  
		Size: 866.3 KB (866338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5503fa64e155ef3f38020cb39d4ef61e25bd09b9f8d7a5df1cfa9547896ab104`  
		Last Modified: Tue, 21 Nov 2023 12:48:23 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f5f3eef71e881c4bfcd0e60deaed602b6cbebe8c32f5534b602da9a88a6134`  
		Last Modified: Tue, 21 Nov 2023 12:48:55 GMT  
		Size: 258.1 MB (258123365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:f927bb32725ccd9f73b1e72ab156720cf1ec51d13aaf287cee32d5094fe6d81d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305922675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2863c92c9fbbbd8734d662c56d886e8c5a4496ca74e16cf221481e46bfdec4`
-	Default Command: `["R"]`

```dockerfile
# Tue, 21 Nov 2023 05:07:18 GMT
ADD file:6bcc5494bc5ece86858cc0a9db1f3dbaed7e64670b3a78b5868b8795646fb7c4 in / 
# Tue, 21 Nov 2023 05:07:26 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 15:09:11 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 21 Nov 2023 15:09:12 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 21 Nov 2023 15:09:21 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 15:09:23 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 21 Nov 2023 15:09:23 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 21 Nov 2023 15:09:24 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Nov 2023 15:09:24 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 21 Nov 2023 15:09:24 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 21 Nov 2023 15:10:05 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 15:10:15 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f502a1e486510d668a00f33968ab7fd0960f1db8c92e8904a91b1b728da08811`  
		Last Modified: Tue, 21 Nov 2023 05:12:03 GMT  
		Size: 49.0 MB (48970248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ef4ea96762e9408aa8d27f243ec0eebd41a2ea3bc000ff57a70874b98c0040`  
		Last Modified: Tue, 21 Nov 2023 15:10:26 GMT  
		Size: 3.4 KB (3356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae05cfdf5c91d7d5200c0a39f91de293045fba947d0e35d5cd8cc01434c4333`  
		Last Modified: Tue, 21 Nov 2023 15:10:28 GMT  
		Size: 25.4 MB (25367370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5363787978c47db3288cb552ea0fb83283d25cb58eded84a559ee107b8dbde21`  
		Last Modified: Tue, 21 Nov 2023 15:10:26 GMT  
		Size: 922.3 KB (922274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fc86cdc750e4a9af6baea9d15a1533f11f5cbff624cbd2c2aa0047f1229763`  
		Last Modified: Tue, 21 Nov 2023 15:10:26 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd96d1cdca6763ad46269ada70fa43ef6ab53b45141ee556f7c707f12b18212`  
		Last Modified: Tue, 21 Nov 2023 15:10:49 GMT  
		Size: 230.7 MB (230659078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

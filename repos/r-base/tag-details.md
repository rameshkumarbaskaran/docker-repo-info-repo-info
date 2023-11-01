<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.3.2`](#r-base432)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.3.2`

```console
$ docker pull r-base@sha256:e0a209a2c84336d0159cf5943dd711b8f47c5469aa867f379575a71130c1dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.3.2` - linux; amd64

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

### `r-base:4.3.2` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:8880164830d7cff80b95c4e5268ccccbe228ea293e88c1fceeb0c93e298d247c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.0 MB (328044094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e16ff4028f486367d4102dbec06d2bfbe16e3113ed571ce15cbcf640a6780d1`
-	Default Command: `["R"]`

```dockerfile
# Wed, 11 Oct 2023 18:26:23 GMT
ADD file:c48ddb3be6db73fb74475f132903784b2239816dcf46a967c1bfb0f8a23fd0bb in / 
# Wed, 11 Oct 2023 18:26:23 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:09:17 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 12 Oct 2023 10:09:18 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 12 Oct 2023 10:09:28 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:09:30 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 12 Oct 2023 10:09:30 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 12 Oct 2023 10:09:30 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Oct 2023 10:09:31 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 31 Oct 2023 23:57:41 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 31 Oct 2023 23:58:50 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 23:58:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:484b389f95af6a0503d73ac652b29ef33a2d2fbb6e295f8bbe656d503a592a3a`  
		Last Modified: Wed, 11 Oct 2023 18:32:10 GMT  
		Size: 49.5 MB (49505546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f70272f1692c9b4f82ef47a9cf030b16fcf04ba6e41714d479d7e3bd53d1e28`  
		Last Modified: Thu, 12 Oct 2023 10:10:45 GMT  
		Size: 3.4 KB (3361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de85415d442decef501bde5fc680d6243552b2ad6415fa30678ade91a6fae187`  
		Last Modified: Thu, 12 Oct 2023 10:10:48 GMT  
		Size: 25.4 MB (25358078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ed2dad41a93e49b56e4cac1f9350988542196eb096a932846fddb4efc6daad`  
		Last Modified: Thu, 12 Oct 2023 10:10:45 GMT  
		Size: 866.3 KB (866330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d61c476288523fd5e434fc762a49df0e3beccd99114bbdc0e9b7e8c5c1e244d`  
		Last Modified: Thu, 12 Oct 2023 10:10:45 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f1ca7f0aaa0c47dba5df9576249cd1cf78143f079f9ddf735ec6736e19f2d0`  
		Last Modified: Tue, 31 Oct 2023 23:59:32 GMT  
		Size: 252.3 MB (252310428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.2` - linux; ppc64le

```console
$ docker pull r-base@sha256:11f1e37c9ca93f7f7876a466d4a1f4a6ce54591fc0f7d1470a275500bf48c8de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338270248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90692f6752d61d2a208afecc8823975725f7d40a64796332f2adace254a6f382`
-	Default Command: `["R"]`

```dockerfile
# Wed, 01 Nov 2023 00:23:36 GMT
ADD file:2a57f528bf7c5e3f557f80c7b960cad458b8d6815a64f2364bb079efad5cc0df in / 
# Wed, 01 Nov 2023 00:23:40 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:42:06 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 01 Nov 2023 00:42:07 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 01 Nov 2023 00:42:27 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 00:42:30 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 01 Nov 2023 00:42:30 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 01 Nov 2023 00:42:31 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Nov 2023 00:42:32 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 01 Nov 2023 00:42:32 GMT
ENV R_BASE_VERSION=4.3.2
# Wed, 01 Nov 2023 00:45:06 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 00:45:15 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c86f9849ab446c023b055adf524217a29db6df1063fa124656a744d8c5454154`  
		Last Modified: Wed, 01 Nov 2023 00:29:10 GMT  
		Size: 53.4 MB (53390711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8b9e5b4d13e93f32a3d7cbe2c8d464286c2e4d2eee0dd7800fd9769081a26`  
		Last Modified: Wed, 01 Nov 2023 00:45:36 GMT  
		Size: 3.4 KB (3361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dade9eae0562c772992e6fbc0cb14c52ddb421454e32631e43fab3f05e0a146`  
		Last Modified: Wed, 01 Nov 2023 00:45:40 GMT  
		Size: 25.9 MB (25913734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f55ed3660805bf925bb6a613548ed7add35971f3e14a289046869f0532a6f1`  
		Last Modified: Wed, 01 Nov 2023 00:45:36 GMT  
		Size: 866.3 KB (866328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97736b6dd71673945310440ab1bb5407aa2a7818cb60334faeeb43e0a6844919`  
		Last Modified: Wed, 01 Nov 2023 00:45:36 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b654c28e681ed6d00ce9e8a52b9018687104f0d25452ddab62a61550f70399`  
		Last Modified: Wed, 01 Nov 2023 00:46:08 GMT  
		Size: 258.1 MB (258095763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.2` - linux; s390x

```console
$ docker pull r-base@sha256:387c5dd9e9a1c16fd7997241b5ac48f43b35d7cc560d1d466818273af15f954c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305824259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c713e34a45245b0dba6ab9d564422d88dc3e0c46085ab44f6743dfcfbd2a06`
-	Default Command: `["R"]`

```dockerfile
# Wed, 01 Nov 2023 00:45:04 GMT
ADD file:c1e9cc0f1e50baa8f4578d6066a853f19ddeadaa04b24e2c8666570b775be9af in / 
# Wed, 01 Nov 2023 00:45:08 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 08:33:23 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 01 Nov 2023 08:33:23 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 01 Nov 2023 08:33:46 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 08:33:51 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 01 Nov 2023 08:33:52 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 01 Nov 2023 08:33:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Nov 2023 08:33:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 01 Nov 2023 08:33:54 GMT
ENV R_BASE_VERSION=4.3.2
# Wed, 01 Nov 2023 08:35:08 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 08:35:33 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:01519b303830161a8a78b116a589cddd3dd917366a480e71bfd6b19f14adcfc2`  
		Last Modified: Wed, 01 Nov 2023 00:50:14 GMT  
		Size: 48.9 MB (48900179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a017d199d37bfd3692e3d945c9b513c1088e458e354a230817e5777b14d1300`  
		Last Modified: Wed, 01 Nov 2023 08:35:49 GMT  
		Size: 3.4 KB (3357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f81b98a8d62afa4c8b4c0869fd32f11bcffb39899ea929bc7ca428933ad346b`  
		Last Modified: Wed, 01 Nov 2023 08:35:52 GMT  
		Size: 25.4 MB (25367387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc07e173ac8c7524973454f857fa8a452f59261bfdbbea45d38b454f2fca285`  
		Last Modified: Wed, 01 Nov 2023 08:35:49 GMT  
		Size: 922.3 KB (922277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c30c0089171aea3e78f4a63f6a7c3a51eac01762b865ccda63d176b13690044`  
		Last Modified: Wed, 01 Nov 2023 08:35:49 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91253d43fd3ec6f0ca128d4e5e7485e64fef0cd3a91896022521f870c08fd6c2`  
		Last Modified: Wed, 01 Nov 2023 08:36:18 GMT  
		Size: 230.6 MB (230630710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:e0a209a2c84336d0159cf5943dd711b8f47c5469aa867f379575a71130c1dc84
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
$ docker pull r-base@sha256:8880164830d7cff80b95c4e5268ccccbe228ea293e88c1fceeb0c93e298d247c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.0 MB (328044094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e16ff4028f486367d4102dbec06d2bfbe16e3113ed571ce15cbcf640a6780d1`
-	Default Command: `["R"]`

```dockerfile
# Wed, 11 Oct 2023 18:26:23 GMT
ADD file:c48ddb3be6db73fb74475f132903784b2239816dcf46a967c1bfb0f8a23fd0bb in / 
# Wed, 11 Oct 2023 18:26:23 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:09:17 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 12 Oct 2023 10:09:18 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 12 Oct 2023 10:09:28 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:09:30 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 12 Oct 2023 10:09:30 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 12 Oct 2023 10:09:30 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Oct 2023 10:09:31 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 31 Oct 2023 23:57:41 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 31 Oct 2023 23:58:50 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Oct 2023 23:58:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:484b389f95af6a0503d73ac652b29ef33a2d2fbb6e295f8bbe656d503a592a3a`  
		Last Modified: Wed, 11 Oct 2023 18:32:10 GMT  
		Size: 49.5 MB (49505546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f70272f1692c9b4f82ef47a9cf030b16fcf04ba6e41714d479d7e3bd53d1e28`  
		Last Modified: Thu, 12 Oct 2023 10:10:45 GMT  
		Size: 3.4 KB (3361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de85415d442decef501bde5fc680d6243552b2ad6415fa30678ade91a6fae187`  
		Last Modified: Thu, 12 Oct 2023 10:10:48 GMT  
		Size: 25.4 MB (25358078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ed2dad41a93e49b56e4cac1f9350988542196eb096a932846fddb4efc6daad`  
		Last Modified: Thu, 12 Oct 2023 10:10:45 GMT  
		Size: 866.3 KB (866330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d61c476288523fd5e434fc762a49df0e3beccd99114bbdc0e9b7e8c5c1e244d`  
		Last Modified: Thu, 12 Oct 2023 10:10:45 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f1ca7f0aaa0c47dba5df9576249cd1cf78143f079f9ddf735ec6736e19f2d0`  
		Last Modified: Tue, 31 Oct 2023 23:59:32 GMT  
		Size: 252.3 MB (252310428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:11f1e37c9ca93f7f7876a466d4a1f4a6ce54591fc0f7d1470a275500bf48c8de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338270248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90692f6752d61d2a208afecc8823975725f7d40a64796332f2adace254a6f382`
-	Default Command: `["R"]`

```dockerfile
# Wed, 01 Nov 2023 00:23:36 GMT
ADD file:2a57f528bf7c5e3f557f80c7b960cad458b8d6815a64f2364bb079efad5cc0df in / 
# Wed, 01 Nov 2023 00:23:40 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:42:06 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 01 Nov 2023 00:42:07 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 01 Nov 2023 00:42:27 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 00:42:30 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 01 Nov 2023 00:42:30 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 01 Nov 2023 00:42:31 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Nov 2023 00:42:32 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 01 Nov 2023 00:42:32 GMT
ENV R_BASE_VERSION=4.3.2
# Wed, 01 Nov 2023 00:45:06 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 00:45:15 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c86f9849ab446c023b055adf524217a29db6df1063fa124656a744d8c5454154`  
		Last Modified: Wed, 01 Nov 2023 00:29:10 GMT  
		Size: 53.4 MB (53390711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8b9e5b4d13e93f32a3d7cbe2c8d464286c2e4d2eee0dd7800fd9769081a26`  
		Last Modified: Wed, 01 Nov 2023 00:45:36 GMT  
		Size: 3.4 KB (3361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dade9eae0562c772992e6fbc0cb14c52ddb421454e32631e43fab3f05e0a146`  
		Last Modified: Wed, 01 Nov 2023 00:45:40 GMT  
		Size: 25.9 MB (25913734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f55ed3660805bf925bb6a613548ed7add35971f3e14a289046869f0532a6f1`  
		Last Modified: Wed, 01 Nov 2023 00:45:36 GMT  
		Size: 866.3 KB (866328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97736b6dd71673945310440ab1bb5407aa2a7818cb60334faeeb43e0a6844919`  
		Last Modified: Wed, 01 Nov 2023 00:45:36 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b654c28e681ed6d00ce9e8a52b9018687104f0d25452ddab62a61550f70399`  
		Last Modified: Wed, 01 Nov 2023 00:46:08 GMT  
		Size: 258.1 MB (258095763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:387c5dd9e9a1c16fd7997241b5ac48f43b35d7cc560d1d466818273af15f954c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305824259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c713e34a45245b0dba6ab9d564422d88dc3e0c46085ab44f6743dfcfbd2a06`
-	Default Command: `["R"]`

```dockerfile
# Wed, 01 Nov 2023 00:45:04 GMT
ADD file:c1e9cc0f1e50baa8f4578d6066a853f19ddeadaa04b24e2c8666570b775be9af in / 
# Wed, 01 Nov 2023 00:45:08 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 08:33:23 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 01 Nov 2023 08:33:23 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 01 Nov 2023 08:33:46 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 08:33:51 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 01 Nov 2023 08:33:52 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 01 Nov 2023 08:33:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Nov 2023 08:33:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 01 Nov 2023 08:33:54 GMT
ENV R_BASE_VERSION=4.3.2
# Wed, 01 Nov 2023 08:35:08 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 08:35:33 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:01519b303830161a8a78b116a589cddd3dd917366a480e71bfd6b19f14adcfc2`  
		Last Modified: Wed, 01 Nov 2023 00:50:14 GMT  
		Size: 48.9 MB (48900179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a017d199d37bfd3692e3d945c9b513c1088e458e354a230817e5777b14d1300`  
		Last Modified: Wed, 01 Nov 2023 08:35:49 GMT  
		Size: 3.4 KB (3357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f81b98a8d62afa4c8b4c0869fd32f11bcffb39899ea929bc7ca428933ad346b`  
		Last Modified: Wed, 01 Nov 2023 08:35:52 GMT  
		Size: 25.4 MB (25367387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc07e173ac8c7524973454f857fa8a452f59261bfdbbea45d38b454f2fca285`  
		Last Modified: Wed, 01 Nov 2023 08:35:49 GMT  
		Size: 922.3 KB (922277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c30c0089171aea3e78f4a63f6a7c3a51eac01762b865ccda63d176b13690044`  
		Last Modified: Wed, 01 Nov 2023 08:35:49 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91253d43fd3ec6f0ca128d4e5e7485e64fef0cd3a91896022521f870c08fd6c2`  
		Last Modified: Wed, 01 Nov 2023 08:36:18 GMT  
		Size: 230.6 MB (230630710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

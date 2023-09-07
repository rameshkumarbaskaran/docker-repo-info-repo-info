## `r-base:latest`

```console
$ docker pull r-base@sha256:d9d1467834e83f9157ba138300270943fb98f7bd6bbc707af08a7d66288aab1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:5615a9a0fc5054296d845d8c5f8dcfc7417a5c237f903a8995a003cb2c6cde35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339210509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f425c33941b1c44d702c370df57c6dbca5f25f6fd84cfe9186c1af039acef23e`
-	Default Command: `["R"]`

```dockerfile
# Thu, 07 Sep 2023 00:23:06 GMT
ADD file:76da3f2b01205bf031c5a2baa5619f5692978dddb951a74e40bb95b7153a58b3 in / 
# Thu, 07 Sep 2023 00:23:07 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 04:58:13 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 07 Sep 2023 04:58:13 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 07 Sep 2023 04:58:24 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 04:58:26 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 07 Sep 2023 04:58:26 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 07 Sep 2023 04:58:26 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Sep 2023 04:58:27 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 07 Sep 2023 04:58:27 GMT
ENV R_BASE_VERSION=4.3.1
# Thu, 07 Sep 2023 04:59:18 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 04:59:20 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:e20a7cf08f98f931d334586c1398ad4809e12fa399f21f419a18fabc331e71b0`  
		Last Modified: Thu, 07 Sep 2023 00:29:42 GMT  
		Size: 49.5 MB (49514768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989d7e82ac05c8b7ba3b86d23d02667e4dba28797ca8e9930bcea6948c8ac9aa`  
		Last Modified: Thu, 07 Sep 2023 04:59:28 GMT  
		Size: 3.4 KB (3361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef00ee4aaa57bf4bbb3cebf3fcf6c946ef924bd6e357773f2438e8f3d777f650`  
		Last Modified: Thu, 07 Sep 2023 04:59:31 GMT  
		Size: 25.5 MB (25510919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3212e9ec9f51477194bdd8ae4d3d4059c9786f771190f9961d108bc58ae3f6db`  
		Last Modified: Thu, 07 Sep 2023 04:59:29 GMT  
		Size: 866.3 KB (866324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f61e6bc960e377f4640531e13d60c4203678c5418b82db9c57720b1a29f34f`  
		Last Modified: Thu, 07 Sep 2023 04:59:28 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d48ba8581c4c2a69faa4464d1536b45cc05bdc90513236889675a733cef0686`  
		Last Modified: Thu, 07 Sep 2023 04:59:57 GMT  
		Size: 263.3 MB (263314788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:61ceb54e8ab59eef9be9f32ce2f0912f0a830de19c8016e43d70cd93fdbca73e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.9 MB (581905349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946bef997180497fd51e50cafdf7518b14f68b0871515e704d47a4dba63eb700`
-	Default Command: `["R"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:28 GMT
ADD file:4140d565c599e759836b448aa03732461eb29cbc683f3162d889a36569afd8fb in / 
# Tue, 15 Aug 2023 23:41:28 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 09:57:24 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 16 Aug 2023 09:57:24 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 16 Aug 2023 09:57:34 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 09:57:36 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 16 Aug 2023 09:57:36 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 09:57:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 16 Aug 2023 09:57:36 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 16 Aug 2023 09:57:36 GMT
ENV R_BASE_VERSION=4.3.1
# Wed, 16 Aug 2023 09:59:25 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 09:59:34 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:786a118997b083196267446ee0d1d1a908f05fd7748fa2ed8e7560d0db91bf72`  
		Last Modified: Tue, 15 Aug 2023 23:46:51 GMT  
		Size: 49.5 MB (49522071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d83fe0e801ebfcea9f1b76e2d3a8440948795b4173507fbc218a4d0b24009a2`  
		Last Modified: Wed, 16 Aug 2023 09:59:51 GMT  
		Size: 3.4 KB (3364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90260b3794100e8ca45e25b490573585537a0f5070fa7fea3c9e3fab734d0635`  
		Last Modified: Wed, 16 Aug 2023 09:59:54 GMT  
		Size: 25.3 MB (25332557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4071048ed0b5296edd81d86859527b4c78eae2950098ec7fa5bfefa3bac8a9`  
		Last Modified: Wed, 16 Aug 2023 09:59:51 GMT  
		Size: 866.3 KB (866323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b2ee2534203ec1a0438301d7f1788da0a08d364ed5f9b79ac8296d7a34dc78`  
		Last Modified: Wed, 16 Aug 2023 09:59:51 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1900525746163e2da1fe569b2d41dc345d5d388177d7b771ca4c281b58094a6`  
		Last Modified: Wed, 16 Aug 2023 10:00:37 GMT  
		Size: 506.2 MB (506180685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:5c9ca6167684dab45c62b5d0b43e2a11c05c300f0e1f9b8c1e477cfc7ecf5902
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338396998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4e864721a1924ed14de3c8120328f7c119f45aefbd11f01d51bfb459120968`
-	Default Command: `["R"]`

```dockerfile
# Thu, 07 Sep 2023 00:20:13 GMT
ADD file:69350b5a5e94c4a556e56f265533a04f8035ebc4bd834bec57b98a246ee547a6 in / 
# Thu, 07 Sep 2023 00:20:18 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 07:52:45 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 07 Sep 2023 07:52:48 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 07 Sep 2023 07:53:28 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 07:53:44 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 07 Sep 2023 07:53:48 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 07 Sep 2023 07:53:49 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Sep 2023 07:53:51 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 07 Sep 2023 07:53:51 GMT
ENV R_BASE_VERSION=4.3.1
# Thu, 07 Sep 2023 07:58:26 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 07:58:55 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:7c3a2b005dd31b7bb84d8511ccf37b021f6db4066b3d2136dbdc778ea24e8eac`  
		Last Modified: Thu, 07 Sep 2023 00:27:03 GMT  
		Size: 53.5 MB (53456014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a62c27e3b7ea4074a864783e569e58370fe48a58945723abd7ce0afe5cc3e1f`  
		Last Modified: Thu, 07 Sep 2023 07:59:14 GMT  
		Size: 3.4 KB (3363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4fcf9c4487f7dec0eba22ec1f9ce207e9c2aa252d1b4a508a0194eecc14b59`  
		Last Modified: Thu, 07 Sep 2023 07:59:19 GMT  
		Size: 25.9 MB (25912663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca07462b1f5396f1ecbb4280e71d657cba788b0c394d3a51896957f97bd2fe6b`  
		Last Modified: Thu, 07 Sep 2023 07:59:15 GMT  
		Size: 866.3 KB (866331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5761ff250027db062cbec4d8b210bd79a30ad24ee88cb5244f1ded5b6c9909`  
		Last Modified: Thu, 07 Sep 2023 07:59:14 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61be84fe4fa237471e009cdb42f286ef8aae9dde60138f8cbdf67adcdc753c22`  
		Last Modified: Thu, 07 Sep 2023 08:00:06 GMT  
		Size: 258.2 MB (258158276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:af1a06ec96f6c49951a4aaae68880105763281bd219d499ecfc7a11e446db47d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.9 MB (533865166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9503dedb8b9317e82bf3c2c1fd8ecb8383abdae941ffb9d2279d6b7d9fe511bb`
-	Default Command: `["R"]`

```dockerfile
# Tue, 15 Aug 2023 23:44:56 GMT
ADD file:8ee59edaaa7d4498cb111901a75ed6d7cfa7dc646dde70eabca650d719fb7d57 in / 
# Tue, 15 Aug 2023 23:45:03 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 05:09:41 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 16 Aug 2023 05:09:41 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Wed, 16 Aug 2023 05:09:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 05:09:52 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 16 Aug 2023 05:09:52 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 05:09:52 GMT
ENV LANG=en_US.UTF-8
# Wed, 16 Aug 2023 05:09:53 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 16 Aug 2023 05:09:53 GMT
ENV R_BASE_VERSION=4.3.1
# Wed, 16 Aug 2023 05:11:26 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 05:11:46 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:977206ef11492cbb9ef774b7ffa955b2066c215ff2be2d1fbb83d474a8d85cfc`  
		Last Modified: Tue, 15 Aug 2023 23:49:47 GMT  
		Size: 48.5 MB (48539796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9d13b5544e64004b75c4f6d8fe7aaadfdea805229b093d73066b55d5e87024`  
		Last Modified: Wed, 16 Aug 2023 05:12:08 GMT  
		Size: 3.4 KB (3362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f7ca405f6e5177dd1bd80022f22a857fc3408bec99db950d9a20e50d554ca9`  
		Last Modified: Wed, 16 Aug 2023 05:12:10 GMT  
		Size: 25.3 MB (25272073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f278ffb8e47f400d54a0f55b66460a3b5b0e1425c1e3177f76b1c812776836d1`  
		Last Modified: Wed, 16 Aug 2023 05:12:08 GMT  
		Size: 922.3 KB (922275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1975728fe1aae6412f3e99197e6225f2b3dffabfafd2c99de5dfa8b25e66c3`  
		Last Modified: Wed, 16 Aug 2023 05:12:08 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8d1fae64bc2171e3bfff6e6b315a1e9e9664623711f5c6f0e97a81a49f912e`  
		Last Modified: Wed, 16 Aug 2023 05:12:56 GMT  
		Size: 459.1 MB (459127310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.3.1`](#r-base431)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.3.1`

```console
$ docker pull r-base@sha256:7eec64c4abb9b2b98c38bdec584ab4fdc7d3c1f265db9420e9fc47b58d0994b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.3.1` - linux; amd64

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

### `r-base:4.3.1` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:adce400779f0f2b4f30edd4bd1622f136c2bda4584c268ebf3f6689d8e200c3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325471607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92155b4b21442206020d553c15ab0e046d97040a6017ed31991fa10d4d75e8f1`
-	Default Command: `["R"]`

```dockerfile
# Thu, 07 Sep 2023 00:41:08 GMT
ADD file:69f87b30025e86f5acfb8429da721cfe92ff7a1c139df827231caa96a982a89a in / 
# Thu, 07 Sep 2023 00:41:09 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:41:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 07 Sep 2023 09:41:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 07 Sep 2023 09:41:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:41:50 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 07 Sep 2023 09:41:50 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 07 Sep 2023 09:41:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Sep 2023 09:41:51 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 07 Sep 2023 09:41:51 GMT
ENV R_BASE_VERSION=4.3.1
# Thu, 07 Sep 2023 09:42:42 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:42:47 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:cbef94b03c52659992feffae251a9a4af30679b4e560f2f8fa84e26f3ce8140c`  
		Last Modified: Thu, 07 Sep 2023 00:46:33 GMT  
		Size: 49.4 MB (49445334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d454ac763c9575efed0bae2752d7cc051d5e358c7b8d844b29544761fd49b489`  
		Last Modified: Thu, 07 Sep 2023 09:43:05 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7040be56146dfb573404e89439f1a5c42b6fc1db8596d6bc56def0d7266380`  
		Last Modified: Thu, 07 Sep 2023 09:43:08 GMT  
		Size: 25.3 MB (25333036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f840420237bd9e60e6820d10249b5d34925acbfaa5fea3de34a6c98bbc2c0d4`  
		Last Modified: Thu, 07 Sep 2023 09:43:06 GMT  
		Size: 866.3 KB (866332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bda2f17df293208d888dda01ad2f1985101f0fbd42e3faf8013531e43c34ad4`  
		Last Modified: Thu, 07 Sep 2023 09:43:05 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de910b53b299ac3a4635a8f6f5c361f449e7e75accd105e1b4ac6f5ef5d2af2`  
		Last Modified: Thu, 07 Sep 2023 09:43:26 GMT  
		Size: 249.8 MB (249823197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.1` - linux; ppc64le

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

### `r-base:4.3.1` - linux; s390x

```console
$ docker pull r-base@sha256:a8764fb36644d7be23147b28659068455571561d50e1a644290b6f03449ba173
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304665343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7da3b6a54d3c4a6cc1b4d9a50e672e482485b61bed78f7a72e4e623606e3f7`
-	Default Command: `["R"]`

```dockerfile
# Thu, 07 Sep 2023 00:46:52 GMT
ADD file:abcf51b81cd6f9cfc93b9963d223d2066f6e087d383af2edcf8f9a577dc23efd in / 
# Thu, 07 Sep 2023 00:46:56 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:40:04 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 07 Sep 2023 09:40:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 07 Sep 2023 09:40:14 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:40:19 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 07 Sep 2023 09:40:19 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 07 Sep 2023 09:40:19 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Sep 2023 09:40:20 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 07 Sep 2023 09:40:20 GMT
ENV R_BASE_VERSION=4.3.1
# Thu, 07 Sep 2023 09:41:06 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:41:17 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ee1a4ae1256a1fd777550db8f08b55a9e6e2b2d07e77c364c53343f9f594e95e`  
		Last Modified: Thu, 07 Sep 2023 00:51:44 GMT  
		Size: 48.6 MB (48573786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03025c0e3c889235f049b357ed661eace9c82b7be8a31e98238e7a0b34e095c3`  
		Last Modified: Thu, 07 Sep 2023 09:41:30 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a132777548148b85928877f34abf6850a75a747f64196b930ffd836daf89e3`  
		Last Modified: Thu, 07 Sep 2023 09:41:33 GMT  
		Size: 25.3 MB (25272584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d08035c8849c57c73a3536e4f21777b0b4a5fecf2b17a4f20887f9c2603990`  
		Last Modified: Thu, 07 Sep 2023 09:41:30 GMT  
		Size: 922.3 KB (922279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c17d461902e3ebc69614273386960076f6ddeaa704b78ab71231fb697e9ee7`  
		Last Modified: Thu, 07 Sep 2023 09:41:30 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c65f79fd283303b8a04da44a4d7f225af5be9f62e5aa4ad604f7486be58f5c`  
		Last Modified: Thu, 07 Sep 2023 09:41:54 GMT  
		Size: 229.9 MB (229892984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:7eec64c4abb9b2b98c38bdec584ab4fdc7d3c1f265db9420e9fc47b58d0994b1
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
$ docker pull r-base@sha256:adce400779f0f2b4f30edd4bd1622f136c2bda4584c268ebf3f6689d8e200c3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325471607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92155b4b21442206020d553c15ab0e046d97040a6017ed31991fa10d4d75e8f1`
-	Default Command: `["R"]`

```dockerfile
# Thu, 07 Sep 2023 00:41:08 GMT
ADD file:69f87b30025e86f5acfb8429da721cfe92ff7a1c139df827231caa96a982a89a in / 
# Thu, 07 Sep 2023 00:41:09 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:41:38 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 07 Sep 2023 09:41:38 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 07 Sep 2023 09:41:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:41:50 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 07 Sep 2023 09:41:50 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 07 Sep 2023 09:41:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Sep 2023 09:41:51 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 07 Sep 2023 09:41:51 GMT
ENV R_BASE_VERSION=4.3.1
# Thu, 07 Sep 2023 09:42:42 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:42:47 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:cbef94b03c52659992feffae251a9a4af30679b4e560f2f8fa84e26f3ce8140c`  
		Last Modified: Thu, 07 Sep 2023 00:46:33 GMT  
		Size: 49.4 MB (49445334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d454ac763c9575efed0bae2752d7cc051d5e358c7b8d844b29544761fd49b489`  
		Last Modified: Thu, 07 Sep 2023 09:43:05 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7040be56146dfb573404e89439f1a5c42b6fc1db8596d6bc56def0d7266380`  
		Last Modified: Thu, 07 Sep 2023 09:43:08 GMT  
		Size: 25.3 MB (25333036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f840420237bd9e60e6820d10249b5d34925acbfaa5fea3de34a6c98bbc2c0d4`  
		Last Modified: Thu, 07 Sep 2023 09:43:06 GMT  
		Size: 866.3 KB (866332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bda2f17df293208d888dda01ad2f1985101f0fbd42e3faf8013531e43c34ad4`  
		Last Modified: Thu, 07 Sep 2023 09:43:05 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de910b53b299ac3a4635a8f6f5c361f449e7e75accd105e1b4ac6f5ef5d2af2`  
		Last Modified: Thu, 07 Sep 2023 09:43:26 GMT  
		Size: 249.8 MB (249823197 bytes)  
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
$ docker pull r-base@sha256:a8764fb36644d7be23147b28659068455571561d50e1a644290b6f03449ba173
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304665343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7da3b6a54d3c4a6cc1b4d9a50e672e482485b61bed78f7a72e4e623606e3f7`
-	Default Command: `["R"]`

```dockerfile
# Thu, 07 Sep 2023 00:46:52 GMT
ADD file:abcf51b81cd6f9cfc93b9963d223d2066f6e087d383af2edcf8f9a577dc23efd in / 
# Thu, 07 Sep 2023 00:46:56 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:40:04 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Thu, 07 Sep 2023 09:40:05 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Thu, 07 Sep 2023 09:40:14 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:40:19 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 07 Sep 2023 09:40:19 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 07 Sep 2023 09:40:19 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Sep 2023 09:40:20 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Thu, 07 Sep 2023 09:40:20 GMT
ENV R_BASE_VERSION=4.3.1
# Thu, 07 Sep 2023 09:41:06 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:41:17 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ee1a4ae1256a1fd777550db8f08b55a9e6e2b2d07e77c364c53343f9f594e95e`  
		Last Modified: Thu, 07 Sep 2023 00:51:44 GMT  
		Size: 48.6 MB (48573786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03025c0e3c889235f049b357ed661eace9c82b7be8a31e98238e7a0b34e095c3`  
		Last Modified: Thu, 07 Sep 2023 09:41:30 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a132777548148b85928877f34abf6850a75a747f64196b930ffd836daf89e3`  
		Last Modified: Thu, 07 Sep 2023 09:41:33 GMT  
		Size: 25.3 MB (25272584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d08035c8849c57c73a3536e4f21777b0b4a5fecf2b17a4f20887f9c2603990`  
		Last Modified: Thu, 07 Sep 2023 09:41:30 GMT  
		Size: 922.3 KB (922279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c17d461902e3ebc69614273386960076f6ddeaa704b78ab71231fb697e9ee7`  
		Last Modified: Thu, 07 Sep 2023 09:41:30 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c65f79fd283303b8a04da44a4d7f225af5be9f62e5aa4ad604f7486be58f5c`  
		Last Modified: Thu, 07 Sep 2023 09:41:54 GMT  
		Size: 229.9 MB (229892984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.3.2`](#r-base432)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.3.2`

```console
$ docker pull r-base@sha256:c2661bdb5077e2f9e17e20f4fae20b8a07fddfdb85a4dcc6661cdc7274172282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:4.3.2` - linux; amd64

```console
$ docker pull r-base@sha256:2031e6723c29ab07ad875d8fba9fa60fb7111357d7268f28393353f64592b13d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340466565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f46bbab0fbf852f4ed6c97604f29bf12a8d38628b51564fbb9739b4922eb7d`
-	Default Command: `["R"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:47 GMT
ADD file:bf1a099790136a24feb4eac287781f4d35a1188036c126be1ae0a93f2e5d2adf in / 
# Tue, 19 Dec 2023 01:22:48 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:10:11 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 19 Dec 2023 04:10:12 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 19 Dec 2023 04:10:22 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:10:25 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 19 Dec 2023 04:10:25 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 19 Dec 2023 04:10:25 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Dec 2023 04:10:26 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 19 Dec 2023 04:10:26 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 19 Dec 2023 04:11:24 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:11:26 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:2be50d1418f669b761525b481330d50356bbd66349941bd0ed8e3c04c64c8ada`  
		Last Modified: Tue, 19 Dec 2023 01:28:59 GMT  
		Size: 49.6 MB (49583409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf17b7b5242934c0aba511f92c02ce16b993fa8fa24cd2cb7f1b51ab89fc8e9e`  
		Last Modified: Tue, 19 Dec 2023 04:11:40 GMT  
		Size: 3.4 KB (3364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba60adf71939a54c86822562d6b19901b0ebfd652e41a20d6675252b0cc8d7a`  
		Last Modified: Tue, 19 Dec 2023 04:11:43 GMT  
		Size: 25.6 MB (25632406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9757002524d9952f68fb0043191a997d58312019ef47810cd22665058fd58fc6`  
		Last Modified: Tue, 19 Dec 2023 04:11:40 GMT  
		Size: 866.3 KB (866326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56b61288bd2707889b0b3c339ee47d610902d88d881008796107e73191ac567`  
		Last Modified: Tue, 19 Dec 2023 04:11:40 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdf2a03cf1508120d7141f70b206b88ec9523a8ed106de16ea450655d87d64b`  
		Last Modified: Tue, 19 Dec 2023 04:12:09 GMT  
		Size: 264.4 MB (264380708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.2` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:247c2dfcb69e5df6f231c6f972d97688c740d015179d4987cda5a2b30323bfdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.1 MB (326069617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3998e890e5bef3fecf4f4e1cb9c78bae1a7d58ed0a8f1f447c9d37b85452ac`
-	Default Command: `["R"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:36 GMT
ADD file:19f717739f7e55ba067aa6bb34df0d612deb5f8c2614311d867f5f6a987beb96 in / 
# Tue, 21 Nov 2023 06:28:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 19:48:34 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 21 Nov 2023 19:48:34 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 21 Nov 2023 19:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:48:45 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 21 Nov 2023 19:48:45 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 21 Nov 2023 19:48:45 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Nov 2023 19:48:46 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 21 Nov 2023 19:48:46 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 21 Nov 2023 19:49:52 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:49:56 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:b331fba2b83cc1c8a6d0cbd20ea0869610ed9049598db306ed9a572e23fbf94d`  
		Last Modified: Tue, 21 Nov 2023 06:34:03 GMT  
		Size: 49.6 MB (49571279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71126464fb3469bb4eea63ccb83b442968e15d0bfcd87e954056602369aee0b7`  
		Last Modified: Tue, 21 Nov 2023 19:50:17 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999ccc115d88ed29e22c40c5c6de7204e4066da0ee6679e29991342c32e497b9`  
		Last Modified: Tue, 21 Nov 2023 19:50:19 GMT  
		Size: 25.4 MB (25361668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10a5e69ff2d37a70c2dcf8c3da9505715edb324f1f3e17766d952c028e52d8b`  
		Last Modified: Tue, 21 Nov 2023 19:50:17 GMT  
		Size: 866.3 KB (866323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd826140ead029f8cafc9fcc7c71d58bd6b04681e99e9650d3f327b5608d074`  
		Last Modified: Tue, 21 Nov 2023 19:50:17 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b10f45d92890a24f7532f4fc280613de000121a0a3ea9d82ad034a975c2eda`  
		Last Modified: Tue, 21 Nov 2023 19:50:48 GMT  
		Size: 250.3 MB (250266636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.2` - linux; ppc64le

```console
$ docker pull r-base@sha256:a84727cdb0bdc7894cc0a89532eab2075bd9eeb172958ecfbc837a3fd6565fe4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339358296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2f554b36886a4b49d4b23bc614377b5aea155cf550ba094f5c7049f51e9416`
-	Default Command: `["R"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:50 GMT
ADD file:ee3cb605ce884e3fd7b604dfca909636e0b59216fe3336f2825e7337ba916a2e in / 
# Tue, 19 Dec 2023 01:23:53 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:07:25 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 19 Dec 2023 06:07:27 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 19 Dec 2023 06:07:44 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:07:47 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 19 Dec 2023 06:07:48 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 19 Dec 2023 06:07:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Dec 2023 06:07:49 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 19 Dec 2023 06:07:49 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 19 Dec 2023 06:09:55 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:10:02 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bc865b325cbd5fad6fb967a293ffe0e52c3003a42cf80fdc316014fe20a7d923`  
		Last Modified: Tue, 19 Dec 2023 01:29:30 GMT  
		Size: 53.5 MB (53476443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31eaabebe967f6cc92629d3e4d14e93764ba1a15334973f43caed87e2876cc`  
		Last Modified: Tue, 19 Dec 2023 06:10:24 GMT  
		Size: 3.4 KB (3364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc4b883673e476c0c19ceb12d43c7eeb82f3f1ca52ac9666cbb9c2522776538`  
		Last Modified: Tue, 19 Dec 2023 06:10:27 GMT  
		Size: 26.0 MB (25959473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ff96b3d00cf9079b2c07f6a1418b62ca236741ec4e8755f7f21f31d58ff18d`  
		Last Modified: Tue, 19 Dec 2023 06:10:24 GMT  
		Size: 866.3 KB (866323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f869163e8d56d7316ef7705b70e7853de8d6ff3cc4c811c3105767cfa6ca77ba`  
		Last Modified: Tue, 19 Dec 2023 06:10:24 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc692e2404781e5fe9bb5e05090597e5bb7eea5a6617e8f6fdbeacb334c5b482`  
		Last Modified: Tue, 19 Dec 2023 06:10:57 GMT  
		Size: 259.1 MB (259052342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.3.2` - linux; s390x

```console
$ docker pull r-base@sha256:8323622cd9df8efc7c0b906b353f38d435b05ff4fe9d77715b7b8ba37d0b97cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.9 MB (306909387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edd3f76f174b99b59e8ebd947e8653c4027574a0a3dcfe21983c31da049a376`
-	Default Command: `["R"]`

```dockerfile
# Tue, 19 Dec 2023 01:44:58 GMT
ADD file:632dc1ca5542f093ca4f7354e6eada70468846f8756116f18fdbaec1eaa91442 in / 
# Tue, 19 Dec 2023 01:45:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 09:51:29 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 19 Dec 2023 09:51:30 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 19 Dec 2023 09:51:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 09:51:41 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 19 Dec 2023 09:51:41 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 19 Dec 2023 09:51:41 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Dec 2023 09:51:42 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 19 Dec 2023 09:51:42 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 19 Dec 2023 09:52:21 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 09:52:31 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:0897e866e45024ee14fbf1277f64a545d81ee7a189397842b04a9438eae6c8f6`  
		Last Modified: Tue, 19 Dec 2023 01:49:30 GMT  
		Size: 49.0 MB (49047746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17068127ebd85008150836380ca38cc8821bac474e88c5b35f826271ae10825c`  
		Last Modified: Tue, 19 Dec 2023 09:52:45 GMT  
		Size: 3.4 KB (3362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e15b8fed9a9b143ed4209f0fab52ba69fbcbd5ceb1a1736ce27518c2f8d54e3`  
		Last Modified: Tue, 19 Dec 2023 09:52:48 GMT  
		Size: 25.4 MB (25392737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b65ce8b8568c14e8edbd616102c5ac5347658fde892e6a2a741d0aab6212af`  
		Last Modified: Tue, 19 Dec 2023 09:52:45 GMT  
		Size: 922.3 KB (922277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf48f527efccbfc6ee2f603baf3ffc7551cd601049dd7dbe7430fde33e1df272`  
		Last Modified: Tue, 19 Dec 2023 09:52:45 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d94f08d7b84c268ea34c43ec9c8de3c6561018d75df892cc375f5bff078e887`  
		Last Modified: Tue, 19 Dec 2023 09:53:09 GMT  
		Size: 231.5 MB (231542916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:c2661bdb5077e2f9e17e20f4fae20b8a07fddfdb85a4dcc6661cdc7274172282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:2031e6723c29ab07ad875d8fba9fa60fb7111357d7268f28393353f64592b13d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340466565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f46bbab0fbf852f4ed6c97604f29bf12a8d38628b51564fbb9739b4922eb7d`
-	Default Command: `["R"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:47 GMT
ADD file:bf1a099790136a24feb4eac287781f4d35a1188036c126be1ae0a93f2e5d2adf in / 
# Tue, 19 Dec 2023 01:22:48 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:10:11 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 19 Dec 2023 04:10:12 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 19 Dec 2023 04:10:22 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:10:25 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 19 Dec 2023 04:10:25 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 19 Dec 2023 04:10:25 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Dec 2023 04:10:26 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 19 Dec 2023 04:10:26 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 19 Dec 2023 04:11:24 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:11:26 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:2be50d1418f669b761525b481330d50356bbd66349941bd0ed8e3c04c64c8ada`  
		Last Modified: Tue, 19 Dec 2023 01:28:59 GMT  
		Size: 49.6 MB (49583409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf17b7b5242934c0aba511f92c02ce16b993fa8fa24cd2cb7f1b51ab89fc8e9e`  
		Last Modified: Tue, 19 Dec 2023 04:11:40 GMT  
		Size: 3.4 KB (3364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba60adf71939a54c86822562d6b19901b0ebfd652e41a20d6675252b0cc8d7a`  
		Last Modified: Tue, 19 Dec 2023 04:11:43 GMT  
		Size: 25.6 MB (25632406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9757002524d9952f68fb0043191a997d58312019ef47810cd22665058fd58fc6`  
		Last Modified: Tue, 19 Dec 2023 04:11:40 GMT  
		Size: 866.3 KB (866326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56b61288bd2707889b0b3c339ee47d610902d88d881008796107e73191ac567`  
		Last Modified: Tue, 19 Dec 2023 04:11:40 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdf2a03cf1508120d7141f70b206b88ec9523a8ed106de16ea450655d87d64b`  
		Last Modified: Tue, 19 Dec 2023 04:12:09 GMT  
		Size: 264.4 MB (264380708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:247c2dfcb69e5df6f231c6f972d97688c740d015179d4987cda5a2b30323bfdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.1 MB (326069617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3998e890e5bef3fecf4f4e1cb9c78bae1a7d58ed0a8f1f447c9d37b85452ac`
-	Default Command: `["R"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:36 GMT
ADD file:19f717739f7e55ba067aa6bb34df0d612deb5f8c2614311d867f5f6a987beb96 in / 
# Tue, 21 Nov 2023 06:28:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 19:48:34 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 21 Nov 2023 19:48:34 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 21 Nov 2023 19:48:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:48:45 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 21 Nov 2023 19:48:45 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 21 Nov 2023 19:48:45 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Nov 2023 19:48:46 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 21 Nov 2023 19:48:46 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 21 Nov 2023 19:49:52 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:49:56 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:b331fba2b83cc1c8a6d0cbd20ea0869610ed9049598db306ed9a572e23fbf94d`  
		Last Modified: Tue, 21 Nov 2023 06:34:03 GMT  
		Size: 49.6 MB (49571279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71126464fb3469bb4eea63ccb83b442968e15d0bfcd87e954056602369aee0b7`  
		Last Modified: Tue, 21 Nov 2023 19:50:17 GMT  
		Size: 3.4 KB (3360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999ccc115d88ed29e22c40c5c6de7204e4066da0ee6679e29991342c32e497b9`  
		Last Modified: Tue, 21 Nov 2023 19:50:19 GMT  
		Size: 25.4 MB (25361668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10a5e69ff2d37a70c2dcf8c3da9505715edb324f1f3e17766d952c028e52d8b`  
		Last Modified: Tue, 21 Nov 2023 19:50:17 GMT  
		Size: 866.3 KB (866323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd826140ead029f8cafc9fcc7c71d58bd6b04681e99e9650d3f327b5608d074`  
		Last Modified: Tue, 21 Nov 2023 19:50:17 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b10f45d92890a24f7532f4fc280613de000121a0a3ea9d82ad034a975c2eda`  
		Last Modified: Tue, 21 Nov 2023 19:50:48 GMT  
		Size: 250.3 MB (250266636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:a84727cdb0bdc7894cc0a89532eab2075bd9eeb172958ecfbc837a3fd6565fe4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339358296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2f554b36886a4b49d4b23bc614377b5aea155cf550ba094f5c7049f51e9416`
-	Default Command: `["R"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:50 GMT
ADD file:ee3cb605ce884e3fd7b604dfca909636e0b59216fe3336f2825e7337ba916a2e in / 
# Tue, 19 Dec 2023 01:23:53 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:07:25 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 19 Dec 2023 06:07:27 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 19 Dec 2023 06:07:44 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:07:47 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 19 Dec 2023 06:07:48 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 19 Dec 2023 06:07:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Dec 2023 06:07:49 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 19 Dec 2023 06:07:49 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 19 Dec 2023 06:09:55 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:10:02 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bc865b325cbd5fad6fb967a293ffe0e52c3003a42cf80fdc316014fe20a7d923`  
		Last Modified: Tue, 19 Dec 2023 01:29:30 GMT  
		Size: 53.5 MB (53476443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31eaabebe967f6cc92629d3e4d14e93764ba1a15334973f43caed87e2876cc`  
		Last Modified: Tue, 19 Dec 2023 06:10:24 GMT  
		Size: 3.4 KB (3364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc4b883673e476c0c19ceb12d43c7eeb82f3f1ca52ac9666cbb9c2522776538`  
		Last Modified: Tue, 19 Dec 2023 06:10:27 GMT  
		Size: 26.0 MB (25959473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ff96b3d00cf9079b2c07f6a1418b62ca236741ec4e8755f7f21f31d58ff18d`  
		Last Modified: Tue, 19 Dec 2023 06:10:24 GMT  
		Size: 866.3 KB (866323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f869163e8d56d7316ef7705b70e7853de8d6ff3cc4c811c3105767cfa6ca77ba`  
		Last Modified: Tue, 19 Dec 2023 06:10:24 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc692e2404781e5fe9bb5e05090597e5bb7eea5a6617e8f6fdbeacb334c5b482`  
		Last Modified: Tue, 19 Dec 2023 06:10:57 GMT  
		Size: 259.1 MB (259052342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:8323622cd9df8efc7c0b906b353f38d435b05ff4fe9d77715b7b8ba37d0b97cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.9 MB (306909387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edd3f76f174b99b59e8ebd947e8653c4027574a0a3dcfe21983c31da049a376`
-	Default Command: `["R"]`

```dockerfile
# Tue, 19 Dec 2023 01:44:58 GMT
ADD file:632dc1ca5542f093ca4f7354e6eada70468846f8756116f18fdbaec1eaa91442 in / 
# Tue, 19 Dec 2023 01:45:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 09:51:29 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 19 Dec 2023 09:51:30 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 19 Dec 2023 09:51:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 09:51:41 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 19 Dec 2023 09:51:41 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 19 Dec 2023 09:51:41 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Dec 2023 09:51:42 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 19 Dec 2023 09:51:42 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 19 Dec 2023 09:52:21 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 09:52:31 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:0897e866e45024ee14fbf1277f64a545d81ee7a189397842b04a9438eae6c8f6`  
		Last Modified: Tue, 19 Dec 2023 01:49:30 GMT  
		Size: 49.0 MB (49047746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17068127ebd85008150836380ca38cc8821bac474e88c5b35f826271ae10825c`  
		Last Modified: Tue, 19 Dec 2023 09:52:45 GMT  
		Size: 3.4 KB (3362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e15b8fed9a9b143ed4209f0fab52ba69fbcbd5ceb1a1736ce27518c2f8d54e3`  
		Last Modified: Tue, 19 Dec 2023 09:52:48 GMT  
		Size: 25.4 MB (25392737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b65ce8b8568c14e8edbd616102c5ac5347658fde892e6a2a741d0aab6212af`  
		Last Modified: Tue, 19 Dec 2023 09:52:45 GMT  
		Size: 922.3 KB (922277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf48f527efccbfc6ee2f603baf3ffc7551cd601049dd7dbe7430fde33e1df272`  
		Last Modified: Tue, 19 Dec 2023 09:52:45 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d94f08d7b84c268ea34c43ec9c8de3c6561018d75df892cc375f5bff078e887`  
		Last Modified: Tue, 19 Dec 2023 09:53:09 GMT  
		Size: 231.5 MB (231542916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

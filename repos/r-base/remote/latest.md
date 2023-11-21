## `r-base:latest`

```console
$ docker pull r-base@sha256:0844dea3ec58326dfe780074966f001c61566f5b54a2d54e4aac06ee70e5faa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:e587849727ad0855cbf919a5137b75d0b27ea90a3b3b11d862d581a597e57fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339706121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51ab79f0adf2f9e672cc2f8f6ae42fb33883df48d80e939eadc2195a5972f3f`
-	Default Command: `["R"]`

```dockerfile
# Tue, 21 Nov 2023 05:23:51 GMT
ADD file:9bf7047d4bc565e7e2cb1baf7275fe6b02fc9e4627e500bb4d7c8cd739a26aae in / 
# Tue, 21 Nov 2023 05:23:51 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 19:49:59 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Tue, 21 Nov 2023 19:50:00 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker
# Tue, 21 Nov 2023 19:50:10 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:50:12 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 21 Nov 2023 19:50:12 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 21 Nov 2023 19:50:13 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Nov 2023 19:50:13 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Tue, 21 Nov 2023 19:50:13 GMT
ENV R_BASE_VERSION=4.3.2
# Tue, 21 Nov 2023 19:51:06 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:51:08 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:786c9ee75a8d6bb4c357dfb6a4cff0b70faa3dd8a36a5024897ebb5c8c6cbba9`  
		Last Modified: Tue, 21 Nov 2023 05:29:45 GMT  
		Size: 49.5 MB (49538803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abf5944b5083a0c580671271699cab00c74f246317e31ec85f267f886f5304d`  
		Last Modified: Tue, 21 Nov 2023 19:51:28 GMT  
		Size: 3.4 KB (3356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1936a419ec91c802ef8611dd485e7008a355a2522a910bb9ec6341e580b45f5e`  
		Last Modified: Tue, 21 Nov 2023 19:51:31 GMT  
		Size: 25.5 MB (25519275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5588a4c2d5f4c9e0e082001f0b9879811afe304b5027bf09166e26111640523`  
		Last Modified: Tue, 21 Nov 2023 19:51:28 GMT  
		Size: 866.3 KB (866326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a3551a86bba8722ce6bcec6b17a41c8ffebde92618af58fe6ae01c44bd0056`  
		Last Modified: Tue, 21 Nov 2023 19:51:28 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bb7b5b91304066c1d3399a85ed026abf276474590098710f0670d6ac6e79e7`  
		Last Modified: Tue, 21 Nov 2023 19:51:56 GMT  
		Size: 263.8 MB (263778012 bytes)  
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

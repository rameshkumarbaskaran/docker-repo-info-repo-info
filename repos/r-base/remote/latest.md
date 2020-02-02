## `r-base:latest`

```console
$ docker pull r-base@sha256:da997d6cfbba979eb2ce490134ef386656452565b8d7aadcb96be0eabb413bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:a536d65e0bd78f167c43ffbe8cd8326a88669db061c0d388b88fc2aa0f8f3098
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294061516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ace8280b3d2ea01a7051ac0d3f800e51e24086763edda10f39222f076a488d`
-	Default Command: `["R"]`

```dockerfile
# Sat, 01 Feb 2020 17:24:12 GMT
ADD file:eefa3f1929486475ead0aa6a9002891b3b05a98556bdd8b07a78536ccb66b2c9 in / 
# Sat, 01 Feb 2020 17:24:12 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:43:35 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Sun, 02 Feb 2020 00:43:36 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Sun, 02 Feb 2020 00:43:46 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 00:43:49 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sun, 02 Feb 2020 00:43:49 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 02 Feb 2020 00:43:50 GMT
ENV LANG=en_US.UTF-8
# Sun, 02 Feb 2020 00:43:50 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Sun, 02 Feb 2020 00:43:50 GMT
ENV R_BASE_VERSION=3.6.2
# Sun, 02 Feb 2020 00:44:36 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 00:44:37 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:7c9fdd8a58ab01cb58d1c1eb32a2f697f78cf9bdaa500ee2c436b7acecd65d44`  
		Last Modified: Sat, 01 Feb 2020 17:29:16 GMT  
		Size: 51.5 MB (51490733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769350f95299066f4db404e7e230484b7a51bda435075db533286c186fd891d1`  
		Last Modified: Sun, 02 Feb 2020 00:44:53 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6f5045cd46d6bc8e22a1055c987884f0af29d0e269eef9ec22b69ed560436b`  
		Last Modified: Sun, 02 Feb 2020 00:44:58 GMT  
		Size: 27.4 MB (27350636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560534ec24b29b913887163602b8150a03d07c73dca2a44cbb40e8fb0db23ce7`  
		Last Modified: Sun, 02 Feb 2020 00:44:53 GMT  
		Size: 862.9 KB (862870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d7337eaaee7c5fdfed6855058b4d1386c2531cc7ee2b930a090523ab3fdfae`  
		Last Modified: Sun, 02 Feb 2020 00:44:53 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5470fe4fdf908dab9b9e1997d4adfe0a329b107a5779fbc3ad0a1039c71d7d34`  
		Last Modified: Sun, 02 Feb 2020 00:45:31 GMT  
		Size: 214.4 MB (214355138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:8f985ffa8981d3c16055ea1ac15073eb39cf454958f1f88d53ea0a35792f4224
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288768952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca81223d44343b97ee164415011716c606405ed621e8d48678c529fb90c6e337`
-	Default Command: `["R"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:54 GMT
ADD file:81bf471be0573ca9cea4a87f30dd2cf8d88ccab02c0ef8b71f5f206e801e43f5 in / 
# Sat, 28 Dec 2019 04:43:59 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 23:40:10 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Sat, 28 Dec 2019 23:40:15 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Sat, 28 Dec 2019 23:40:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 23:40:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sat, 28 Dec 2019 23:40:55 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 28 Dec 2019 23:40:56 GMT
ENV LANG=en_US.UTF-8
# Sat, 28 Dec 2019 23:40:58 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Sat, 28 Dec 2019 23:40:59 GMT
ENV R_BASE_VERSION=3.6.2
# Sat, 28 Dec 2019 23:42:36 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 23:42:42 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:00b2b0ad5b2188255dccb119ffcee55e2ab19bc3badb98bee6de5d94182abbd9`  
		Last Modified: Sat, 28 Dec 2019 04:49:34 GMT  
		Size: 50.3 MB (50319363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef046430894650038844fbb18662de6234de9e15c97f54d027f7279862bdf487`  
		Last Modified: Sat, 28 Dec 2019 23:43:02 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c861daaf5b23bf9384e77340f99db8b7e99a328dfbf2a88c2006d26f262d2`  
		Last Modified: Sat, 28 Dec 2019 23:43:09 GMT  
		Size: 27.2 MB (27219713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c463c2d9e098e378f38a131c0fe591303ae517c93167adf9b083ca41a5c64c34`  
		Last Modified: Sat, 28 Dec 2019 23:43:02 GMT  
		Size: 862.9 KB (862872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0572877cdcbf0995809c0f0295527dbd3b995b4fc2f38badc85ebd12fc804ee3`  
		Last Modified: Sat, 28 Dec 2019 23:43:02 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8991bdb1686d6a3c8a2b8a8f9a066b5903371fb73b2e4cd766c4bc311f87ae0`  
		Last Modified: Sat, 28 Dec 2019 23:43:46 GMT  
		Size: 210.4 MB (210364817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

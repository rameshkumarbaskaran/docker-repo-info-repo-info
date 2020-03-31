<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:3.6.3`](#r-base363)
-	[`r-base:latest`](#r-baselatest)

## `r-base:3.6.3`

```console
$ docker pull r-base@sha256:faa130d8d90649a513db68a325a9ac1750d0212c57ae56468ea88e2ff59da808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `r-base:3.6.3` - linux; amd64

```console
$ docker pull r-base@sha256:f376e70ce4ca16030025ca2948ed481dd4829fa8a5dfb64404154bf5fa4ba5e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298357189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b18c25082fdd0e73ed7a9f288db58af0d8f83f108ecba3f7bd04914a56ce5d`
-	Default Command: `["R"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:24 GMT
ADD file:ef6d0ed43a7e57298514883c056f9c35630c293bcd6a5189ade9a7c839492abf in / 
# Tue, 31 Mar 2020 01:24:24 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:32:41 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 31 Mar 2020 04:32:42 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 31 Mar 2020 04:32:52 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:32:55 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 31 Mar 2020 04:32:55 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 31 Mar 2020 04:32:56 GMT
ENV LANG=en_US.UTF-8
# Tue, 31 Mar 2020 04:32:56 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Tue, 31 Mar 2020 04:32:57 GMT
ENV R_BASE_VERSION=3.6.3
# Tue, 31 Mar 2020 04:34:05 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:34:06 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c551897442bae279f3dc3299b5e89627f556d06912d81bd777e18eb066414c32`  
		Last Modified: Tue, 31 Mar 2020 01:29:45 GMT  
		Size: 51.9 MB (51922694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4159dc113650861209ddf42e53425f0521f9bf4f93549e21215efeb696b8d3e5`  
		Last Modified: Tue, 31 Mar 2020 04:34:14 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c34992aa62704c0b9c0cf2428a9ef639b77183a7e53a3b3768704e9585a0dd8`  
		Last Modified: Tue, 31 Mar 2020 04:34:23 GMT  
		Size: 27.3 MB (27294295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1280af9307bb541416f3f0e838ce99e07acd236c8e9ba897909caf3d3bed1f74`  
		Last Modified: Tue, 31 Mar 2020 04:34:15 GMT  
		Size: 863.4 KB (863394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5416fbde85630b1724eed292ae9d519e7123aac0bb27d54a47cd03d7080c9c0`  
		Last Modified: Tue, 31 Mar 2020 04:34:14 GMT  
		Size: 295.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58958fe491e18cb33a0551fb26186449a038987d8eba4e45c3f450239541692d`  
		Last Modified: Tue, 31 Mar 2020 04:35:04 GMT  
		Size: 218.3 MB (218274668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:3.6.3` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:4f3e287da29432527891a729234da31efca3621a3f8e6e1e1df073f684dd710b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (288040675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0fdfac65ea0b0f0853fe47f5d6b87813eeff7ea4d8bdbc53855ee0d6c15194`
-	Default Command: `["R"]`

```dockerfile
# Tue, 31 Mar 2020 02:09:03 GMT
ADD file:bc1f805aa9a29690e572913287441bb951b8906746724af8b91242eb4d61ce6f in / 
# Tue, 31 Mar 2020 02:09:07 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 06:23:20 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 31 Mar 2020 06:23:24 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 31 Mar 2020 06:23:44 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 06:23:52 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 31 Mar 2020 06:23:53 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 31 Mar 2020 06:23:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 31 Mar 2020 06:23:55 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Tue, 31 Mar 2020 06:23:56 GMT
ENV R_BASE_VERSION=3.6.3
# Tue, 31 Mar 2020 06:25:47 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 06:25:56 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:83486a75c02795f350f5cf9f87dd8ff5c602a68ce117775785d6344f3ed716a7`  
		Last Modified: Tue, 31 Mar 2020 02:14:57 GMT  
		Size: 50.9 MB (50858609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad094b8e72c5164f3f8f88884ce679d5276849796707e1d6b14629d9c309914d`  
		Last Modified: Tue, 31 Mar 2020 06:26:11 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4b83f7ff7ccba888b727e119b5cf5c5ce40bb21dddd894bac69358ecae1535`  
		Last Modified: Tue, 31 Mar 2020 06:26:16 GMT  
		Size: 27.2 MB (27166899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53de7ddf7be16ae941ef98ca95e8986774ed0dbe12e48b99fbbeffcd11bc474`  
		Last Modified: Tue, 31 Mar 2020 06:26:11 GMT  
		Size: 863.4 KB (863395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d009e5d58f42ad0c00fc1feeacf764219c773a65d62f4cae1078616bb7428df0`  
		Last Modified: Tue, 31 Mar 2020 06:26:11 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2b2529b64188a294cdd82cc3ee1b1a1666204bda5c24babe3a6a7d940500c9`  
		Last Modified: Tue, 31 Mar 2020 06:26:56 GMT  
		Size: 209.1 MB (209149595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:faa130d8d90649a513db68a325a9ac1750d0212c57ae56468ea88e2ff59da808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:f376e70ce4ca16030025ca2948ed481dd4829fa8a5dfb64404154bf5fa4ba5e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298357189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b18c25082fdd0e73ed7a9f288db58af0d8f83f108ecba3f7bd04914a56ce5d`
-	Default Command: `["R"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:24 GMT
ADD file:ef6d0ed43a7e57298514883c056f9c35630c293bcd6a5189ade9a7c839492abf in / 
# Tue, 31 Mar 2020 01:24:24 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:32:41 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 31 Mar 2020 04:32:42 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 31 Mar 2020 04:32:52 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:32:55 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 31 Mar 2020 04:32:55 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 31 Mar 2020 04:32:56 GMT
ENV LANG=en_US.UTF-8
# Tue, 31 Mar 2020 04:32:56 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Tue, 31 Mar 2020 04:32:57 GMT
ENV R_BASE_VERSION=3.6.3
# Tue, 31 Mar 2020 04:34:05 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:34:06 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c551897442bae279f3dc3299b5e89627f556d06912d81bd777e18eb066414c32`  
		Last Modified: Tue, 31 Mar 2020 01:29:45 GMT  
		Size: 51.9 MB (51922694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4159dc113650861209ddf42e53425f0521f9bf4f93549e21215efeb696b8d3e5`  
		Last Modified: Tue, 31 Mar 2020 04:34:14 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c34992aa62704c0b9c0cf2428a9ef639b77183a7e53a3b3768704e9585a0dd8`  
		Last Modified: Tue, 31 Mar 2020 04:34:23 GMT  
		Size: 27.3 MB (27294295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1280af9307bb541416f3f0e838ce99e07acd236c8e9ba897909caf3d3bed1f74`  
		Last Modified: Tue, 31 Mar 2020 04:34:15 GMT  
		Size: 863.4 KB (863394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5416fbde85630b1724eed292ae9d519e7123aac0bb27d54a47cd03d7080c9c0`  
		Last Modified: Tue, 31 Mar 2020 04:34:14 GMT  
		Size: 295.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58958fe491e18cb33a0551fb26186449a038987d8eba4e45c3f450239541692d`  
		Last Modified: Tue, 31 Mar 2020 04:35:04 GMT  
		Size: 218.3 MB (218274668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:4f3e287da29432527891a729234da31efca3621a3f8e6e1e1df073f684dd710b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (288040675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0fdfac65ea0b0f0853fe47f5d6b87813eeff7ea4d8bdbc53855ee0d6c15194`
-	Default Command: `["R"]`

```dockerfile
# Tue, 31 Mar 2020 02:09:03 GMT
ADD file:bc1f805aa9a29690e572913287441bb951b8906746724af8b91242eb4d61ce6f in / 
# Tue, 31 Mar 2020 02:09:07 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 06:23:20 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 31 Mar 2020 06:23:24 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 31 Mar 2020 06:23:44 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 06:23:52 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 31 Mar 2020 06:23:53 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 31 Mar 2020 06:23:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 31 Mar 2020 06:23:55 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Tue, 31 Mar 2020 06:23:56 GMT
ENV R_BASE_VERSION=3.6.3
# Tue, 31 Mar 2020 06:25:47 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 06:25:56 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:83486a75c02795f350f5cf9f87dd8ff5c602a68ce117775785d6344f3ed716a7`  
		Last Modified: Tue, 31 Mar 2020 02:14:57 GMT  
		Size: 50.9 MB (50858609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad094b8e72c5164f3f8f88884ce679d5276849796707e1d6b14629d9c309914d`  
		Last Modified: Tue, 31 Mar 2020 06:26:11 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4b83f7ff7ccba888b727e119b5cf5c5ce40bb21dddd894bac69358ecae1535`  
		Last Modified: Tue, 31 Mar 2020 06:26:16 GMT  
		Size: 27.2 MB (27166899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53de7ddf7be16ae941ef98ca95e8986774ed0dbe12e48b99fbbeffcd11bc474`  
		Last Modified: Tue, 31 Mar 2020 06:26:11 GMT  
		Size: 863.4 KB (863395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d009e5d58f42ad0c00fc1feeacf764219c773a65d62f4cae1078616bb7428df0`  
		Last Modified: Tue, 31 Mar 2020 06:26:11 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2b2529b64188a294cdd82cc3ee1b1a1666204bda5c24babe3a6a7d940500c9`  
		Last Modified: Tue, 31 Mar 2020 06:26:56 GMT  
		Size: 209.1 MB (209149595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

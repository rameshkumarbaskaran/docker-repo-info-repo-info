## `r-base:latest`

```console
$ docker pull r-base@sha256:2cf7f581093201f60c84fd9229f63ca08927de45d51294a0cae25f314d99eec4
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
$ docker pull r-base@sha256:a52d90f395cc0a06fa58dc29cab796b9dbf77cf7ac02327805e6fc866c06ef2a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286284608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5539466a3046cce5ff87feb750088e4ff7a9e466b2cf998507db5ae4d87802fb`
-	Default Command: `["R"]`

```dockerfile
# Wed, 26 Feb 2020 00:51:35 GMT
ADD file:e032e27e8935ad66dc76d8dd15bdf9fb36fcc0318c7e322fcdae2ee219c11b61 in / 
# Wed, 26 Feb 2020 00:51:42 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 14:50:40 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 26 Feb 2020 14:50:45 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 26 Feb 2020 14:51:13 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:51:22 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 26 Feb 2020 14:51:24 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 26 Feb 2020 14:51:25 GMT
ENV LANG=en_US.UTF-8
# Wed, 26 Feb 2020 14:51:28 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Wed, 26 Feb 2020 14:51:29 GMT
ENV R_BASE_VERSION=3.6.2
# Wed, 26 Feb 2020 14:53:27 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:53:32 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:c55f06ecbc45a6b3fd4dcd737b73d5b6baa8545548d0610d133fad7fbb7be09e`  
		Last Modified: Wed, 26 Feb 2020 00:59:19 GMT  
		Size: 50.8 MB (50808498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7aa40081a4c3acb54721ed8af71d9d8b92228a4f62dfb4f98151de81d7e11c8`  
		Last Modified: Wed, 26 Feb 2020 14:53:44 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd25a08d3e01c623cda4e3d1ef09fcd60d55ac12b8cdb6ef3b91e1965b2fb4e`  
		Last Modified: Wed, 26 Feb 2020 14:53:50 GMT  
		Size: 27.2 MB (27227086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bcd97dd1ca4be9976e01ac68037d0e11521e394d53544c3c158e4275af2754`  
		Last Modified: Wed, 26 Feb 2020 14:53:44 GMT  
		Size: 862.9 KB (862866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161edfc7e36fd4c7de2c2a209076952456b6a85288218f171c1b4dd7c43480a9`  
		Last Modified: Wed, 26 Feb 2020 14:53:44 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dc28d0921b9d508d58a3b2f664df7810e92631e2795fe82964055f1eb6009e`  
		Last Modified: Wed, 26 Feb 2020 14:54:35 GMT  
		Size: 207.4 MB (207383974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

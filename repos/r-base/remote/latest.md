## `r-base:latest`

```console
$ docker pull r-base@sha256:ddc1143b05f9b5694418f368d199ad576e048b148eb42de9db99cfcecce834e3
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
$ docker pull r-base@sha256:9ce4ca95929c5533c423ad14204f6ada168e0403accf50501aa25ea6c1b9a7ea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284522601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684b2d4227505d65e42d513327a51a23af17f90072865b7fe2984f3bd8b4d08d`
-	Default Command: `["R"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:35 GMT
ADD file:db821559bc10f9e72e5927bea485644dbba15b9be5d035d29e74ff74c90eaebc in / 
# Sat, 01 Feb 2020 16:43:37 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 07:38:45 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Sun, 02 Feb 2020 07:38:51 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Sun, 02 Feb 2020 07:39:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:39:20 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Sun, 02 Feb 2020 07:39:21 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 02 Feb 2020 07:39:22 GMT
ENV LANG=en_US.UTF-8
# Sun, 02 Feb 2020 07:39:23 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Sun, 02 Feb 2020 07:39:24 GMT
ENV R_BASE_VERSION=3.6.2
# Sun, 02 Feb 2020 07:41:08 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 07:41:12 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:6a8ea3b8ec391d7f13575570e7881031715ff8ef67e1224726395e166f3c9ea7`  
		Last Modified: Sat, 01 Feb 2020 16:49:35 GMT  
		Size: 50.5 MB (50453000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937ccc48732c862439ec98f95b86327fca053393a67a4375c4da4319f34e9d59`  
		Last Modified: Sun, 02 Feb 2020 07:41:33 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a566ed03d85d132ecf54ad11e97a33c8f215ac41e762a20ce8d40a87fd3f5008`  
		Last Modified: Sun, 02 Feb 2020 07:41:40 GMT  
		Size: 27.2 MB (27224303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca43e9a7e5f5757199951c5f18ee3f9a7c69cf64614a03762d010f9132a25ce1`  
		Last Modified: Sun, 02 Feb 2020 07:41:33 GMT  
		Size: 862.9 KB (862870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5010da7d0b1ac5d47b267161e3a7de1d521cdaeae587e1c66d10141cd35fba`  
		Last Modified: Sun, 02 Feb 2020 07:41:34 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b7f6a8a4192dde0c1171ceb44e5be53604f917bd114c96c0fa689155c099d2`  
		Last Modified: Sun, 02 Feb 2020 07:42:19 GMT  
		Size: 206.0 MB (205980242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

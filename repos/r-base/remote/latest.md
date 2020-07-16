## `r-base:latest`

```console
$ docker pull r-base@sha256:bc6c9c3364bf303d53ca8389ee480a2c832204ddf1cb7ffe21ba18bdeb38c9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:8751b59dc7966aa6c7c355c6b07252aa12f5636c8d5db37fad21fd45624203dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340906923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194fa228510e6d248a25ddcbb2b2b543f611fa70468d3e789c2084eb09bb7a75`
-	Default Command: `["R"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:49 GMT
ADD file:63ef8f38bb25d9c0e944d04e91b6d6c6eb32289709829d3bb80998e94ff2a506 in / 
# Tue, 09 Jun 2020 01:23:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 16:53:26 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 09 Jun 2020 16:53:26 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 15 Jul 2020 23:47:34 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		ed 		fonts-texgyre 		less 		locales 		vim-tiny 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 15 Jul 2020 23:47:37 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 15 Jul 2020 23:47:37 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 15 Jul 2020 23:47:37 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jul 2020 23:47:38 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Wed, 15 Jul 2020 23:47:38 GMT
ENV R_BASE_VERSION=4.0.2
# Wed, 15 Jul 2020 23:48:36 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/build.r /usr/local/bin/build.r 	&& ln -s /usr/lib/R/site-library/littler/examples/check.r /usr/local/bin/check.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 15 Jul 2020 23:48:37 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:0ab9185ddfe50c951de582032c5e29e21a851a328056e6bee6299e0ff55ec807`  
		Last Modified: Tue, 09 Jun 2020 01:28:27 GMT  
		Size: 51.4 MB (51413498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe522cb8773f50b648207a771978f0815a06186e0161550134a9f1d0de90b7c`  
		Last Modified: Tue, 09 Jun 2020 16:54:45 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069212e018184ddd5b74b2137ab23d302e83c725182c1da2955dee62680d3c78`  
		Last Modified: Wed, 15 Jul 2020 23:48:47 GMT  
		Size: 27.3 MB (27340271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db88dffe9e04558a8fb5898d95e78f81df8390947e51fda7a116ef982417a6dc`  
		Last Modified: Wed, 15 Jul 2020 23:48:44 GMT  
		Size: 863.4 KB (863395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b1afaf74edb234aeae4223811bf0b68bad024d564a6935f22308360db58da1`  
		Last Modified: Wed, 15 Jul 2020 23:48:44 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deb4ced7b0ad435119b70aa777081647a76588e5b2074f03d3c52adb8cca3f6`  
		Last Modified: Wed, 15 Jul 2020 23:49:19 GMT  
		Size: 261.3 MB (261287620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:860d312644fe79ce4dd2cf058763413b83b0da6b390bd1a20aa28fcbfda210fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.8 MB (317841669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef917feb9965c4b32ee04a830dc14844bd5e310de732dd9f241c535d719bc39`
-	Default Command: `["R"]`

```dockerfile
# Tue, 09 Jun 2020 01:55:08 GMT
ADD file:3705d77b7f9ddcac964099514289de1ff74f3618435e1c0846d112f5075abfae in / 
# Tue, 09 Jun 2020 01:55:11 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:21:22 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Tue, 09 Jun 2020 04:21:25 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 15 Jul 2020 23:32:25 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		ed 		fonts-texgyre 		less 		locales 		vim-tiny 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 15 Jul 2020 23:32:31 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 15 Jul 2020 23:32:31 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 15 Jul 2020 23:32:32 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jul 2020 23:32:34 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Wed, 15 Jul 2020 23:32:35 GMT
ENV R_BASE_VERSION=4.0.2
# Wed, 15 Jul 2020 23:35:23 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/build.r /usr/local/bin/build.r 	&& ln -s /usr/lib/R/site-library/littler/examples/check.r /usr/local/bin/check.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 15 Jul 2020 23:35:28 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a2b4880979f186e2b0fb3aceb4435b72654989a46906ae64e190d06c969f2926`  
		Last Modified: Tue, 09 Jun 2020 02:00:48 GMT  
		Size: 50.4 MB (50353822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783b3c4723c1792fe2ea047df23720951cdd4586b19f8756a99ea66454d2c4e`  
		Last Modified: Tue, 09 Jun 2020 04:24:03 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4320fda5f8ed11c79249a0de88acc7eb6ce64b9df0c30df7a2a3e4d4c49481bb`  
		Last Modified: Wed, 15 Jul 2020 23:35:47 GMT  
		Size: 27.2 MB (27205999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30285bc00f7d146b4b785891efddfe61cd802635f7c72c6f7ea221144cd0cd34`  
		Last Modified: Wed, 15 Jul 2020 23:35:41 GMT  
		Size: 863.4 KB (863391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6528af4ba0cfb8f512f9e554391a187bc6f6db412ab8bf1b1d7416fc551b9149`  
		Last Modified: Wed, 15 Jul 2020 23:35:41 GMT  
		Size: 299.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd41b89e7d4e903ed6ad00b120d1efd54996f45cac7a71a4bc9d0433c81d7d`  
		Last Modified: Wed, 15 Jul 2020 23:36:31 GMT  
		Size: 239.4 MB (239416281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:ceea1a55fdb014def8a7d2169928d869b2fb93d13b61ba049b173319119ece15
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338899679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a854bfd4d54464c22b17f6e005a3fc28d8ccb4400985c9d2b222f9796ec8659a`
-	Default Command: `["R"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:56 GMT
ADD file:72fcd44a3cd61718c43b8fd4856b710ec66a4c58ddc118863a85dfa8016f5c8c in / 
# Tue, 09 Jun 2020 01:26:00 GMT
CMD ["bash"]
# Thu, 16 Jul 2020 00:59:03 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Thu, 16 Jul 2020 00:59:24 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Thu, 16 Jul 2020 01:01:29 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		ed 		fonts-texgyre 		less 		locales 		vim-tiny 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jul 2020 01:01:46 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Thu, 16 Jul 2020 01:01:51 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 16 Jul 2020 01:01:56 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Jul 2020 01:02:05 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Thu, 16 Jul 2020 01:02:07 GMT
ENV R_BASE_VERSION=4.0.2
# Thu, 16 Jul 2020 01:16:46 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/build.r /usr/local/bin/build.r 	&& ln -s /usr/lib/R/site-library/littler/examples/check.r /usr/local/bin/check.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jul 2020 01:17:08 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:9ff154698924dfd0c8d74f3ad2e91d17dd68ef0c5b54849d3f7241b9df7886b5`  
		Last Modified: Tue, 09 Jun 2020 01:38:19 GMT  
		Size: 55.1 MB (55148002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f7a9bfdc7701ae1d19b15ef2ce2b2b9164f9f6bfa2ff911b744c419abb7a9b`  
		Last Modified: Thu, 16 Jul 2020 01:17:31 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2401f8461ec5cb1b8937f2769e416e4a0f3545ceaee4eaeee8d896871866685f`  
		Last Modified: Thu, 16 Jul 2020 01:17:40 GMT  
		Size: 27.6 MB (27615577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e8e392599980ec5358bfa12518998fe9e9224311a389e32403f1e55a0d5e7`  
		Last Modified: Thu, 16 Jul 2020 01:17:31 GMT  
		Size: 863.4 KB (863389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcb8c62bf0d215aa351ed32f7f5cb16d3847ecae7b57de3b0cf18a2a8b99eb6`  
		Last Modified: Thu, 16 Jul 2020 01:17:31 GMT  
		Size: 299.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486cd660a376eb9880d609029e04aa36fa2154d30609741e594aee6ecd76ad0a`  
		Last Modified: Thu, 16 Jul 2020 01:18:14 GMT  
		Size: 255.3 MB (255270511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:544384846abe657672f041d8b8c23142c2ffc244280f032a449f6cc3a1caedb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:6d054041921fc1e70dec78463c20a48b47240e382b16944dcd5ede53bdc649cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (297034855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aad1ffccc5335d7c49365e051ed02ec7551d4ebe95250f890e24804198853c0`
-	Default Command: `["R"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:54 GMT
ADD file:bf9b71c3da178fa1ba282c110853082e94e9f8a90773b43b6104bdb8c9e54f5a in / 
# Wed, 26 Feb 2020 00:41:54 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 17:58:31 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 26 Feb 2020 17:58:33 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 26 Feb 2020 17:58:55 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 17:59:00 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 26 Feb 2020 17:59:00 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 26 Feb 2020 17:59:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 26 Feb 2020 17:59:02 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Tue, 03 Mar 2020 00:24:34 GMT
ENV R_BASE_VERSION=3.6.3
# Tue, 03 Mar 2020 00:25:53 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 03 Mar 2020 00:25:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1fcd5305bc72cb154c6bf3d1a204b8bcfc0d91d4811e6681dd2b7aafdaaa8669`  
		Last Modified: Wed, 26 Feb 2020 00:47:41 GMT  
		Size: 51.9 MB (51852708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11dae79a979ed78d9ab050337efd0a70e97e541a58aca4a9ef4decd0f444bd26`  
		Last Modified: Wed, 26 Feb 2020 18:00:18 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb692405f4d99a70dcd1dd32a1e0f61045fa501ed9a1bc7c42ca1ee1273f52b`  
		Last Modified: Wed, 26 Feb 2020 18:00:23 GMT  
		Size: 27.4 MB (27351738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9280d4f7544d4a121297722e320f2a93e71a8d793194a81be9578fd9e1452383`  
		Last Modified: Wed, 26 Feb 2020 18:00:19 GMT  
		Size: 862.9 KB (862861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab66f892f181dfa4664981ea04e0c6d793050629bf32a7aa1b9426cdec37458d`  
		Last Modified: Wed, 26 Feb 2020 18:00:19 GMT  
		Size: 295.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5681dea11ec5ec2cb2c64229df7915ccc86753c61c81d496b0ad4102f8a9e4a`  
		Last Modified: Tue, 03 Mar 2020 00:26:36 GMT  
		Size: 217.0 MB (216965409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:dd0b586f7e1b84b0aa847e8f3d4f46f7618f2b7577103fd8fb2513172c963d38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287331272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8238920874c204f0b4d240a32b900010ecd1acfc6e67a73ce0dee66482ce1b`
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
# Tue, 03 Mar 2020 00:43:01 GMT
ENV R_BASE_VERSION=3.6.3
# Tue, 03 Mar 2020 00:44:58 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 03 Mar 2020 00:45:01 GMT
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
	-	`sha256:6fac50520fee20a4e6dae3924bc1d109df256a0884d098538528145f6909d2c1`  
		Last Modified: Tue, 03 Mar 2020 00:46:03 GMT  
		Size: 208.4 MB (208430638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:4.0.2`](#r-base402)
-	[`r-base:latest`](#r-baselatest)

## `r-base:4.0.2`

```console
$ docker pull r-base@sha256:e292b19eb361d5494ee5eab580db3dc11f1ecb59200c1bc1625f81e78a67410b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `r-base:4.0.2` - linux; amd64

```console
$ docker pull r-base@sha256:8920791e1dab8259d9b7a6372591f010ceeffce0e52bd103329f4932047c7ad7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333491833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d984908c70c0a24d92ff092ab1d5e61787ea6667d1daa34e33b644a01a466d75`
-	Default Command: `["R"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:27 GMT
ADD file:f87e67a50d51914c2d4d77ad9fb2395ec8f720b21958111ea5e493ea7b788d12 in / 
# Wed, 22 Jul 2020 02:07:27 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:01:57 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 22 Jul 2020 22:01:58 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 22 Jul 2020 22:02:11 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		ed 		fonts-texgyre 		less 		locales 		vim-tiny 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:02:14 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 22 Jul 2020 22:02:14 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 22 Jul 2020 22:02:14 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 Jul 2020 22:02:15 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Wed, 22 Jul 2020 22:02:15 GMT
ENV R_BASE_VERSION=4.0.2
# Wed, 22 Jul 2020 22:03:11 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/build.r /usr/local/bin/build.r 	&& ln -s /usr/lib/R/site-library/littler/examples/check.r /usr/local/bin/check.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:03:11 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:73b408cb748b0d1dd55d6ee6f4be6beddeeaefef08a2f1733d219cfa7c8eaf22`  
		Last Modified: Wed, 22 Jul 2020 02:12:41 GMT  
		Size: 54.1 MB (54102525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5216627df1d485b31150331d070eaf109fdb7487e2514d507a96e83d1ef2d6bb`  
		Last Modified: Wed, 22 Jul 2020 22:03:31 GMT  
		Size: 1.9 KB (1853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5233fa73a943546017946412cf9bc1f586bafb8efdcabeaf29fdc131fa93d19b`  
		Last Modified: Wed, 22 Jul 2020 22:03:36 GMT  
		Size: 32.6 MB (32639318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224d21aef6e2255d00febc18891d4a3ed3a7f15c091bc3017946bc1cad92973d`  
		Last Modified: Wed, 22 Jul 2020 22:03:31 GMT  
		Size: 863.6 KB (863571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3491ee7b75dcd62a391486d825ee8071cf9614ccf00fb4cfe46153e845d3bfb`  
		Last Modified: Wed, 22 Jul 2020 22:03:31 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd8bc235aa1a7f6117c92d18ab29e6019a99fe2190eaf42f6b78fe6c17a2220`  
		Last Modified: Wed, 22 Jul 2020 22:04:12 GMT  
		Size: 245.9 MB (245884272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.0.2` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:956edd2e7edf713f023775e2707025db06556410996d7debb7b9acce1d2304c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 MB (311799691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cecb44eeb8e9decfdbd36e89c22bc4f9d1934ff5e8bd863a71bc4cf77e181b`
-	Default Command: `["R"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:29 GMT
ADD file:a9b119b35a33d56fcb58f91ca0224992754db12e0d3b07747c62963bc14659c8 in / 
# Wed, 22 Jul 2020 00:44:32 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:19:51 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 22 Jul 2020 18:20:06 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 22 Jul 2020 18:21:26 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		ed 		fonts-texgyre 		less 		locales 		vim-tiny 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:21:52 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 22 Jul 2020 18:22:00 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 22 Jul 2020 18:22:05 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 Jul 2020 18:22:11 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Wed, 22 Jul 2020 18:22:12 GMT
ENV R_BASE_VERSION=4.0.2
# Wed, 22 Jul 2020 18:24:09 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/build.r /usr/local/bin/build.r 	&& ln -s /usr/lib/R/site-library/littler/examples/check.r /usr/local/bin/check.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:24:16 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:3bd06a7da77e986d495b6461507cdfdd810e88d105914958d9602ec1c748e59c`  
		Last Modified: Wed, 22 Jul 2020 00:50:38 GMT  
		Size: 52.9 MB (52886390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fd899cc707d5e31d413ecf9244e96b6df4cd08d368c5a1073357064a989497`  
		Last Modified: Wed, 22 Jul 2020 18:24:28 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753a01faf8cb37ede96c30ca8bd066325e7fa69ccecf842cf2949238514d814e`  
		Last Modified: Wed, 22 Jul 2020 18:24:38 GMT  
		Size: 31.8 MB (31810242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f65e5f40237135eb0dc1ecbca05b0ad9e996547a54645dbf2c1f224e177ee2`  
		Last Modified: Wed, 22 Jul 2020 18:24:28 GMT  
		Size: 863.6 KB (863577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b461ec2eec3b5affd95277495804497a9d37e03a8561572308599999416d5f`  
		Last Modified: Wed, 22 Jul 2020 18:24:28 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4935880f04a2f54a0851bb9c16a7b44807a6f0238e199a0eac80ab6575eee24`  
		Last Modified: Wed, 22 Jul 2020 18:25:28 GMT  
		Size: 226.2 MB (226237296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:4.0.2` - linux; ppc64le

```console
$ docker pull r-base@sha256:8053db17f111e35f91dc18fa95ed7a9e90d8cf75798367009a2f0ca9c1ba125c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.7 MB (328668535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2050051c720747171cdd515df23ce0d8352c44f3b8d9469f6e2df0407f309b96`
-	Default Command: `["R"]`

```dockerfile
# Wed, 22 Jul 2020 02:18:37 GMT
ADD file:d6f4416408e160284a3c90cab6e53a951dbbc7c1dfa4811f000212296eba31d7 in / 
# Wed, 22 Jul 2020 02:18:43 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 16:36:54 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 22 Jul 2020 16:37:04 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 22 Jul 2020 16:40:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		ed 		fonts-texgyre 		less 		locales 		vim-tiny 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 16:40:19 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 22 Jul 2020 16:40:23 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 22 Jul 2020 16:40:27 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 Jul 2020 16:40:45 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Wed, 22 Jul 2020 16:40:52 GMT
ENV R_BASE_VERSION=4.0.2
# Wed, 22 Jul 2020 16:49:08 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/build.r /usr/local/bin/build.r 	&& ln -s /usr/lib/R/site-library/littler/examples/check.r /usr/local/bin/check.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 16:49:25 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1e364755122e5010d03f3981d981af0aa16507fb01fdd2c15d80db1a963b580f`  
		Last Modified: Wed, 22 Jul 2020 02:31:33 GMT  
		Size: 58.0 MB (57953376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feef8a33b4b62328cdb97c472c74451134599e5d747e71a852c4a8de0efb9c0d`  
		Last Modified: Wed, 22 Jul 2020 16:49:49 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf961d0022aa866c60a9f344c7471db43ffc2be326be68fa7dc4485340e0cdcf`  
		Last Modified: Wed, 22 Jul 2020 16:49:54 GMT  
		Size: 33.8 MB (33769704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbbb5f2890145f505886efac8b220b1bc027cdcc2209919c53965e75af5cd11`  
		Last Modified: Wed, 22 Jul 2020 16:49:49 GMT  
		Size: 863.6 KB (863574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce397ad821652ca80c5024156ab489bb9be2c3c4d44a687d92a5401f890dc8d1`  
		Last Modified: Wed, 22 Jul 2020 16:49:49 GMT  
		Size: 299.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f5f384a1a66f8977f3f739478739be2d29317f8b4f9435cffa8f241c9c95f0`  
		Last Modified: Wed, 22 Jul 2020 16:50:34 GMT  
		Size: 236.1 MB (236079698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:e292b19eb361d5494ee5eab580db3dc11f1ecb59200c1bc1625f81e78a67410b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:8920791e1dab8259d9b7a6372591f010ceeffce0e52bd103329f4932047c7ad7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333491833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d984908c70c0a24d92ff092ab1d5e61787ea6667d1daa34e33b644a01a466d75`
-	Default Command: `["R"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:27 GMT
ADD file:f87e67a50d51914c2d4d77ad9fb2395ec8f720b21958111ea5e493ea7b788d12 in / 
# Wed, 22 Jul 2020 02:07:27 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:01:57 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 22 Jul 2020 22:01:58 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 22 Jul 2020 22:02:11 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		ed 		fonts-texgyre 		less 		locales 		vim-tiny 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:02:14 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 22 Jul 2020 22:02:14 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 22 Jul 2020 22:02:14 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 Jul 2020 22:02:15 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Wed, 22 Jul 2020 22:02:15 GMT
ENV R_BASE_VERSION=4.0.2
# Wed, 22 Jul 2020 22:03:11 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/build.r /usr/local/bin/build.r 	&& ln -s /usr/lib/R/site-library/littler/examples/check.r /usr/local/bin/check.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:03:11 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:73b408cb748b0d1dd55d6ee6f4be6beddeeaefef08a2f1733d219cfa7c8eaf22`  
		Last Modified: Wed, 22 Jul 2020 02:12:41 GMT  
		Size: 54.1 MB (54102525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5216627df1d485b31150331d070eaf109fdb7487e2514d507a96e83d1ef2d6bb`  
		Last Modified: Wed, 22 Jul 2020 22:03:31 GMT  
		Size: 1.9 KB (1853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5233fa73a943546017946412cf9bc1f586bafb8efdcabeaf29fdc131fa93d19b`  
		Last Modified: Wed, 22 Jul 2020 22:03:36 GMT  
		Size: 32.6 MB (32639318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224d21aef6e2255d00febc18891d4a3ed3a7f15c091bc3017946bc1cad92973d`  
		Last Modified: Wed, 22 Jul 2020 22:03:31 GMT  
		Size: 863.6 KB (863571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3491ee7b75dcd62a391486d825ee8071cf9614ccf00fb4cfe46153e845d3bfb`  
		Last Modified: Wed, 22 Jul 2020 22:03:31 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd8bc235aa1a7f6117c92d18ab29e6019a99fe2190eaf42f6b78fe6c17a2220`  
		Last Modified: Wed, 22 Jul 2020 22:04:12 GMT  
		Size: 245.9 MB (245884272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:956edd2e7edf713f023775e2707025db06556410996d7debb7b9acce1d2304c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 MB (311799691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cecb44eeb8e9decfdbd36e89c22bc4f9d1934ff5e8bd863a71bc4cf77e181b`
-	Default Command: `["R"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:29 GMT
ADD file:a9b119b35a33d56fcb58f91ca0224992754db12e0d3b07747c62963bc14659c8 in / 
# Wed, 22 Jul 2020 00:44:32 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 18:19:51 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 22 Jul 2020 18:20:06 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 22 Jul 2020 18:21:26 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		ed 		fonts-texgyre 		less 		locales 		vim-tiny 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:21:52 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 22 Jul 2020 18:22:00 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 22 Jul 2020 18:22:05 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 Jul 2020 18:22:11 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Wed, 22 Jul 2020 18:22:12 GMT
ENV R_BASE_VERSION=4.0.2
# Wed, 22 Jul 2020 18:24:09 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/build.r /usr/local/bin/build.r 	&& ln -s /usr/lib/R/site-library/littler/examples/check.r /usr/local/bin/check.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:24:16 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:3bd06a7da77e986d495b6461507cdfdd810e88d105914958d9602ec1c748e59c`  
		Last Modified: Wed, 22 Jul 2020 00:50:38 GMT  
		Size: 52.9 MB (52886390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fd899cc707d5e31d413ecf9244e96b6df4cd08d368c5a1073357064a989497`  
		Last Modified: Wed, 22 Jul 2020 18:24:28 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753a01faf8cb37ede96c30ca8bd066325e7fa69ccecf842cf2949238514d814e`  
		Last Modified: Wed, 22 Jul 2020 18:24:38 GMT  
		Size: 31.8 MB (31810242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f65e5f40237135eb0dc1ecbca05b0ad9e996547a54645dbf2c1f224e177ee2`  
		Last Modified: Wed, 22 Jul 2020 18:24:28 GMT  
		Size: 863.6 KB (863577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b461ec2eec3b5affd95277495804497a9d37e03a8561572308599999416d5f`  
		Last Modified: Wed, 22 Jul 2020 18:24:28 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4935880f04a2f54a0851bb9c16a7b44807a6f0238e199a0eac80ab6575eee24`  
		Last Modified: Wed, 22 Jul 2020 18:25:28 GMT  
		Size: 226.2 MB (226237296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:8053db17f111e35f91dc18fa95ed7a9e90d8cf75798367009a2f0ca9c1ba125c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.7 MB (328668535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2050051c720747171cdd515df23ce0d8352c44f3b8d9469f6e2df0407f309b96`
-	Default Command: `["R"]`

```dockerfile
# Wed, 22 Jul 2020 02:18:37 GMT
ADD file:d6f4416408e160284a3c90cab6e53a951dbbc7c1dfa4811f000212296eba31d7 in / 
# Wed, 22 Jul 2020 02:18:43 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 16:36:54 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 22 Jul 2020 16:37:04 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 22 Jul 2020 16:40:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		ed 		fonts-texgyre 		less 		locales 		vim-tiny 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 16:40:19 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 22 Jul 2020 16:40:23 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 22 Jul 2020 16:40:27 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 Jul 2020 16:40:45 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Wed, 22 Jul 2020 16:40:52 GMT
ENV R_BASE_VERSION=4.0.2
# Wed, 22 Jul 2020 16:49:08 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/build.r /usr/local/bin/build.r 	&& ln -s /usr/lib/R/site-library/littler/examples/check.r /usr/local/bin/check.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 16:49:25 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:1e364755122e5010d03f3981d981af0aa16507fb01fdd2c15d80db1a963b580f`  
		Last Modified: Wed, 22 Jul 2020 02:31:33 GMT  
		Size: 58.0 MB (57953376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feef8a33b4b62328cdb97c472c74451134599e5d747e71a852c4a8de0efb9c0d`  
		Last Modified: Wed, 22 Jul 2020 16:49:49 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf961d0022aa866c60a9f344c7471db43ffc2be326be68fa7dc4485340e0cdcf`  
		Last Modified: Wed, 22 Jul 2020 16:49:54 GMT  
		Size: 33.8 MB (33769704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbbb5f2890145f505886efac8b220b1bc027cdcc2209919c53965e75af5cd11`  
		Last Modified: Wed, 22 Jul 2020 16:49:49 GMT  
		Size: 863.6 KB (863574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce397ad821652ca80c5024156ab489bb9be2c3c4d44a687d92a5401f890dc8d1`  
		Last Modified: Wed, 22 Jul 2020 16:49:49 GMT  
		Size: 299.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f5f384a1a66f8977f3f739478739be2d29317f8b4f9435cffa8f241c9c95f0`  
		Last Modified: Wed, 22 Jul 2020 16:50:34 GMT  
		Size: 236.1 MB (236079698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

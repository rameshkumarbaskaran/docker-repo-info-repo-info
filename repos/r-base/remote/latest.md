## `r-base:latest`

```console
$ docker pull r-base@sha256:53e6cfd9e603d8c8d9fba162217bd22f1605ed801e096a4ff94af0b137231938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:42c5988e209690d334d3d0117bbabd932a33106f726603642a8612b584de8644
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338995163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ef3904a475479319438e3051acda0df03e8cf21e55c01158db9ff45cf6c09c`
-	Default Command: `["R"]`

```dockerfile
# Wed, 11 May 2022 01:22:25 GMT
ADD file:281fd73718c53fc59c1102594f7f1e885886403980fd1b7ca7f5c96a97f4332b in / 
# Wed, 11 May 2022 01:22:25 GMT
CMD ["bash"]
# Wed, 11 May 2022 09:19:40 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 11 May 2022 09:19:41 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 11 May 2022 09:19:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 09:19:52 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 11 May 2022 09:19:52 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 11 May 2022 09:19:52 GMT
ENV LANG=en_US.UTF-8
# Wed, 11 May 2022 09:19:53 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 11 May 2022 09:19:53 GMT
ENV R_BASE_VERSION=4.2.0
# Wed, 11 May 2022 09:20:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 09:20:40 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:bb3baf4f16d6f037d735d8dffacf29da8066f489b61bffeceeda9f6403aadeb6`  
		Last Modified: Wed, 11 May 2022 01:29:18 GMT  
		Size: 52.9 MB (52944486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2111bbc5433eca944ee5c72112d8dd0af3c8b58166cf253c4a5962277136738`  
		Last Modified: Wed, 11 May 2022 09:20:56 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6451c42a423dde0eed7dc0aa6fff44f13861522677fb4850d30f098c833e0634`  
		Last Modified: Wed, 11 May 2022 09:21:00 GMT  
		Size: 27.8 MB (27800969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3824ae840517ec001011ec0e868cbc8d2cd8ba5457a6bb4e903cab3b2c7468`  
		Last Modified: Wed, 11 May 2022 09:20:57 GMT  
		Size: 864.6 KB (864611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee0c53da2944e8e539b17a8a8c6c970799212392a92aef659a948f7c5914f21`  
		Last Modified: Wed, 11 May 2022 09:20:56 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f757280e14ccf7c5dd0a7420b3783aafb1f68f1e5571f27681dbd743c7e6731a`  
		Last Modified: Wed, 11 May 2022 09:21:26 GMT  
		Size: 257.4 MB (257382871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:c479c45e66f763c92a65c4c0a0f359aa9d7e6992557d0033c8f72146e3e5cea1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.0 MB (327961074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637689a4cf2281434032cc504cdd21405d4b72f3bd9ec9535f8c4f660b5e5e4b`
-	Default Command: `["R"]`

```dockerfile
# Wed, 11 May 2022 00:49:33 GMT
ADD file:0988640837d33ed2d59a755b6ce36280aed5b71564cd63d0a6ca0e453c6a3fbe in / 
# Wed, 11 May 2022 00:49:34 GMT
CMD ["bash"]
# Wed, 11 May 2022 11:54:59 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 11 May 2022 11:55:00 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 11 May 2022 11:55:11 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 11:55:13 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 11 May 2022 11:55:14 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 11 May 2022 11:55:15 GMT
ENV LANG=en_US.UTF-8
# Wed, 11 May 2022 11:55:16 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 11 May 2022 11:55:17 GMT
ENV R_BASE_VERSION=4.2.0
# Wed, 11 May 2022 11:56:26 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 11:56:27 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:df081a59b146866ecb46fd8e9497a42fbb21fa5c69ac731dfb18c94237063401`  
		Last Modified: Wed, 11 May 2022 00:58:17 GMT  
		Size: 52.0 MB (52041284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d4da358aa077efdf543424278e4454346be8bd0e6c3f26ffb1f57580cbb23a`  
		Last Modified: Wed, 11 May 2022 11:56:48 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5971da3165582d687d18639dcb761c9e20796735b8f5ffeabb2a2bb48c060f5e`  
		Last Modified: Wed, 11 May 2022 11:56:52 GMT  
		Size: 27.6 MB (27649049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa514657e474ac3915638f0fe2025f9e0ead9113be157b0fc68438b4d15215d3`  
		Last Modified: Wed, 11 May 2022 11:56:49 GMT  
		Size: 864.6 KB (864611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06e8474060655b473f5188458b6cb00da94d9ca75e17bd204ab9b6935907f5e`  
		Last Modified: Wed, 11 May 2022 11:56:48 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60155711291fd7ad532217e80256134989e20026e3fdd8df0aee820fe33f3e05`  
		Last Modified: Wed, 11 May 2022 11:57:17 GMT  
		Size: 247.4 MB (247403953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:d266c044dd0f202c934c2bc142cb9f79ea8cef5be99a4f8e01dbcaab22e88d3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.0 MB (338005034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2d9d80cfbcca22786705d63f7a61951e1e522d26391403457475ac30240bbb`
-	Default Command: `["R"]`

```dockerfile
# Wed, 11 May 2022 01:36:50 GMT
ADD file:8824d2629598c6f5c70db2488623b2873dd8496f2765f9a16b931e62ebe1d2ca in / 
# Wed, 11 May 2022 01:36:58 GMT
CMD ["bash"]
# Wed, 11 May 2022 14:08:04 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 11 May 2022 14:08:17 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 11 May 2022 14:09:57 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:10:07 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 11 May 2022 14:10:12 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 11 May 2022 14:10:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 11 May 2022 14:10:22 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 11 May 2022 14:10:26 GMT
ENV R_BASE_VERSION=4.2.0
# Wed, 11 May 2022 14:16:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:16:53 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f847dd78355ff75879dd0f1ed43325b24a1351e2cb0038f2cf60d5e061b5b866`  
		Last Modified: Wed, 11 May 2022 01:46:57 GMT  
		Size: 57.2 MB (57150570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b12b755287361006c0528870d3b56ef447c99483b78d29f9f27f5363578bcae`  
		Last Modified: Wed, 11 May 2022 14:17:22 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab95c5ea7c946a7f5fec117da0e8b1b44c13cbfabe434e074368791be39e18`  
		Last Modified: Wed, 11 May 2022 14:17:26 GMT  
		Size: 28.1 MB (28116508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cbf74157feaae7eccad2e1bed24736b304ca1226ab3d655e05a6d3d3d01d4d`  
		Last Modified: Wed, 11 May 2022 14:17:23 GMT  
		Size: 864.6 KB (864616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bd0c005890cf6815eb421cec6728504e3b018800cfc617117994810c1dd42b`  
		Last Modified: Wed, 11 May 2022 14:17:22 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ea9d64f7741d05c0855435f54474042e8c7a19fa4c22ee11ac13afd8768663`  
		Last Modified: Wed, 11 May 2022 14:18:00 GMT  
		Size: 251.9 MB (251871101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:7d9a7d662a01a6b571f2ece9f5e0d5d9f8fffd95687047d4c4b62c614bb12eac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303502140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff06ff773b519e04c597ac2259cdb23740df1758169938f952da6a9e69503f04`
-	Default Command: `["R"]`

```dockerfile
# Wed, 11 May 2022 00:46:20 GMT
ADD file:bc41b042aacce4ae1287887b131147ffd633199e05ca01c60eb947f7870fbe1f in / 
# Wed, 11 May 2022 00:46:22 GMT
CMD ["bash"]
# Wed, 11 May 2022 11:47:51 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Wed, 11 May 2022 11:47:55 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 11 May 2022 11:48:19 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 11:48:22 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 11 May 2022 11:48:22 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 11 May 2022 11:48:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 11 May 2022 11:48:23 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 11 May 2022 11:48:23 GMT
ENV R_BASE_VERSION=4.2.0
# Wed, 11 May 2022 11:49:09 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 11:49:16 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:0b8e880b03aeb5fc80c518705ebfff1cf2c20587545b643f5f61de5e3b0dc6c3`  
		Last Modified: Wed, 11 May 2022 00:52:17 GMT  
		Size: 51.5 MB (51483822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaccd76326dba199712c9e7eeccc6db8d2e03dbf04d5f61323ada92291dc28d`  
		Last Modified: Wed, 11 May 2022 11:49:32 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a19e59ec7fd6f493865b938f16edbc51406fd2337997c3944ce8729dc0ad2f`  
		Last Modified: Wed, 11 May 2022 11:49:34 GMT  
		Size: 27.5 MB (27505458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7723d6b8fde3889721eaac3b05dfaa30ca8de11c00239c0d4d5929c061a159b1`  
		Last Modified: Wed, 11 May 2022 11:49:32 GMT  
		Size: 920.2 KB (920189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c396fae589782cbc3d117a2af893d0d781383ef8aa10976e6612bb2e8494de9`  
		Last Modified: Wed, 11 May 2022 11:49:32 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62709858c720238add7e417599c75adc8c6a088c536f9c2226c87fef24a7bfec`  
		Last Modified: Wed, 11 May 2022 11:49:53 GMT  
		Size: 223.6 MB (223590434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

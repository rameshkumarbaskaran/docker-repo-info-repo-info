## `r-base:latest`

```console
$ docker pull r-base@sha256:28f173167a334a94cf90043c95f260b36f6dba781a6b863c135ee9057a720074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:6eaf4b405bbb6538cead9219221c66a68a52c0718e38745a59a233e14c26a967
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.1 MB (644140148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d505b1b24a98083901eb7a50ddaf8bfdf296bbf7b81a1407b837cdff799c611`
-	Default Command: `["R"]`

```dockerfile
# Tue, 17 Nov 2020 20:24:45 GMT
ADD file:b6d9d03d246917cd8a499e26b7dafcdd42ca61c3cbb6e60b78c888a349814210 in / 
# Tue, 17 Nov 2020 20:24:45 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:21:07 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 18 Nov 2020 08:21:08 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 18 Nov 2020 08:21:22 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:21:25 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 18 Nov 2020 08:21:25 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 18 Nov 2020 08:21:25 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Nov 2020 08:21:26 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 18 Nov 2020 08:21:26 GMT
ENV R_BASE_VERSION=4.0.3
# Wed, 18 Nov 2020 08:24:05 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:24:06 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:a919358b170f991da872d2c4a5b2210ce45783166a93d65c90ee3cad6b86dbc8`  
		Last Modified: Tue, 17 Nov 2020 20:30:58 GMT  
		Size: 55.6 MB (55577988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1a676142d9f8d956a73ebf191e49d0cfe6a8062c92c85c1c1e0ef01a7d9bc4`  
		Last Modified: Wed, 18 Nov 2020 08:24:29 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbe917a25f5b0973636460470a97c3ed05959d992ef5414c7138c59613a622e`  
		Last Modified: Wed, 18 Nov 2020 08:24:36 GMT  
		Size: 25.6 MB (25558198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fdbdc08d5003898a1569e91ec7ba5568d84ea4806d34187f7e8c670f11e8ae`  
		Last Modified: Wed, 18 Nov 2020 08:24:29 GMT  
		Size: 863.6 KB (863578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7e3fa43e357767fd578d1b7a1a6c4f88193a7c91f87ad8549c09e884dc7fca`  
		Last Modified: Wed, 18 Nov 2020 08:24:28 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0808418726cfd4b10b2a7b0bbccd1d55c65f100364aa5ef49baf1b0d766a2f`  
		Last Modified: Wed, 18 Nov 2020 08:26:37 GMT  
		Size: 562.1 MB (562138189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:28345858836ff8e03ee0e5ba0c56fff5fad81772ded711d438da81bd2292d661
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.9 MB (610876058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7ce30fde7892a626ce923d1c33c3234e32e518899ad846b7593395c4f3d787`
-	Default Command: `["R"]`

```dockerfile
# Tue, 17 Nov 2020 20:28:30 GMT
ADD file:d37369ae30ab48a0f2543398c3654e86c4974a89273a04c2eba7fa459d0bc05b in / 
# Tue, 17 Nov 2020 20:28:35 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 09:04:13 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 18 Nov 2020 09:04:23 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 18 Nov 2020 09:05:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:05:14 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 18 Nov 2020 09:05:15 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 18 Nov 2020 09:05:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Nov 2020 09:05:18 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 18 Nov 2020 09:05:19 GMT
ENV R_BASE_VERSION=4.0.3
# Wed, 18 Nov 2020 09:07:47 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 09:07:52 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:43bafc6092e82ecdff33419c83556ff270d573c7d3e94e242c50046b2cde340e`  
		Last Modified: Tue, 17 Nov 2020 20:34:59 GMT  
		Size: 54.3 MB (54323514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78355d8724a9336ebad09c2ac07c027c0b1774ba67db9d8b36298ad475590786`  
		Last Modified: Wed, 18 Nov 2020 09:08:11 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38393bce8dbe11220d01fd5e079697f12d96d124bb002866874a57ea7544856`  
		Last Modified: Wed, 18 Nov 2020 09:08:18 GMT  
		Size: 25.6 MB (25562157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e9e4964d619bc6922a33f4ad3db592487b96f4ea86a32839b2171ca1d841a1`  
		Last Modified: Wed, 18 Nov 2020 09:08:10 GMT  
		Size: 863.6 KB (863574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dd518bb0d8741ce94cc23c6915e2390cf424704be1497ed9a7bad59cae73e4`  
		Last Modified: Wed, 18 Nov 2020 09:08:10 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0224b5e32f7d73270d11d7943adc2c8dac18cfb803c2a56e080def3dc28c3d87`  
		Last Modified: Wed, 18 Nov 2020 09:10:25 GMT  
		Size: 530.1 MB (530124585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:f14e1662edbeebb2c9e6b1cc38af4ae90de52e058dead44566d96ffba0c679af
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.3 MB (613313880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adcc0e2c50ee03625ade975c2ec10ee2812c8dcced8aab7b381881d571b5e7c1`
-	Default Command: `["R"]`

```dockerfile
# Tue, 17 Nov 2020 23:25:16 GMT
ADD file:74e3f9199d8973f4d6859f7dfad98ea11e79e7829d5756710a16351f8c033596 in / 
# Tue, 17 Nov 2020 23:25:24 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 10:06:53 GMT
LABEL org.label-schema.license=GPL-2.0 org.label-schema.vcs-url=https://github.com/rocker-org/r-base org.label-schema.vendor=Rocker Project maintainer=Dirk Eddelbuettel <edd@debian.org>
# Wed, 18 Nov 2020 10:07:06 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Wed, 18 Nov 2020 10:08:11 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 10:08:21 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Wed, 18 Nov 2020 10:08:24 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 18 Nov 2020 10:08:26 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Nov 2020 10:08:30 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends
# Wed, 18 Nov 2020 10:08:35 GMT
ENV R_BASE_VERSION=4.0.3
# Wed, 18 Nov 2020 10:16:52 GMT
RUN apt-get update         && apt-get install -t unstable -y --no-install-recommends                 gcc-9-base                 libopenblas0-pthread 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 10:16:58 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:ac668230de37b88984090c102d2d7b0848c85b72d33b9fe4aff709b7ef0074ed`  
		Last Modified: Tue, 17 Nov 2020 23:38:25 GMT  
		Size: 59.8 MB (59761435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c05719ec613e5ce07a8a32f835dfaa5162ad8acc7f2c619ba4c90b06806e656`  
		Last Modified: Wed, 18 Nov 2020 10:17:13 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de98d65e9efa65b4ea55a70f08f8d43802a3dafd91caa1ad7a77c57d20f1e07`  
		Last Modified: Wed, 18 Nov 2020 10:17:18 GMT  
		Size: 25.8 MB (25773500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5028154bc4993e2607ff85963e6013c3f2ea51581c8cecc9b94a1e3f59e3dc`  
		Last Modified: Wed, 18 Nov 2020 10:17:14 GMT  
		Size: 863.6 KB (863578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e82a370224d81e617bf9bb64eb08c9939808ccbc5833aefa935b1b4bfdd87`  
		Last Modified: Wed, 18 Nov 2020 10:17:14 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2a2b677d0eff30f3c0a002e31fbd62f9fa36b0f5db799a8fa9e5540963b0e9`  
		Last Modified: Wed, 18 Nov 2020 10:18:54 GMT  
		Size: 526.9 MB (526913130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

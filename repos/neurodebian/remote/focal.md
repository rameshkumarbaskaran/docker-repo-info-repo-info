## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:4e7af61e2e9289eae0fa09e7df1a2dd835248d5735a4897e78c87abb5f46d176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:4533ae40c203b821d331a1769632881a810c0ef285e73353b10eb35aad34eb8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e81b9beb29eb7fc36b4502cad48ee7628826862ca6cd339dad397da1cb0f7f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:59:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:59:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 02 Mar 2023 04:59:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 02 Mar 2023 04:59:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04aa245e8cf14b4957e41694df0101cf3e7c1f3c70e0c0609a575baff52720a`  
		Last Modified: Thu, 02 Mar 2023 05:00:42 GMT  
		Size: 5.5 MB (5494398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3604d23a5296dcb40e59f99bd1e3794c4a6b1da0f21f2758532ca6bd198884e`  
		Last Modified: Thu, 02 Mar 2023 05:00:41 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04966aaa9ed577cb2d23e89dfbf7f3a25aa68d0858837c1d51f6cba868b9fde9`  
		Last Modified: Thu, 02 Mar 2023 05:00:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6991b34437f0d313cc1758593ae3aca5f2e2a560c0c9e152d32322ac1a0d6b00`  
		Last Modified: Thu, 02 Mar 2023 05:00:42 GMT  
		Size: 239.0 KB (238982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:da7229782d5fba3c8438c2b2de88bd3c6099ae476b1703fa26e86395a7562083
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32913450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e563d61ed1e782e4a6aaa7a5d76b241ebd72621b74a11f862ab60ded47aa82b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:41:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:41:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 16 Mar 2023 02:41:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 16 Mar 2023 02:41:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e0fa92cd3582d80aff5b2299f607fdb844073e93206a5faa67edc5c9325ca0`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 5.5 MB (5475368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3890803dae85595f0523a3e12cd251ae1e4da06c3a09f31ae4fcc17a6907078`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c0f4751d574a8300a6c196239dfe9680016fbf164f5df83edfc561850e0cea`  
		Last Modified: Thu, 16 Mar 2023 02:43:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a62bffbf3b260bd8e982d4681e9f6928427b97a549221f60cd5f5e6593644f1`  
		Last Modified: Thu, 16 Mar 2023 02:43:02 GMT  
		Size: 239.9 KB (239908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

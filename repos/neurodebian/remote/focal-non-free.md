## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:7d92c9ebe90a7c6f708b792ea78fadf4a1ee38d449b8ff9d6a5bc703f4f94b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e073e031a4a6d9a0ba2e8698883a93d78f7f02605dce5429e06938d0c3a696f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34317018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3615da31fcee40f87efbe02509455a6357ffbe41d7f9ea2805858013d9bd03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:29:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:29:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 08:29:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 08:29:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:29:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:7a2c559011895d255fce249c00396abff5ae7e0c0a92931d0ed493e71de78e3a`  
		Last Modified: Tue, 03 Oct 2023 17:02:08 GMT  
		Size: 28.6 MB (28580681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd85b9bbb4f6a9a09f01ff35c38ff6c009e4ed47c1e1adb561e5e1881ef6329`  
		Last Modified: Fri, 13 Oct 2023 08:31:16 GMT  
		Size: 5.5 MB (5494637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a82d4dfa24a3aa971caf981cc84ea5292b7c56b4335194a635a745d12cf335e`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e62499f00f9e5e824ea39061aa4a173eb1dea821e53978d30d32377cfdb483`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fecfaed538c1437570df4d09b720ce5fc7a1516d14bf689952efdb1882979b2`  
		Last Modified: Fri, 13 Oct 2023 08:31:15 GMT  
		Size: 239.4 KB (239434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78be323d4e6d5888beb53bc54cb02411f80710e117bd8b93dd3fbd147bde90cb`  
		Last Modified: Fri, 13 Oct 2023 08:31:24 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:07d82819b71e813a5458133a08ac64541f6f6e9a15fd4b3820a02e8fb49f945d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32917032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f0af1ce5b729930583866de774b375ed677e0ccee5d9799aa876e8bf8877c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:55:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:55:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 02:55:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 02:55:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:55:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735b752a5a5ddf2e2a73ae4efa42262f0bc4d0c1d75658b76770451fc0458f6a`  
		Last Modified: Fri, 13 Oct 2023 02:56:47 GMT  
		Size: 5.5 MB (5475192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3041aaece1d5937a215d07e3f1fc08de72687caf87826635325e5c8f7f45418c`  
		Last Modified: Fri, 13 Oct 2023 02:56:46 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da06e0720e864bbf2fbae18550b7e7877c71a63f413c7ee1d76240441c64895`  
		Last Modified: Fri, 13 Oct 2023 02:56:46 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43168bfd26889b61874a4ae799abf4489eb95c11265e131ec5b50d6971d9a819`  
		Last Modified: Fri, 13 Oct 2023 02:56:47 GMT  
		Size: 240.1 KB (240069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4f4e3657a300eddb3d58745b4ef645b6bdf391f63bb940bf63fe58cff0b930`  
		Last Modified: Fri, 13 Oct 2023 02:56:56 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

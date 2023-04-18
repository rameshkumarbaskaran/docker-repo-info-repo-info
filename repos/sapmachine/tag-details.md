<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.18`](#sapmachine11018)
-	[`sapmachine:17`](#sapmachine17)
-	[`sapmachine:17.0.6`](#sapmachine1706)
-	[`sapmachine:19`](#sapmachine19)
-	[`sapmachine:19.0.2`](#sapmachine1902)
-	[`sapmachine:20`](#sapmachine20)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:9e3e741228785f7a3787687fb35c580e3ad298721375eae0fb523850ec77e975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:05316a992634334e26faab31a57f90e5da70fa738316d4e27204da05162ee00b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235426738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca84ca2080981c0417237ca92669250491412bd5b7028afe910155215a64f57b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:18:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:19:26 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.18     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:19:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 18 Apr 2023 01:19:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa7fcf1d088a5e28885bcd22e9b185e81e5f63d784be8e835865efa147ef11`  
		Last Modified: Tue, 18 Apr 2023 01:21:26 GMT  
		Size: 7.9 MB (7917699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d1dc35b68f32b3a76b3c6fa6615d78106e3bb4ffc38e9d7ecbd420c11cbee6`  
		Last Modified: Tue, 18 Apr 2023 01:21:38 GMT  
		Size: 198.9 MB (198930476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e91812d42286a6f278365d399e287b048dad342ca95b7c5a5b48f7379c74cc7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231821747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5372c0f66e4e855bd91e56e8ef8bd7816fd7c7a0bb6d67691ed6a676f3038a9e`
-	Default Command: `["jshell"]`

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
# Thu, 16 Mar 2023 03:54:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:00 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.18     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 16 Mar 2023 03:55:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c31633819b087c3d39e7948f611348779db8dd22bc8a3db707f870d7cd24b3`  
		Last Modified: Thu, 16 Mar 2023 03:56:12 GMT  
		Size: 7.8 MB (7757240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d11ce92bc63bc694aa4a48385a4db111547fe48e3897858dc8ba02a261a0961`  
		Last Modified: Thu, 16 Mar 2023 03:56:23 GMT  
		Size: 196.9 MB (196868346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:84e5bbe5c7a2b16f7b6911c0284a34e139add5e01416b10776d9cd92cc89ec6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227466215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fc88032b4c4553fb34edbfbc2717290bf9622c064159fcd44943d469e598ab`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:16:10 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.18     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:16:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 18 Apr 2023 01:16:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7b240a15bddb0a3f238ea0f9dd5dcffb15162dfa03f4e233171b45b41c03e9`  
		Last Modified: Tue, 18 Apr 2023 01:22:20 GMT  
		Size: 9.3 MB (9316592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4680d4dae6266355337349d9fd4b301f24654d7ae03fe2ddb227a639b978434`  
		Last Modified: Tue, 18 Apr 2023 01:22:39 GMT  
		Size: 184.8 MB (184848643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.18`

```console
$ docker pull sapmachine@sha256:9e3e741228785f7a3787687fb35c580e3ad298721375eae0fb523850ec77e975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:11.0.18` - linux; amd64

```console
$ docker pull sapmachine@sha256:05316a992634334e26faab31a57f90e5da70fa738316d4e27204da05162ee00b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235426738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca84ca2080981c0417237ca92669250491412bd5b7028afe910155215a64f57b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:18:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:19:26 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.18     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:19:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 18 Apr 2023 01:19:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa7fcf1d088a5e28885bcd22e9b185e81e5f63d784be8e835865efa147ef11`  
		Last Modified: Tue, 18 Apr 2023 01:21:26 GMT  
		Size: 7.9 MB (7917699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d1dc35b68f32b3a76b3c6fa6615d78106e3bb4ffc38e9d7ecbd420c11cbee6`  
		Last Modified: Tue, 18 Apr 2023 01:21:38 GMT  
		Size: 198.9 MB (198930476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11.0.18` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e91812d42286a6f278365d399e287b048dad342ca95b7c5a5b48f7379c74cc7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231821747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5372c0f66e4e855bd91e56e8ef8bd7816fd7c7a0bb6d67691ed6a676f3038a9e`
-	Default Command: `["jshell"]`

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
# Thu, 16 Mar 2023 03:54:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:00 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.18     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 16 Mar 2023 03:55:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c31633819b087c3d39e7948f611348779db8dd22bc8a3db707f870d7cd24b3`  
		Last Modified: Thu, 16 Mar 2023 03:56:12 GMT  
		Size: 7.8 MB (7757240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d11ce92bc63bc694aa4a48385a4db111547fe48e3897858dc8ba02a261a0961`  
		Last Modified: Thu, 16 Mar 2023 03:56:23 GMT  
		Size: 196.9 MB (196868346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11.0.18` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:84e5bbe5c7a2b16f7b6911c0284a34e139add5e01416b10776d9cd92cc89ec6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227466215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fc88032b4c4553fb34edbfbc2717290bf9622c064159fcd44943d469e598ab`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:16:10 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.18     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:16:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 18 Apr 2023 01:16:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7b240a15bddb0a3f238ea0f9dd5dcffb15162dfa03f4e233171b45b41c03e9`  
		Last Modified: Tue, 18 Apr 2023 01:22:20 GMT  
		Size: 9.3 MB (9316592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4680d4dae6266355337349d9fd4b301f24654d7ae03fe2ddb227a639b978434`  
		Last Modified: Tue, 18 Apr 2023 01:22:39 GMT  
		Size: 184.8 MB (184848643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:e0e5b84b264b22f2378eff69d5648b8a811fc443da1de63249cd7961637a07b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:0f5b31b7c70158e5d83143b53e1c8a739330b8db54a82c428e516fb8b4e79737
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234576769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c56f4b9b999a03f0369b1999860e53fd74b99f591efea3bd2631b5e769efb20`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:18:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:06 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 18 Apr 2023 01:20:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa7fcf1d088a5e28885bcd22e9b185e81e5f63d784be8e835865efa147ef11`  
		Last Modified: Tue, 18 Apr 2023 01:21:26 GMT  
		Size: 7.9 MB (7917699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97af029ef0ba5a27d6027cb52ca458497a95b2a8d5494c4053aafb503193315a`  
		Last Modified: Tue, 18 Apr 2023 01:22:00 GMT  
		Size: 198.1 MB (198080507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e87e4c94e8d466ddccf7332e8696062d6e11e368d0bf39bfbde62c7c3c5affb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231062233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ebef26da4731478f25f320c57432db38b545ad88837982884cc356ae92d78f`
-	Default Command: `["jshell"]`

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
# Thu, 16 Mar 2023 03:54:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:28 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 16 Mar 2023 03:55:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c31633819b087c3d39e7948f611348779db8dd22bc8a3db707f870d7cd24b3`  
		Last Modified: Thu, 16 Mar 2023 03:56:12 GMT  
		Size: 7.8 MB (7757240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a37334232fc2008f6bbcb04969537ab530206c40ad106fd76326bac241c1ca`  
		Last Modified: Thu, 16 Mar 2023 03:56:43 GMT  
		Size: 196.1 MB (196108832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c40e29cbe729aac7aa05453ec75f28bedf042a2545eb6c76c2ed9e96de70ef3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240841478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1963003680e5c809897c76f6ea3648ee60f36c9a3d52bb18a63256d3c8caa5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:18:03 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:18:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 18 Apr 2023 01:18:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7b240a15bddb0a3f238ea0f9dd5dcffb15162dfa03f4e233171b45b41c03e9`  
		Last Modified: Tue, 18 Apr 2023 01:22:20 GMT  
		Size: 9.3 MB (9316592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18569d6a9c5078185f28c33f6ee8624e6cf685f2b6ad30cd706b7be4573b1cf4`  
		Last Modified: Tue, 18 Apr 2023 01:23:16 GMT  
		Size: 198.2 MB (198223906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17.0.6`

```console
$ docker pull sapmachine@sha256:e0e5b84b264b22f2378eff69d5648b8a811fc443da1de63249cd7961637a07b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:17.0.6` - linux; amd64

```console
$ docker pull sapmachine@sha256:0f5b31b7c70158e5d83143b53e1c8a739330b8db54a82c428e516fb8b4e79737
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234576769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c56f4b9b999a03f0369b1999860e53fd74b99f591efea3bd2631b5e769efb20`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:18:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:06 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 18 Apr 2023 01:20:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa7fcf1d088a5e28885bcd22e9b185e81e5f63d784be8e835865efa147ef11`  
		Last Modified: Tue, 18 Apr 2023 01:21:26 GMT  
		Size: 7.9 MB (7917699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97af029ef0ba5a27d6027cb52ca458497a95b2a8d5494c4053aafb503193315a`  
		Last Modified: Tue, 18 Apr 2023 01:22:00 GMT  
		Size: 198.1 MB (198080507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17.0.6` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e87e4c94e8d466ddccf7332e8696062d6e11e368d0bf39bfbde62c7c3c5affb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231062233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ebef26da4731478f25f320c57432db38b545ad88837982884cc356ae92d78f`
-	Default Command: `["jshell"]`

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
# Thu, 16 Mar 2023 03:54:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:28 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 16 Mar 2023 03:55:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c31633819b087c3d39e7948f611348779db8dd22bc8a3db707f870d7cd24b3`  
		Last Modified: Thu, 16 Mar 2023 03:56:12 GMT  
		Size: 7.8 MB (7757240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a37334232fc2008f6bbcb04969537ab530206c40ad106fd76326bac241c1ca`  
		Last Modified: Thu, 16 Mar 2023 03:56:43 GMT  
		Size: 196.1 MB (196108832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17.0.6` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c40e29cbe729aac7aa05453ec75f28bedf042a2545eb6c76c2ed9e96de70ef3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240841478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1963003680e5c809897c76f6ea3648ee60f36c9a3d52bb18a63256d3c8caa5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:18:03 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:18:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 18 Apr 2023 01:18:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7b240a15bddb0a3f238ea0f9dd5dcffb15162dfa03f4e233171b45b41c03e9`  
		Last Modified: Tue, 18 Apr 2023 01:22:20 GMT  
		Size: 9.3 MB (9316592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18569d6a9c5078185f28c33f6ee8624e6cf685f2b6ad30cd706b7be4573b1cf4`  
		Last Modified: Tue, 18 Apr 2023 01:23:16 GMT  
		Size: 198.2 MB (198223906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:19`

```console
$ docker pull sapmachine@sha256:f7d320244ca1ce6942f7eb31708c5deb525a1a17d46af9e3ab1c500fcd9e219c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:19` - linux; amd64

```console
$ docker pull sapmachine@sha256:f6db33a419c3b4f30b6b7d8b79ecb1417fb7cabdd441e267be2257e2b870bf42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242933904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fae60402ccbe2bf52998d1e1d6088446c03622ce12817faccba034419fcfbd9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:18:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:39 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Tue, 18 Apr 2023 01:20:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa7fcf1d088a5e28885bcd22e9b185e81e5f63d784be8e835865efa147ef11`  
		Last Modified: Tue, 18 Apr 2023 01:21:26 GMT  
		Size: 7.9 MB (7917699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e280faa2fe0ed741f94bc34495ba97c284fc88a22bc403194eba3123b1ec850`  
		Last Modified: Tue, 18 Apr 2023 01:22:24 GMT  
		Size: 206.4 MB (206437642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:19` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:899093ed8b230b827dd2eac415ef84b9d0af3d42142b7f3b4906375906cba676
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239521140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a3f5d25bd19146e65897b9386b9eacbd7fe46046130260f2b370401e96edb2`
-	Default Command: `["jshell"]`

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
# Thu, 16 Mar 2023 03:54:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:55 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Thu, 16 Mar 2023 03:55:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c31633819b087c3d39e7948f611348779db8dd22bc8a3db707f870d7cd24b3`  
		Last Modified: Thu, 16 Mar 2023 03:56:12 GMT  
		Size: 7.8 MB (7757240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf59d8bb78000813504bb1bb159974e8d9064e7713cdd345476cec4c446b084b`  
		Last Modified: Thu, 16 Mar 2023 03:57:05 GMT  
		Size: 204.6 MB (204567739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:19` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c1b737d073b595172aa1e382460bb8cf9176e2000509ae8d7de62a9ca60602d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249082648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e298f301ff65c37de05cd3c7f863eca02d3833434951fda1ff8c580b0ba350b5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:08 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Tue, 18 Apr 2023 01:20:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7b240a15bddb0a3f238ea0f9dd5dcffb15162dfa03f4e233171b45b41c03e9`  
		Last Modified: Tue, 18 Apr 2023 01:22:20 GMT  
		Size: 9.3 MB (9316592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f545935701a93640980d9d039e9e166cdf0d9c2f40b8d3280148be0dbe4bf168`  
		Last Modified: Tue, 18 Apr 2023 01:23:53 GMT  
		Size: 206.5 MB (206465076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:19.0.2`

```console
$ docker pull sapmachine@sha256:f7d320244ca1ce6942f7eb31708c5deb525a1a17d46af9e3ab1c500fcd9e219c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:19.0.2` - linux; amd64

```console
$ docker pull sapmachine@sha256:f6db33a419c3b4f30b6b7d8b79ecb1417fb7cabdd441e267be2257e2b870bf42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242933904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fae60402ccbe2bf52998d1e1d6088446c03622ce12817faccba034419fcfbd9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:18:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:39 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Tue, 18 Apr 2023 01:20:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa7fcf1d088a5e28885bcd22e9b185e81e5f63d784be8e835865efa147ef11`  
		Last Modified: Tue, 18 Apr 2023 01:21:26 GMT  
		Size: 7.9 MB (7917699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e280faa2fe0ed741f94bc34495ba97c284fc88a22bc403194eba3123b1ec850`  
		Last Modified: Tue, 18 Apr 2023 01:22:24 GMT  
		Size: 206.4 MB (206437642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:19.0.2` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:899093ed8b230b827dd2eac415ef84b9d0af3d42142b7f3b4906375906cba676
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239521140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a3f5d25bd19146e65897b9386b9eacbd7fe46046130260f2b370401e96edb2`
-	Default Command: `["jshell"]`

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
# Thu, 16 Mar 2023 03:54:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:55 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Thu, 16 Mar 2023 03:55:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c31633819b087c3d39e7948f611348779db8dd22bc8a3db707f870d7cd24b3`  
		Last Modified: Thu, 16 Mar 2023 03:56:12 GMT  
		Size: 7.8 MB (7757240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf59d8bb78000813504bb1bb159974e8d9064e7713cdd345476cec4c446b084b`  
		Last Modified: Thu, 16 Mar 2023 03:57:05 GMT  
		Size: 204.6 MB (204567739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:19.0.2` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c1b737d073b595172aa1e382460bb8cf9176e2000509ae8d7de62a9ca60602d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249082648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e298f301ff65c37de05cd3c7f863eca02d3833434951fda1ff8c580b0ba350b5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:08 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Tue, 18 Apr 2023 01:20:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7b240a15bddb0a3f238ea0f9dd5dcffb15162dfa03f4e233171b45b41c03e9`  
		Last Modified: Tue, 18 Apr 2023 01:22:20 GMT  
		Size: 9.3 MB (9316592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f545935701a93640980d9d039e9e166cdf0d9c2f40b8d3280148be0dbe4bf168`  
		Last Modified: Tue, 18 Apr 2023 01:23:53 GMT  
		Size: 206.5 MB (206465076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:20`

```console
$ docker pull sapmachine@sha256:0e0fa531518ed00659f8b3753c74e24ed2ac2e8994f724406c9620b3e2adb030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:20` - linux; amd64

```console
$ docker pull sapmachine@sha256:5305baf0b92f8e614e32c9f4fb89579f90589faedc7bef7943884bbbecfbfb26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244212786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549d0f3cda91a5c3047e4a04027f88947b8ca4d60da44a42b1972e14c693361b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:18:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:21:14 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:21:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 18 Apr 2023 01:21:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa7fcf1d088a5e28885bcd22e9b185e81e5f63d784be8e835865efa147ef11`  
		Last Modified: Tue, 18 Apr 2023 01:21:26 GMT  
		Size: 7.9 MB (7917699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491290f1581ae2267641201c694aa8e06bb983e6bdd6e8b5c1ba020394c15091`  
		Last Modified: Tue, 18 Apr 2023 01:22:48 GMT  
		Size: 207.7 MB (207716524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:20` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:56d4437f0ebbd9ec4157733220032ea5d3cdf39b89cf86f24e41b06311c37c9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240999760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2384dd5ad3e776e9ee68d932a44c2a350721307473cd3ab52055884eb46959`
-	Default Command: `["jshell"]`

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
# Thu, 16 Mar 2023 03:54:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Mar 2023 19:47:29 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Mar 2023 19:47:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Fri, 24 Mar 2023 19:47:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c31633819b087c3d39e7948f611348779db8dd22bc8a3db707f870d7cd24b3`  
		Last Modified: Thu, 16 Mar 2023 03:56:12 GMT  
		Size: 7.8 MB (7757240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73ea06d7958afd59a6059ee5d5aa523fc930bf2382f8d5b2be0c4231baa8099`  
		Last Modified: Fri, 24 Mar 2023 19:48:01 GMT  
		Size: 206.0 MB (206046359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:20` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3ca051ce1a1932d780eabc7bace9ea43bd6ef2ca7de9060d892da3eba14efa3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251189847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4457e5898c3a9f81b9f9eb3c6d85a9bbeda6f54e98067a3e6a8fa3c302b9618d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:21:55 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:21:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 18 Apr 2023 01:22:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7b240a15bddb0a3f238ea0f9dd5dcffb15162dfa03f4e233171b45b41c03e9`  
		Last Modified: Tue, 18 Apr 2023 01:22:20 GMT  
		Size: 9.3 MB (9316592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c519a469c815fedc87e0131e8dce65b06ba4bfec7ba2edf79e9c420bf869ba7`  
		Last Modified: Tue, 18 Apr 2023 01:24:28 GMT  
		Size: 208.6 MB (208572275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:0e0fa531518ed00659f8b3753c74e24ed2ac2e8994f724406c9620b3e2adb030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:5305baf0b92f8e614e32c9f4fb89579f90589faedc7bef7943884bbbecfbfb26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244212786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549d0f3cda91a5c3047e4a04027f88947b8ca4d60da44a42b1972e14c693361b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:18:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:21:14 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:21:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 18 Apr 2023 01:21:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa7fcf1d088a5e28885bcd22e9b185e81e5f63d784be8e835865efa147ef11`  
		Last Modified: Tue, 18 Apr 2023 01:21:26 GMT  
		Size: 7.9 MB (7917699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491290f1581ae2267641201c694aa8e06bb983e6bdd6e8b5c1ba020394c15091`  
		Last Modified: Tue, 18 Apr 2023 01:22:48 GMT  
		Size: 207.7 MB (207716524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:latest` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:56d4437f0ebbd9ec4157733220032ea5d3cdf39b89cf86f24e41b06311c37c9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240999760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2384dd5ad3e776e9ee68d932a44c2a350721307473cd3ab52055884eb46959`
-	Default Command: `["jshell"]`

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
# Thu, 16 Mar 2023 03:54:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Mar 2023 19:47:29 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Mar 2023 19:47:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Fri, 24 Mar 2023 19:47:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c31633819b087c3d39e7948f611348779db8dd22bc8a3db707f870d7cd24b3`  
		Last Modified: Thu, 16 Mar 2023 03:56:12 GMT  
		Size: 7.8 MB (7757240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73ea06d7958afd59a6059ee5d5aa523fc930bf2382f8d5b2be0c4231baa8099`  
		Last Modified: Fri, 24 Mar 2023 19:48:01 GMT  
		Size: 206.0 MB (206046359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:latest` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3ca051ce1a1932d780eabc7bace9ea43bd6ef2ca7de9060d892da3eba14efa3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251189847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4457e5898c3a9f81b9f9eb3c6d85a9bbeda6f54e98067a3e6a8fa3c302b9618d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:21:55 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:21:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 18 Apr 2023 01:22:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7b240a15bddb0a3f238ea0f9dd5dcffb15162dfa03f4e233171b45b41c03e9`  
		Last Modified: Tue, 18 Apr 2023 01:22:20 GMT  
		Size: 9.3 MB (9316592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c519a469c815fedc87e0131e8dce65b06ba4bfec7ba2edf79e9c420bf869ba7`  
		Last Modified: Tue, 18 Apr 2023 01:24:28 GMT  
		Size: 208.6 MB (208572275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:e0e5b84b264b22f2378eff69d5648b8a811fc443da1de63249cd7961637a07b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:0f5b31b7c70158e5d83143b53e1c8a739330b8db54a82c428e516fb8b4e79737
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234576769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c56f4b9b999a03f0369b1999860e53fd74b99f591efea3bd2631b5e769efb20`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:18:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:06 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 18 Apr 2023 01:20:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa7fcf1d088a5e28885bcd22e9b185e81e5f63d784be8e835865efa147ef11`  
		Last Modified: Tue, 18 Apr 2023 01:21:26 GMT  
		Size: 7.9 MB (7917699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97af029ef0ba5a27d6027cb52ca458497a95b2a8d5494c4053aafb503193315a`  
		Last Modified: Tue, 18 Apr 2023 01:22:00 GMT  
		Size: 198.1 MB (198080507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e87e4c94e8d466ddccf7332e8696062d6e11e368d0bf39bfbde62c7c3c5affb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231062233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ebef26da4731478f25f320c57432db38b545ad88837982884cc356ae92d78f`
-	Default Command: `["jshell"]`

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
# Thu, 16 Mar 2023 03:54:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:28 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 16 Mar 2023 03:55:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c31633819b087c3d39e7948f611348779db8dd22bc8a3db707f870d7cd24b3`  
		Last Modified: Thu, 16 Mar 2023 03:56:12 GMT  
		Size: 7.8 MB (7757240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a37334232fc2008f6bbcb04969537ab530206c40ad106fd76326bac241c1ca`  
		Last Modified: Thu, 16 Mar 2023 03:56:43 GMT  
		Size: 196.1 MB (196108832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c40e29cbe729aac7aa05453ec75f28bedf042a2545eb6c76c2ed9e96de70ef3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240841478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1963003680e5c809897c76f6ea3648ee60f36c9a3d52bb18a63256d3c8caa5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:18:03 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:18:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 18 Apr 2023 01:18:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7b240a15bddb0a3f238ea0f9dd5dcffb15162dfa03f4e233171b45b41c03e9`  
		Last Modified: Tue, 18 Apr 2023 01:22:20 GMT  
		Size: 9.3 MB (9316592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18569d6a9c5078185f28c33f6ee8624e6cf685f2b6ad30cd706b7be4573b1cf4`  
		Last Modified: Tue, 18 Apr 2023 01:23:16 GMT  
		Size: 198.2 MB (198223906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

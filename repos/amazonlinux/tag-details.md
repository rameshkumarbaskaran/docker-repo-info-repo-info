<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:2.0.20230207.0-with-sources`](#amazonlinux20202302070-with-sources)
-	[`amazonlinux:2.0.20230307.0`](#amazonlinux20202303070)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2018.03.0.20230207.0-with-sources`](#amazonlinux2018030202302070-with-sources)
-	[`amazonlinux:2018.03.0.20230306.1`](#amazonlinux2018030202303061)
-	[`amazonlinux:2023`](#amazonlinux2023)
-	[`amazonlinux:2023.0.20230308.0`](#amazonlinux20230202303080)
-	[`amazonlinux:devel`](#amazonlinuxdevel)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:89615436a3c65b5ff404cd47797ffa161762f5ca44eb8daa1ff79f46e8a04235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:448c749be9c4c1bf8fe31d4df3e4261cf51a503b6a752b808fb12d3e32a983a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62263014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e11ae717bbfb4b6f2a3530c9c080026b0bf1431e5a3f2a8eadf75f32bbaa1d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:20:50 GMT
COPY dir:dae6c6d350c29d0ccb0d00cb6456bd0a1110ea8d6a9d2decc204b29e1a988a1f in / 
# Fri, 10 Mar 2023 01:20:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:108f80a147fc26a1ca01b8ca8751b44dbbac2105a65bdec5ac8f03011747c558`  
		Last Modified: Fri, 10 Mar 2023 01:22:03 GMT  
		Size: 62.3 MB (62263014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:f6dc1046eb8d41c757177414c99b795644dc61483066dd074bd487fd1ae6971f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:db6f5b872cf347550fbc84997035060cb3f29b4092a502414aea35e1614a58d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515032600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de55c246e0ff336c46024f08fa4c8a76b99da444999c63a7a28e4590eafa6608`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Feb 2023 18:19:33 GMT
ADD file:f748cf37d9bb118581db4644923fc7f81aeac9af93188e42a5c85bbbba9770f0 in / 
# Fri, 10 Feb 2023 18:19:34 GMT
CMD ["/bin/bash"]
# Fri, 10 Feb 2023 18:19:59 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-2f3f7e5ea9b509a345d00531d4b8504f7720dde9cae889e01f4d4e8dbc71db34.tar.gz"     && echo "717d08c398cc28d075ab0ebe75c3785a5277a51c6ab89f5a959b7f1c7d2b98fa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:42f354128e7b08a45107942fd4ecc2977b7144b5ec9a6c343c288a99da208911`  
		Last Modified: Fri, 10 Feb 2023 18:20:39 GMT  
		Size: 62.3 MB (62267134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c8a964734f86273bdbe5f0d0815e887a76e38d1cdcd222072559d44584cef7`  
		Last Modified: Fri, 10 Feb 2023 18:21:31 GMT  
		Size: 452.8 MB (452765466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:8a3fbbbaf93665e495fd66e86c7c5d46de44ab0bc74460b97489820747e0a164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:814655abae4d4a99d56331869b05bad83c478aab39fccdd8518433fc502d7b17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62477005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af679e330749bc0062bcc833a2ad1935451f97141a92c4d2cd2a6b4ea1fa966`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:20:24 GMT
COPY dir:1fe253a28ffa7545ac05b2d6b2410c0b48083e8195b6557287b6a94e845122d3 in / 
# Fri, 10 Mar 2023 01:20:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:07e4d356f367b468402d36db62e60b734522576ce93a8e7246f1b36899c58f5e`  
		Last Modified: Thu, 09 Mar 2023 17:52:43 GMT  
		Size: 62.5 MB (62477005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c416e2994ff7eb6fa34d3e222ee1d981f1baa4df3721bb7514ea8e9da07de4ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64125204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6244a074eaf4d7a69992cbf81965e31de33a16cae44a5a54e94b18b27003d41b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:39:35 GMT
COPY dir:1997e4057e1f8b7df06806432d2b2c303c1f6ef5b18e8273d4393b867415d8b2 in / 
# Fri, 10 Mar 2023 01:39:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:042c9cfa8a36c0ffe86667a7dd7d488f78cbe295aa845213c01fdf8784165a92`  
		Last Modified: Fri, 10 Mar 2023 01:40:11 GMT  
		Size: 64.1 MB (64125204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:c4b2a5f5fb26e7450ea583866daabe17846bf5153dd32f528c87677fabb1e117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:3fa69e7667e2798b355efa1cb986e0ce87646a102faef7c1557982eb1b0411fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.7 MB (492732704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da14082e500f08e79e37c063e3ed02b7a4ddef1a580b553c91045fec60f0146`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 21:20:09 GMT
ADD file:29cd40b7c56d98385ece53bcbadfefd25bc70ccf0326777986ef6a5720bdfe83 in / 
# Thu, 16 Feb 2023 21:20:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 21:20:38 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-7e289542d782642b256d8350ebcc22b568c00303c6cedda53c0cc26f5de6cca4.tar.gz"     && echo "28173c8559de7e4838d9ae0e1c163243d6d1274f28d242ced6e7fa44272b36bb  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:d78505e615251c4f4af6eaa9507b67917d263d23551dcc5a1eed3c012d32a54d`  
		Last Modified: Wed, 15 Feb 2023 00:09:42 GMT  
		Size: 62.4 MB (62386320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e448b8061a833ba558b9628ae3dc088e3690f1a0c1624d5813333ca0224c06`  
		Last Modified: Thu, 16 Feb 2023 21:21:46 GMT  
		Size: 430.3 MB (430346384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ba3f1afa6fa0103b96d2c2d4a70a860e5e21426cc566d1fba15be4558808f5b9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.4 MB (494350183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b75bcfc11d633380eb8a00eaa5fbd5672efa3107a1d65f850b71dfea70bf46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 20:39:31 GMT
ADD file:17574026c2754afa903450c59a6d8f7d0905209b174cbe9c13252a61d5a6f916 in / 
# Thu, 16 Feb 2023 20:39:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 20:39:53 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-7e289542d782642b256d8350ebcc22b568c00303c6cedda53c0cc26f5de6cca4.tar.gz"     && echo "28173c8559de7e4838d9ae0e1c163243d6d1274f28d242ced6e7fa44272b36bb  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:71343c2791199c6e2c19c308cff6493497a02f57e225c11405e1934dc7428b3c`  
		Last Modified: Wed, 15 Feb 2023 03:16:17 GMT  
		Size: 64.0 MB (64003805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64a7d1a6cba2e41239f96a04c0f08457a2254983add1e7c6f48ed5668abad4b`  
		Last Modified: Thu, 16 Feb 2023 20:40:47 GMT  
		Size: 430.3 MB (430346378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20230207.0-with-sources`

```console
$ docker pull amazonlinux@sha256:c4b2a5f5fb26e7450ea583866daabe17846bf5153dd32f528c87677fabb1e117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20230207.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:3fa69e7667e2798b355efa1cb986e0ce87646a102faef7c1557982eb1b0411fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.7 MB (492732704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da14082e500f08e79e37c063e3ed02b7a4ddef1a580b553c91045fec60f0146`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 21:20:09 GMT
ADD file:29cd40b7c56d98385ece53bcbadfefd25bc70ccf0326777986ef6a5720bdfe83 in / 
# Thu, 16 Feb 2023 21:20:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 21:20:38 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-7e289542d782642b256d8350ebcc22b568c00303c6cedda53c0cc26f5de6cca4.tar.gz"     && echo "28173c8559de7e4838d9ae0e1c163243d6d1274f28d242ced6e7fa44272b36bb  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:d78505e615251c4f4af6eaa9507b67917d263d23551dcc5a1eed3c012d32a54d`  
		Last Modified: Wed, 15 Feb 2023 00:09:42 GMT  
		Size: 62.4 MB (62386320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e448b8061a833ba558b9628ae3dc088e3690f1a0c1624d5813333ca0224c06`  
		Last Modified: Thu, 16 Feb 2023 21:21:46 GMT  
		Size: 430.3 MB (430346384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20230207.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ba3f1afa6fa0103b96d2c2d4a70a860e5e21426cc566d1fba15be4558808f5b9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.4 MB (494350183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b75bcfc11d633380eb8a00eaa5fbd5672efa3107a1d65f850b71dfea70bf46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 20:39:31 GMT
ADD file:17574026c2754afa903450c59a6d8f7d0905209b174cbe9c13252a61d5a6f916 in / 
# Thu, 16 Feb 2023 20:39:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 20:39:53 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-7e289542d782642b256d8350ebcc22b568c00303c6cedda53c0cc26f5de6cca4.tar.gz"     && echo "28173c8559de7e4838d9ae0e1c163243d6d1274f28d242ced6e7fa44272b36bb  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:71343c2791199c6e2c19c308cff6493497a02f57e225c11405e1934dc7428b3c`  
		Last Modified: Wed, 15 Feb 2023 03:16:17 GMT  
		Size: 64.0 MB (64003805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64a7d1a6cba2e41239f96a04c0f08457a2254983add1e7c6f48ed5668abad4b`  
		Last Modified: Thu, 16 Feb 2023 20:40:47 GMT  
		Size: 430.3 MB (430346378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20230307.0`

```console
$ docker pull amazonlinux@sha256:8a3fbbbaf93665e495fd66e86c7c5d46de44ab0bc74460b97489820747e0a164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20230307.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:814655abae4d4a99d56331869b05bad83c478aab39fccdd8518433fc502d7b17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62477005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af679e330749bc0062bcc833a2ad1935451f97141a92c4d2cd2a6b4ea1fa966`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:20:24 GMT
COPY dir:1fe253a28ffa7545ac05b2d6b2410c0b48083e8195b6557287b6a94e845122d3 in / 
# Fri, 10 Mar 2023 01:20:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:07e4d356f367b468402d36db62e60b734522576ce93a8e7246f1b36899c58f5e`  
		Last Modified: Thu, 09 Mar 2023 17:52:43 GMT  
		Size: 62.5 MB (62477005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20230307.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c416e2994ff7eb6fa34d3e222ee1d981f1baa4df3721bb7514ea8e9da07de4ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64125204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6244a074eaf4d7a69992cbf81965e31de33a16cae44a5a54e94b18b27003d41b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:39:35 GMT
COPY dir:1997e4057e1f8b7df06806432d2b2c303c1f6ef5b18e8273d4393b867415d8b2 in / 
# Fri, 10 Mar 2023 01:39:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:042c9cfa8a36c0ffe86667a7dd7d488f78cbe295aa845213c01fdf8784165a92`  
		Last Modified: Fri, 10 Mar 2023 01:40:11 GMT  
		Size: 64.1 MB (64125204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:89615436a3c65b5ff404cd47797ffa161762f5ca44eb8daa1ff79f46e8a04235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:448c749be9c4c1bf8fe31d4df3e4261cf51a503b6a752b808fb12d3e32a983a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62263014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e11ae717bbfb4b6f2a3530c9c080026b0bf1431e5a3f2a8eadf75f32bbaa1d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:20:50 GMT
COPY dir:dae6c6d350c29d0ccb0d00cb6456bd0a1110ea8d6a9d2decc204b29e1a988a1f in / 
# Fri, 10 Mar 2023 01:20:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:108f80a147fc26a1ca01b8ca8751b44dbbac2105a65bdec5ac8f03011747c558`  
		Last Modified: Fri, 10 Mar 2023 01:22:03 GMT  
		Size: 62.3 MB (62263014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:f6dc1046eb8d41c757177414c99b795644dc61483066dd074bd487fd1ae6971f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:db6f5b872cf347550fbc84997035060cb3f29b4092a502414aea35e1614a58d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515032600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de55c246e0ff336c46024f08fa4c8a76b99da444999c63a7a28e4590eafa6608`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Feb 2023 18:19:33 GMT
ADD file:f748cf37d9bb118581db4644923fc7f81aeac9af93188e42a5c85bbbba9770f0 in / 
# Fri, 10 Feb 2023 18:19:34 GMT
CMD ["/bin/bash"]
# Fri, 10 Feb 2023 18:19:59 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-2f3f7e5ea9b509a345d00531d4b8504f7720dde9cae889e01f4d4e8dbc71db34.tar.gz"     && echo "717d08c398cc28d075ab0ebe75c3785a5277a51c6ab89f5a959b7f1c7d2b98fa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:42f354128e7b08a45107942fd4ecc2977b7144b5ec9a6c343c288a99da208911`  
		Last Modified: Fri, 10 Feb 2023 18:20:39 GMT  
		Size: 62.3 MB (62267134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c8a964734f86273bdbe5f0d0815e887a76e38d1cdcd222072559d44584cef7`  
		Last Modified: Fri, 10 Feb 2023 18:21:31 GMT  
		Size: 452.8 MB (452765466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20230207.0-with-sources`

```console
$ docker pull amazonlinux@sha256:f6dc1046eb8d41c757177414c99b795644dc61483066dd074bd487fd1ae6971f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20230207.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:db6f5b872cf347550fbc84997035060cb3f29b4092a502414aea35e1614a58d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515032600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de55c246e0ff336c46024f08fa4c8a76b99da444999c63a7a28e4590eafa6608`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Feb 2023 18:19:33 GMT
ADD file:f748cf37d9bb118581db4644923fc7f81aeac9af93188e42a5c85bbbba9770f0 in / 
# Fri, 10 Feb 2023 18:19:34 GMT
CMD ["/bin/bash"]
# Fri, 10 Feb 2023 18:19:59 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-2f3f7e5ea9b509a345d00531d4b8504f7720dde9cae889e01f4d4e8dbc71db34.tar.gz"     && echo "717d08c398cc28d075ab0ebe75c3785a5277a51c6ab89f5a959b7f1c7d2b98fa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:42f354128e7b08a45107942fd4ecc2977b7144b5ec9a6c343c288a99da208911`  
		Last Modified: Fri, 10 Feb 2023 18:20:39 GMT  
		Size: 62.3 MB (62267134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c8a964734f86273bdbe5f0d0815e887a76e38d1cdcd222072559d44584cef7`  
		Last Modified: Fri, 10 Feb 2023 18:21:31 GMT  
		Size: 452.8 MB (452765466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20230306.1`

```console
$ docker pull amazonlinux@sha256:89615436a3c65b5ff404cd47797ffa161762f5ca44eb8daa1ff79f46e8a04235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20230306.1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:448c749be9c4c1bf8fe31d4df3e4261cf51a503b6a752b808fb12d3e32a983a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62263014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e11ae717bbfb4b6f2a3530c9c080026b0bf1431e5a3f2a8eadf75f32bbaa1d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:20:50 GMT
COPY dir:dae6c6d350c29d0ccb0d00cb6456bd0a1110ea8d6a9d2decc204b29e1a988a1f in / 
# Fri, 10 Mar 2023 01:20:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:108f80a147fc26a1ca01b8ca8751b44dbbac2105a65bdec5ac8f03011747c558`  
		Last Modified: Fri, 10 Mar 2023 01:22:03 GMT  
		Size: 62.3 MB (62263014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2023`

```console
$ docker pull amazonlinux@sha256:40099aa7e8a1c8fd0498c45c03701f87520febe057a1bc6e71533c628f0a209c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2023` - linux; amd64

```console
$ docker pull amazonlinux@sha256:136a4b1264cc6ed6ad79eaac8b46b452f8654a6b5dc0df5a689538d5bd3ba907
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52261018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56f21ae4a425a04bef44a111ef8cc259f4632a7664041f59ffa61d7f0fc09bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:21:12 GMT
COPY dir:5fe30ccb145d29c8a93766ddbab23bb46d7fb772c29d47014b64bbc9a69b338e in / 
# Fri, 10 Mar 2023 01:21:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:af0f8926184513efe1c86bb309b7494a281bd5ceef3241dcaddbb4bd20f1f01b`  
		Last Modified: Thu, 09 Mar 2023 03:14:23 GMT  
		Size: 52.3 MB (52261018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2023` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:2eabb25d27e9b904d0e529479d110a64ce6a39f289e8711937b4ca7082fbe439
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51299744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b138fd4aa1948f80bdde1770426f703a1213c00145da6140f702b1d77c70db59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:39:50 GMT
COPY dir:a24ad6b5b7163d40d0095f8f28e004ddd962d1da1d45bef3bc712de6d01d91e4 in / 
# Fri, 10 Mar 2023 01:39:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff3e2ba455bc4e3e777721593e5fa68d0805fc5a887bec00bf39724570b1a16b`  
		Last Modified: Thu, 09 Mar 2023 03:14:08 GMT  
		Size: 51.3 MB (51299744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2023.0.20230308.0`

```console
$ docker pull amazonlinux@sha256:40099aa7e8a1c8fd0498c45c03701f87520febe057a1bc6e71533c628f0a209c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2023.0.20230308.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:136a4b1264cc6ed6ad79eaac8b46b452f8654a6b5dc0df5a689538d5bd3ba907
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52261018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56f21ae4a425a04bef44a111ef8cc259f4632a7664041f59ffa61d7f0fc09bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:21:12 GMT
COPY dir:5fe30ccb145d29c8a93766ddbab23bb46d7fb772c29d47014b64bbc9a69b338e in / 
# Fri, 10 Mar 2023 01:21:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:af0f8926184513efe1c86bb309b7494a281bd5ceef3241dcaddbb4bd20f1f01b`  
		Last Modified: Thu, 09 Mar 2023 03:14:23 GMT  
		Size: 52.3 MB (52261018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2023.0.20230308.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:2eabb25d27e9b904d0e529479d110a64ce6a39f289e8711937b4ca7082fbe439
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51299744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b138fd4aa1948f80bdde1770426f703a1213c00145da6140f702b1d77c70db59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:39:50 GMT
COPY dir:a24ad6b5b7163d40d0095f8f28e004ddd962d1da1d45bef3bc712de6d01d91e4 in / 
# Fri, 10 Mar 2023 01:39:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff3e2ba455bc4e3e777721593e5fa68d0805fc5a887bec00bf39724570b1a16b`  
		Last Modified: Thu, 09 Mar 2023 03:14:08 GMT  
		Size: 51.3 MB (51299744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel`

```console
$ docker pull amazonlinux@sha256:40099aa7e8a1c8fd0498c45c03701f87520febe057a1bc6e71533c628f0a209c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel` - linux; amd64

```console
$ docker pull amazonlinux@sha256:136a4b1264cc6ed6ad79eaac8b46b452f8654a6b5dc0df5a689538d5bd3ba907
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52261018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56f21ae4a425a04bef44a111ef8cc259f4632a7664041f59ffa61d7f0fc09bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:21:12 GMT
COPY dir:5fe30ccb145d29c8a93766ddbab23bb46d7fb772c29d47014b64bbc9a69b338e in / 
# Fri, 10 Mar 2023 01:21:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:af0f8926184513efe1c86bb309b7494a281bd5ceef3241dcaddbb4bd20f1f01b`  
		Last Modified: Thu, 09 Mar 2023 03:14:23 GMT  
		Size: 52.3 MB (52261018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:2eabb25d27e9b904d0e529479d110a64ce6a39f289e8711937b4ca7082fbe439
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51299744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b138fd4aa1948f80bdde1770426f703a1213c00145da6140f702b1d77c70db59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:39:50 GMT
COPY dir:a24ad6b5b7163d40d0095f8f28e004ddd962d1da1d45bef3bc712de6d01d91e4 in / 
# Fri, 10 Mar 2023 01:39:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff3e2ba455bc4e3e777721593e5fa68d0805fc5a887bec00bf39724570b1a16b`  
		Last Modified: Thu, 09 Mar 2023 03:14:08 GMT  
		Size: 51.3 MB (51299744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:8a3fbbbaf93665e495fd66e86c7c5d46de44ab0bc74460b97489820747e0a164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:814655abae4d4a99d56331869b05bad83c478aab39fccdd8518433fc502d7b17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62477005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af679e330749bc0062bcc833a2ad1935451f97141a92c4d2cd2a6b4ea1fa966`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:20:24 GMT
COPY dir:1fe253a28ffa7545ac05b2d6b2410c0b48083e8195b6557287b6a94e845122d3 in / 
# Fri, 10 Mar 2023 01:20:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:07e4d356f367b468402d36db62e60b734522576ce93a8e7246f1b36899c58f5e`  
		Last Modified: Thu, 09 Mar 2023 17:52:43 GMT  
		Size: 62.5 MB (62477005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c416e2994ff7eb6fa34d3e222ee1d981f1baa4df3721bb7514ea8e9da07de4ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64125204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6244a074eaf4d7a69992cbf81965e31de33a16cae44a5a54e94b18b27003d41b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:39:35 GMT
COPY dir:1997e4057e1f8b7df06806432d2b2c303c1f6ef5b18e8273d4393b867415d8b2 in / 
# Fri, 10 Mar 2023 01:39:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:042c9cfa8a36c0ffe86667a7dd7d488f78cbe295aa845213c01fdf8784165a92`  
		Last Modified: Fri, 10 Mar 2023 01:40:11 GMT  
		Size: 64.1 MB (64125204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:c4b2a5f5fb26e7450ea583866daabe17846bf5153dd32f528c87677fabb1e117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:3fa69e7667e2798b355efa1cb986e0ce87646a102faef7c1557982eb1b0411fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.7 MB (492732704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da14082e500f08e79e37c063e3ed02b7a4ddef1a580b553c91045fec60f0146`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 21:20:09 GMT
ADD file:29cd40b7c56d98385ece53bcbadfefd25bc70ccf0326777986ef6a5720bdfe83 in / 
# Thu, 16 Feb 2023 21:20:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 21:20:38 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-7e289542d782642b256d8350ebcc22b568c00303c6cedda53c0cc26f5de6cca4.tar.gz"     && echo "28173c8559de7e4838d9ae0e1c163243d6d1274f28d242ced6e7fa44272b36bb  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:d78505e615251c4f4af6eaa9507b67917d263d23551dcc5a1eed3c012d32a54d`  
		Last Modified: Wed, 15 Feb 2023 00:09:42 GMT  
		Size: 62.4 MB (62386320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e448b8061a833ba558b9628ae3dc088e3690f1a0c1624d5813333ca0224c06`  
		Last Modified: Thu, 16 Feb 2023 21:21:46 GMT  
		Size: 430.3 MB (430346384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ba3f1afa6fa0103b96d2c2d4a70a860e5e21426cc566d1fba15be4558808f5b9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.4 MB (494350183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b75bcfc11d633380eb8a00eaa5fbd5672efa3107a1d65f850b71dfea70bf46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 20:39:31 GMT
ADD file:17574026c2754afa903450c59a6d8f7d0905209b174cbe9c13252a61d5a6f916 in / 
# Thu, 16 Feb 2023 20:39:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 20:39:53 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-7e289542d782642b256d8350ebcc22b568c00303c6cedda53c0cc26f5de6cca4.tar.gz"     && echo "28173c8559de7e4838d9ae0e1c163243d6d1274f28d242ced6e7fa44272b36bb  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:71343c2791199c6e2c19c308cff6493497a02f57e225c11405e1934dc7428b3c`  
		Last Modified: Wed, 15 Feb 2023 03:16:17 GMT  
		Size: 64.0 MB (64003805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64a7d1a6cba2e41239f96a04c0f08457a2254983add1e7c6f48ed5668abad4b`  
		Last Modified: Thu, 16 Feb 2023 20:40:47 GMT  
		Size: 430.3 MB (430346378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

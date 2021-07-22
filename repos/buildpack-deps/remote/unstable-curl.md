## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:deda89917c68b331d0a576f387e29d0a848a75493e39ab65a894c508182a7e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:02f2a10a3b60bc1dada0e530f00238b5b5fa53b3d005f72cb3ee65aefca5db7d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70952951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b48862eb062e9cda42cf52a979a9e30369b6f2930ec98e7b82b7309c63b1f0f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:46:20 GMT
ADD file:cac9ad9d988141c80929e8c31f4cb388618dac0bbc048d4c5e3b8029c85c576d in / 
# Thu, 22 Jul 2021 00:46:21 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:13:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:13:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:531fc43e70accbfd0e52721b79cfd564769d6f1b7e64a98e9f670327d4c4820e`  
		Last Modified: Thu, 22 Jul 2021 00:51:36 GMT  
		Size: 54.9 MB (54909299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3334cfec756c2189b8a7cce5cd3ddf363b2acfc7b8a38f1ccf8cdbe4ef115`  
		Last Modified: Thu, 22 Jul 2021 01:21:10 GMT  
		Size: 5.2 MB (5171133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284c0769674315a1486ea9eee2a7dbe2a630850d90b8e445a2b8d7034528be1b`  
		Last Modified: Thu, 22 Jul 2021 01:21:10 GMT  
		Size: 10.9 MB (10872519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:edf5fa9d4767275003022dc627b2afb2d85957ec2ac4eae7e118fce949848181
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68093375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd2561c5f55824c80adec8586426bc4af358f51ed5307b74b0be821ff1c4be3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:51:25 GMT
ADD file:7b9b18b6a1a6deb81eb9bf8638d60de26198ba106aaa757dfb838b264fc90252 in / 
# Thu, 22 Jul 2021 00:51:26 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 02:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 02:07:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9de879dbb26d0cc624c499f5907a14117d0f357e4e39699d3208c57d5091b537`  
		Last Modified: Thu, 22 Jul 2021 01:04:16 GMT  
		Size: 52.4 MB (52445986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef97169c47ca52a8e66f6ef70d0a4d9e5cfae0f8b72d1937ac646b3bdf48d8a`  
		Last Modified: Thu, 22 Jul 2021 02:24:13 GMT  
		Size: 5.1 MB (5075544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e445910f582e1f6da040a3bdd8886f00fcc077bf63486317b6de7c17cf3ba01`  
		Last Modified: Thu, 22 Jul 2021 02:24:15 GMT  
		Size: 10.6 MB (10571845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:39419db02bf8a4e591f47a803a410ecf096d2f6b5df05ee3cbad85bfa089250b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65259139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea97c74f3a267a4ac846bf0ac5a876d207dc8be3e1f2414638b239e4fd27bf09`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:21:40 GMT
ADD file:10ae021b5b2998c7ee0904a6d9b6a3697ef580d3a6b0a0980c2f209a6ad2bb29 in / 
# Wed, 23 Jun 2021 00:21:42 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 05:49:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 05:49:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2bb9348ee5f2e424d70e44ac1d1e0b029bb37d72f6050453f93408edc2af9176`  
		Last Modified: Wed, 23 Jun 2021 00:33:47 GMT  
		Size: 50.1 MB (50105618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc10d3401b65a0651a08c5c29f2e1207dc4ca1027e80abc9b35cf15c88d96958`  
		Last Modified: Wed, 23 Jun 2021 06:21:43 GMT  
		Size: 4.9 MB (4936190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5dd2865193f1b761bf000f90190639fb8bfea0ce5033bf2de30ad2d9738789`  
		Last Modified: Wed, 23 Jun 2021 06:21:45 GMT  
		Size: 10.2 MB (10217331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1918349c0bc2c220cd9d0be7eae70ab2fab2c78f89888c8a145a8c246907c915
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69626197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d79180962c9cf3f7ad0998b324767aac48fad08a792766a7909e4a95ccc6a4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:46 GMT
ADD file:a3549e948b3f56a447f7f9b8c10f86c1915a2f52c546e1e7891735ee86a647ee in / 
# Thu, 22 Jul 2021 00:40:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:17:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:17:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:62e8b52de22392fa7c459ae1bacaf43117fdae59adb2ad8b421412ace5a516b1`  
		Last Modified: Thu, 22 Jul 2021 00:47:01 GMT  
		Size: 53.6 MB (53593074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f26cc7a118272da0a6d22d8d2788a1a25d2f7e416cfda133a48219a5f1fced3`  
		Last Modified: Thu, 22 Jul 2021 01:26:21 GMT  
		Size: 5.2 MB (5159864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d208ca6539dbf6b41a01d767eb9b2904ee7a991935f60f061cd678987bc3b4d`  
		Last Modified: Thu, 22 Jul 2021 01:26:22 GMT  
		Size: 10.9 MB (10873259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9d3d8ad6c733d091f86b09ba9f1e057b7316a0524fa79855b9414aeccd4a55ee
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72465330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76bfbdf36c75c6fde2db899c0b977634ecf1447ebedc2b058db62a6c4017989c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 22 Jun 2021 23:40:18 GMT
ADD file:20378fd7bc859874d8620bd807402968cbe571a1ca281d0f344392ed5d8af55b in / 
# Tue, 22 Jun 2021 23:40:18 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 00:11:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ff9feaae647f307940e0b5cfdb30f3d3a877220cd3394859c1af4b3d653b2e97`  
		Last Modified: Tue, 22 Jun 2021 23:47:46 GMT  
		Size: 55.9 MB (55914853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5310b9c9dfb8fd34f5ff4cccb1d7af5e1baf20620d64357dc51a0e69717717e`  
		Last Modified: Wed, 23 Jun 2021 00:19:34 GMT  
		Size: 5.3 MB (5299879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab8c3b07912881a8d38f2ca51a04fef6fa1d22c0163da069cd226eec7362a07`  
		Last Modified: Wed, 23 Jun 2021 00:19:35 GMT  
		Size: 11.3 MB (11250598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9574c023c1bd1d12c66b471db94f95c90303711848b34d1757fad4cf185c6a24
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69165997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b353911a5e0986a17337cd29fb8e2c9509b62bfbd1f7a09800bdd6533689a35`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:10:12 GMT
ADD file:21823f99ac9631853baf61992ae48f9aaefd9aa14689bdad76945cbe790d4b23 in / 
# Thu, 22 Jul 2021 00:10:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 00:46:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 00:47:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b7674bbd759fec6741d7d94cfebb5e0cf54c599cb2a824313eb96b1d6622a44b`  
		Last Modified: Thu, 22 Jul 2021 00:16:59 GMT  
		Size: 53.2 MB (53162150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bbf92e62547174ba9022d0c0fe12fa84126289620f8148cf33269681b8273c`  
		Last Modified: Thu, 22 Jul 2021 00:57:29 GMT  
		Size: 5.1 MB (5130754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2614779dff3229eb62dc8a974d88a9bf60cfd085721871ad71d642e0517eb35`  
		Last Modified: Thu, 22 Jul 2021 00:57:31 GMT  
		Size: 10.9 MB (10873093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0e9a444c284bc7d71f7102e6b3653b8a43669895f51147fb87969389cd37bc62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75861320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc307aa2b27361e54d29958fb8a2e8bc0b0cfeda19c39970fc62d1839924b9a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jul 2021 15:58:42 GMT
ADD file:9d5a0ba0a24f9a37f3d9812637e4beef52ef27fa65d76c97dffa3f4933633701 in / 
# Fri, 09 Jul 2021 15:58:46 GMT
CMD ["bash"]
# Sat, 10 Jul 2021 06:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Jul 2021 06:41:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:28a36a9b0ca23da4474256976c303c139c5800da883d61fb1e52bc74123ba134`  
		Last Modified: Wed, 23 Jun 2021 00:37:34 GMT  
		Size: 58.8 MB (58812906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c65c32ac33fcec60fedd0b9e713bcf0f7b704d59b14cce6afa4a06e55e315a1`  
		Last Modified: Sat, 10 Jul 2021 07:07:55 GMT  
		Size: 5.4 MB (5421908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57141b1c3dd2e33c1dc87ff3220529d62b3a28a6e52333c04f525f64ebea0006`  
		Last Modified: Sat, 10 Jul 2021 07:07:56 GMT  
		Size: 11.6 MB (11626506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fac536b3c6f07105694e183188dc5fe41b46d71d77661b0d22e2c84328f51de2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65676291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b70d5cb96b55f82794824cd09dc2408db20dcff5465555b723d60309b0f3fc0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:15:18 GMT
ADD file:b4e98baa24988a55379e3fdf724731b1139785071c1e2ca5d8e5adb43be85150 in / 
# Thu, 22 Jul 2021 00:15:21 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:01:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:02:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f89739902ab20ca21252189bdcfa682d2d8fa5c61d2bb714fe2fa6f3a5c519eb`  
		Last Modified: Thu, 22 Jul 2021 00:34:31 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfc4d529e1e9e4423209e8cd25e27a2a6f2936444c4aefe731dff4f2182309a`  
		Last Modified: Thu, 22 Jul 2021 01:24:42 GMT  
		Size: 5.0 MB (4984778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31856dffc5e9c49615c1b03c06dd7711260172bc519c1d48536e27cbf15fadc3`  
		Last Modified: Thu, 22 Jul 2021 01:24:46 GMT  
		Size: 10.3 MB (10293785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6fbaa6f3af6f8a8fd5e119be7497d847276104624486574942dc04f00e3a00d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69103880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3b336957e866e5a8b73b5dd64b491d35f66e4bda13e2756e0ee260433323ad`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:43:01 GMT
ADD file:eb0fa0f991634817ac5af2d4e957d8d14c8fb5a8d501cfeb56949d715ca84f1c in / 
# Thu, 22 Jul 2021 00:43:08 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:16:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:730f0cea2dc4896e7a1a70e4e4e14165f66e42bcd880b7b7242a68c9d2ffa297`  
		Last Modified: Thu, 22 Jul 2021 00:48:31 GMT  
		Size: 53.2 MB (53187330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7d1fd11d3f6b43667d4ca70d209f8ae22c2e40a78c9c810ae7a0f944c04b98`  
		Last Modified: Thu, 22 Jul 2021 01:28:41 GMT  
		Size: 5.2 MB (5152875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082a8f611511094fa5cccaf153c7a6dd4dde6a330473614087e039fa44ca58fe`  
		Last Modified: Thu, 22 Jul 2021 01:28:42 GMT  
		Size: 10.8 MB (10763675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

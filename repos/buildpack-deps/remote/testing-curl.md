## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:a14c169416a313daef7f3f2fbeffef1b0290f08fdd1b89116a29c6303ac2457a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:557e408b13e9e176ea6899ebf4cac90b543cb268bb61072c95fb627ff6487510
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71077922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a011dd3d5bdc20bc84350adb940dbd9308198125815a345e88f05e8242f3b39`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:37:11 GMT
ADD file:96a5f24c28b0ba6960064c54e4643bc56eb6890db2c214c7d54bff6a00f9f049 in / 
# Tue, 13 Oct 2020 01:37:11 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:12:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:12:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:831751213a615bc3a20e0080e123bd3a2f1f1eef137b680b3101f3127cdff08e`  
		Last Modified: Tue, 13 Oct 2020 01:47:33 GMT  
		Size: 52.6 MB (52579873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0865ee0fc4d919fc9d8f50091271f48b9d93d23451b3b03fac42f42c4e96fa1f`  
		Last Modified: Tue, 13 Oct 2020 02:27:31 GMT  
		Size: 7.9 MB (7870921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bd8b5719c34db0bfc0bc2bf3ed420adc1b98d9bd7b52a7210a5b240141fcfa`  
		Last Modified: Tue, 13 Oct 2020 02:27:31 GMT  
		Size: 10.6 MB (10627128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:07337b1fb4e1a050a01a28c70a6f19c384bc55d623012e2f646406716dbf975c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68480969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afcffb53f41ea9c35444359876e717c1db0bee3b3cef5fa36420d8f61d96a9cd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:15 GMT
ADD file:1825c9ae9f20eb2576f772d68892699ef4ca90dff36b8f247bf78ce04ad41a91 in / 
# Tue, 17 Nov 2020 20:19:17 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:35:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:35:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8172f634b664f563947e1ba480d8a7e04acd125ff144bde0dabb4ef26db6d3b1`  
		Last Modified: Tue, 17 Nov 2020 20:29:25 GMT  
		Size: 53.2 MB (53174409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a9bcac9e1b17a227267b364ec33a309b567898a11a1049896dfb513508befa`  
		Last Modified: Tue, 17 Nov 2020 22:05:34 GMT  
		Size: 5.0 MB (4974569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af90ca1b550dfe775778350f5133681fd06314fe43ae77642bada174068cdcf`  
		Last Modified: Tue, 17 Nov 2020 22:05:35 GMT  
		Size: 10.3 MB (10331991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:327a75076720d8302af551179974b3a740913b101d2a0d189ab664943cc05b12
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65566557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02129e421f84ba6ecd8cb86b67763f763a36a44ab8160343f6db9035a2e3bb03`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:26 GMT
ADD file:f2393813e8311e27cf255e78079f523184619c1ee8ff9ccdf51a5cbc61751e1b in / 
# Tue, 17 Nov 2020 20:19:29 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:36:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:907906fd9e2e517e45080a90701520c1c3c654647630763a4cd9f181ae039252`  
		Last Modified: Tue, 17 Nov 2020 20:30:29 GMT  
		Size: 50.8 MB (50756959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644a164f19b5f5e429261a5effb8cbcbbe66d7f6da9e93d9ff34b86f08ed6a42`  
		Last Modified: Tue, 17 Nov 2020 22:04:14 GMT  
		Size: 4.8 MB (4838545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d419d3ef4e0a73ebe3cf3ced0bfa50e1e9961d81ecb60e542323b9bc441e6d`  
		Last Modified: Tue, 17 Nov 2020 22:04:15 GMT  
		Size: 10.0 MB (9971053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:870139afc1cb87556f26207220299fce426670eeeed8a5e0c6cb009058073b71
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70027433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3814727203cde5bc983464b469a64e78c85da5a9db352c94001548018e1702`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:22:08 GMT
ADD file:58908becb64a88c580fc5d9fea54a7e73507d1e537e70b5567f5d58c26ad000d in / 
# Tue, 17 Nov 2020 20:22:10 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:15:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:15:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:df1866c47e1fa1c26619e32544732be4853c6b58bfe5ea76c192ae970daf5da7`  
		Last Modified: Tue, 17 Nov 2020 20:30:56 GMT  
		Size: 54.3 MB (54323419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a71907b4dd26e793f4e9841e590a1a930f7265a02f7c07e57767ef9cbe91f8b`  
		Last Modified: Tue, 17 Nov 2020 22:33:52 GMT  
		Size: 5.1 MB (5055744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2cf86d1130240ba8633c0151d4a4a4b9e6a251bf8ec2bf14d72ce40a67727c`  
		Last Modified: Tue, 17 Nov 2020 22:33:53 GMT  
		Size: 10.6 MB (10648270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:93645a41feb122feacb627e89053c2f9185ed53b9d5888807b98a1d7ac871a8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72934261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab27d76004ea3ba93d35c81b36b5b124ff3ae1fea133c804e95c90be36fb7770`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:01 GMT
ADD file:df88ece8f6b35ea6811921d958952eb8431b76449597cb6d5151e88c62167964 in / 
# Tue, 17 Nov 2020 20:19:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:01:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:01:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d9137c9a05e5bbf8d80413499157abbe788cac975a7926ded72bd9ff285f7520`  
		Last Modified: Tue, 17 Nov 2020 20:25:46 GMT  
		Size: 56.7 MB (56728874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbd9994454c4b84708c2d9754f396aac9f662a7169c2322418210f8d161ac4d`  
		Last Modified: Tue, 17 Nov 2020 21:22:12 GMT  
		Size: 5.2 MB (5182817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87786a5db1b57a9ac7c14addd518c4d55f9ac878f951e8110866257d83d6d82c`  
		Last Modified: Tue, 17 Nov 2020 21:22:13 GMT  
		Size: 11.0 MB (11022570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3455aea8071309ba649d5309af1f2992d031fc76f2f542a0e84057a9d5edc8ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69540370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84936a715fec6a6d95d08f0c67b27b595fb1711d8091451fec1b6f45de5dd8cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:18:02 GMT
ADD file:b3efb0da03cf858a9bc305dec420c5a2fd85b3ba7212cd26f4012b931492bcc2 in / 
# Tue, 17 Nov 2020 20:18:03 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:34:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:34:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b53392aabcbd30c0ebb343f6223dffd1e0d3a034f1683d60ac80a65254522359`  
		Last Modified: Tue, 17 Nov 2020 20:24:23 GMT  
		Size: 53.9 MB (53861718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58b5272c361da3f94922fc2e154b2c7092b6abb657a2857ef7684f41294c60e`  
		Last Modified: Tue, 17 Nov 2020 22:48:33 GMT  
		Size: 5.0 MB (5025865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03528b3943b7f8558ee96ae85f7871910f47c9b5f5e89e078ae6da0783a2ff3`  
		Last Modified: Tue, 17 Nov 2020 22:48:36 GMT  
		Size: 10.7 MB (10652787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c5cf3189687056927cbe4595c765bf7d07921ebc09c49aff670075b462e10ceb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76185814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615d79004b8e9de67dc274cce692bed4e750940b5383b59f639bbc953bcdbd59`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:36:17 GMT
ADD file:29c9502df00306ab143f7a4895ecbd5188710e18fa501d1931dfffe0d2281c6f in / 
# Tue, 13 Oct 2020 01:36:23 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 08:44:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 08:45:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e449e1f1ecdd90acbe5e4ea9a9f941aa8dcee06a83eb2eff72fe4dd55cc20576`  
		Last Modified: Tue, 13 Oct 2020 01:47:12 GMT  
		Size: 56.5 MB (56486527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b868bd306c5ff6ba6bbe52fb1cc3deaa47fed5a1362d135d89cfca87a684e4a4`  
		Last Modified: Tue, 13 Oct 2020 09:29:49 GMT  
		Size: 8.3 MB (8307201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca5bd324b7e56f3121bd85c3a06132da98d95654678c2a01b4439cab8adc5b5`  
		Last Modified: Tue, 13 Oct 2020 09:29:49 GMT  
		Size: 11.4 MB (11392086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6a85ef1c23571644452eecd6858e49b1805e745587e4d503c967e972ba9b2286
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69368901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da2ae2bd32da076d1afbafb8468f9bc49dc76fb205c5dadd91211db8e863247`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:17:06 GMT
ADD file:b2aa936914932ddd337990ffdd06ceff2628d7198e962be967a9781efaba51d9 in / 
# Tue, 17 Nov 2020 20:17:17 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:25:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:25:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:069a0f569bbab3514d40a8e2575a33e70926c0aeacc9099b083427a84cafc126`  
		Last Modified: Tue, 17 Nov 2020 20:22:44 GMT  
		Size: 53.8 MB (53806147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e0c6c52e6336a9fffb0f96f9bb643f4f181052948188c1e0453ed3ab253217`  
		Last Modified: Tue, 17 Nov 2020 21:43:23 GMT  
		Size: 5.0 MB (5048357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce85daf872edba752735571ddb26859c12b6e958818465881a345aa93faeef1`  
		Last Modified: Tue, 17 Nov 2020 21:43:23 GMT  
		Size: 10.5 MB (10514397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

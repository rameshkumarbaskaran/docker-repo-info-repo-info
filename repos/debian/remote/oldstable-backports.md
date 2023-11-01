## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:6266500cb884e490fd47c73927240e093e90f044676ccfd3edbf0448b72919ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:bebd18bdf6c6fb1392e424f8b8ab830d69b3d09a41af3bd74773c93545372678
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55058322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6988002241c131bf5fd8a90ba323a99dd0eada326e0d1f5911c22e6c2139f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:06 GMT
ADD file:30b9dcfcd946b137141d7c5c2edcb9d0817dbdd07b9a6951031ee071ca2e2894 in / 
# Wed, 01 Nov 2023 00:22:06 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:22:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:41bc806f354b99a3f6009571ba6c37f6532fd5828fa506fd50fced3b011f35b5`  
		Last Modified: Wed, 01 Nov 2023 00:27:52 GMT  
		Size: 55.1 MB (55058095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cad93d1666898656190584faf83c3f1f4048c7f369d01c5611d678be153ea67`  
		Last Modified: Wed, 01 Nov 2023 00:28:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:434160a4e353c6e2c523ce24aadc43af9a65f89fa64cf84e9dbbe0d8b6a35f11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52563365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951fc455f579d55b50ce4e9fb6a7ac2eb8d32366cd1b26f09fedf446bd4a17ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:38:06 GMT
ADD file:da1ec7816bb4779ff99eeaf749c3b64e98dbb058fb9b388970e70e6f0429ca30 in / 
# Wed, 11 Oct 2023 17:38:07 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:38:09 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:898468ed91f754fb929ec7597c79f49e3b926e76e037a02d099b5efc966c5435`  
		Last Modified: Wed, 11 Oct 2023 17:41:52 GMT  
		Size: 52.6 MB (52563140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4e68980b4aeb49b8ae7026ab17402966f4f0b0559121b1bd110c7d22f0a94b`  
		Last Modified: Wed, 11 Oct 2023 17:42:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:cd1ba5f77ca06712bfe9f0906e7d208e03e0e35131bba1dc15751780b5a2fd45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50215953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5b6cef0639f2ceecb0ad62bc975a5b3e041521e7e2e2df968947b5563bc44c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:43:15 GMT
ADD file:010bde6be30784c390d5138fd9cd7c469ad66c671eeefeb13c0e3c5186b70d86 in / 
# Wed, 11 Oct 2023 17:43:15 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:43:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cb4669bc4f8e091586991944d88167c76cb15c78accb55788140ac1b9b3250f9`  
		Last Modified: Wed, 11 Oct 2023 17:48:45 GMT  
		Size: 50.2 MB (50215725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e0032f4096be8d6bda80f0f95a994730169e3f77c407258cef3c93419431f7`  
		Last Modified: Wed, 11 Oct 2023 17:48:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8fd4609e11ddcb83b24ed495e019fb95ce1aa2a20c3f155a0a5000e775b8145b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53708054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b11e48820af385a4bd7a70c028ce9bcd29cf7375256f9fa8fde3834ab4544a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:42 GMT
ADD file:3629f45242132f524ae9634afa36ea583bab2ffcb6ce49c842d92077add4c489 in / 
# Wed, 11 Oct 2023 18:25:42 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:25:45 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d1245b9fa820f4d2ddf78e7bad6329a51b3d8fdc1cceb450907259035c7e0473`  
		Last Modified: Wed, 11 Oct 2023 18:30:40 GMT  
		Size: 53.7 MB (53707827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe3116900dbf202b3a89d0a4d988a99bb3047b62e0aa3ed61625b4c02789c50`  
		Last Modified: Wed, 11 Oct 2023 18:30:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:ccffa478aab20cc8e8da61cdfe3993c7b72766e9cdefefd6c777930cb2d58cf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56046559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535940e9176c0ca78db707193f44884f84ffee522881f6df63179818787d91b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:58 GMT
ADD file:fbb4026de842788be138f442c68c97c4cd9f05fbe7e282eb2a1bec5508f411c5 in / 
# Wed, 11 Oct 2023 17:41:59 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:42:02 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a4036d421c6eaaaaafb97abc75064e1210fdd67750a5efbda6e3aa357d14a344`  
		Last Modified: Wed, 11 Oct 2023 17:48:22 GMT  
		Size: 56.0 MB (56046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80f8954bd43ebf0e9403e42d04fdfcee8637ba2810f0c095aea1c5f54cd1ab6`  
		Last Modified: Wed, 11 Oct 2023 17:48:34 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:b6574b6d93136d6829fa35ac573a2b56466b986cdcc80b6b888e05c6e70e3215
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53289261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8021769bee64a371938659a9cc9397d00da3015118d74f9fc2c655caf0af9ec8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:51:24 GMT
ADD file:ffbea6ab30b7fadd815d53bb877e69b127714ea9976b06db2bc05bec98962215 in / 
# Wed, 11 Oct 2023 17:51:31 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:51:43 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e9dd1c85503ac6114304b94839ac51b6680fe86f0655e8a065dae67b6f39d32c`  
		Last Modified: Wed, 11 Oct 2023 18:02:50 GMT  
		Size: 53.3 MB (53289034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1260349e339ac2822ae504b7ab5a6b0a0dd90ebe629ab4b7884ddc5435527e36`  
		Last Modified: Wed, 11 Oct 2023 18:03:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:723a6e384bddf0b80c9537db3363e11c06e8aea5eecd8fccedbbaa1ce98e202f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58929728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e2807368a47550ead81037d908248b81ea9471d56f5047994f9df484443b93`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:21 GMT
ADD file:eaa1db56a0b20b30b76d393ee69a4e7481d866f926db0a129dd2e15db7ffabed in / 
# Wed, 01 Nov 2023 00:22:24 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:22:27 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2d17f706dc2e5f6d2c2df15c6a255acc0283efa6f95faedb0621adf8af6827bf`  
		Last Modified: Wed, 01 Nov 2023 00:27:20 GMT  
		Size: 58.9 MB (58929501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0346bb2356966bbb2c864a3a56628cee0bc4ac0758bcc8a9bd9f0a3016c79438`  
		Last Modified: Wed, 01 Nov 2023 00:27:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:17e12bff615831fa340bf347958bd1db78853cee18477d84b65e641f8246b198
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53296560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63b3495b299326adc0a6f6f9bcc5ee2a9acbdec03d5e7cf42cfab1750dd55d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:51:11 GMT
ADD file:5c0693dfa39dd52d24f19239d55e43f0d2af245a32ae838ab8f32cf565c738e1 in / 
# Wed, 11 Oct 2023 17:51:15 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:51:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:035365d8ea846b3f48e8ae9876bee8e58e3af876d6745beefa24a3ab58db0c74`  
		Last Modified: Wed, 11 Oct 2023 17:58:08 GMT  
		Size: 53.3 MB (53296335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b185611ba09069c6e9b0d304aac44e6f29dc911fc62f50207afe932ab62adf25`  
		Last Modified: Wed, 11 Oct 2023 17:58:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

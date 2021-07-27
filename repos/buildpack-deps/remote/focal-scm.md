## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:34b8b4d213f734b92fee7e318a934a2875db30bdd993c5d3a3445699c13d9a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a72c32c022e2d1cebdcbefa2fc0810ed6a0c7be253660f8ad5ea9c521ee826b1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100680837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b4080e2629487fd86346ead8e8e820c05cb893949b1970238bd1ea0e4cc8ae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 21:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:45:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 26 Jul 2021 21:46:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e844d0dd6bf6aa5959f603bad64a331fca5cda171d344450ca89c77e67410ac3`  
		Last Modified: Mon, 26 Jul 2021 22:11:07 GMT  
		Size: 7.8 MB (7769926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6e2a2dd7363ebee0e3b7e3d44204409298c305ea2a5f38345f68c7b769033b`  
		Last Modified: Mon, 26 Jul 2021 22:11:06 GMT  
		Size: 3.6 MB (3624037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaacada9b3485ee466ed24e835156869e37b446a2fe7a324d2f9349b81b4d0e`  
		Last Modified: Mon, 26 Jul 2021 22:11:30 GMT  
		Size: 60.7 MB (60718930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6c4ab38e644dab1eda7457e885b1ae711f77ce755b22faf62eaf6ee3b8bfa618
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89386529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18679636621171e25551613ca73c1aab9103b9bada4dde37d955edf925bc275b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:08 GMT
ADD file:1ec1791cf8b61620293d0fdf83d76f3c07482a327aefef699a43e82e7c3aa0f0 in / 
# Tue, 13 Jul 2021 23:21:08 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 01:51:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 01:52:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 14 Jul 2021 01:53:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5c5378967b4ed259bac71be5e1a9ea052469b5fe62bed34b19deb57d53dc63c0`  
		Last Modified: Tue, 13 Jul 2021 23:26:18 GMT  
		Size: 24.1 MB (24062066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed249db5e4f1496516d6a4c10ff289843df3f21648df9e24e36bc1b645798f03`  
		Last Modified: Wed, 14 Jul 2021 02:16:21 GMT  
		Size: 6.8 MB (6766542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5dddfbc3ef9239dd2d30749243dfe662b1fc9701fc338d7cedaac8f75b0cb14`  
		Last Modified: Wed, 14 Jul 2021 02:16:17 GMT  
		Size: 3.1 MB (3103714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55a3254dc87f78eeb0159639c9cb7741db9dbb95ba37b00888cbddcb6747dff`  
		Last Modified: Wed, 14 Jul 2021 02:17:14 GMT  
		Size: 55.5 MB (55454207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4fb5b498466e11f65f1ee2e0f67ca3baed607ee02de1d8b0870784936d03d115
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99171621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074a4ca1b28775ea75b942809acdc54cbfa60e1c4fae66e443f657520fad44b4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:29:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:29:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 26 Jul 2021 22:29:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0bcd6c59f771794bb0723fe6b8c1c0e51e9c469cdb93041dcdc9f49d27d7be`  
		Last Modified: Mon, 26 Jul 2021 22:40:18 GMT  
		Size: 7.6 MB (7634457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1740c38141581c96965e8f1d5d11782dd201bcd16881ecdfae0fa9b6054f6639`  
		Last Modified: Mon, 26 Jul 2021 22:40:18 GMT  
		Size: 3.6 MB (3600266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602da12c0e917e64e119e700446d9a9c975bd67127cdcdbf1fdbf3d45dd497c0`  
		Last Modified: Mon, 26 Jul 2021 22:40:41 GMT  
		Size: 60.8 MB (60766643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f0b6c0d6579d94bdbc9ba841282d10dc250d9a1a70a45d513846fe50ac0129a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115852694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b293ea7bd18861c35d3496970baf85c308e302b2bc01edace067091e27512f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 01:24:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 01:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 14 Jul 2021 01:39:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa601d6a2e5b36d987c4fdb079f47adcb54e845f31bdf1e5e9ee48ab4ba4990`  
		Last Modified: Wed, 14 Jul 2021 03:19:13 GMT  
		Size: 8.7 MB (8721735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60512369c33b9f7b7eafd481b6703a8a71a0fd9d9e71aea740ea72bdb8f45529`  
		Last Modified: Wed, 14 Jul 2021 03:19:03 GMT  
		Size: 4.5 MB (4456847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f4ae1d2fa9eb7db42d4fa3a85c284267bc4625ee96a1e6a79e95b1c11a180`  
		Last Modified: Wed, 14 Jul 2021 03:20:58 GMT  
		Size: 69.4 MB (69386266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ade07b1017e234a79006682f1cbf40d6ae638b39780946bdeffad7beca00b8ab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98139731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b44d16486cc0b2ccb507dd23a22997f6170cb6c554932e9c93a0a9a86220eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:12 GMT
ADD file:b8731edfdacfade2ec96757342f216962f3971b24077a9144da3f80003e6893e in / 
# Mon, 26 Jul 2021 20:55:14 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 21:40:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:40:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 26 Jul 2021 21:41:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:38800a0044dea146ca3c3a08bc2c9c956396ad3241a3c343010775650298c379`  
		Last Modified: Mon, 26 Jul 2021 20:57:03 GMT  
		Size: 27.1 MB (27149898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2888a21c9447e296644db94b75a0ebcedbffbfe4771d5361146fa064756319`  
		Last Modified: Mon, 26 Jul 2021 21:48:28 GMT  
		Size: 7.4 MB (7429218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fec118c5a61478d525b2e93c72b9c0d221eba35013d951988beb556e65179e`  
		Last Modified: Mon, 26 Jul 2021 21:48:27 GMT  
		Size: 3.5 MB (3542098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6898d82d2d06b5b154e6bced9a2d915abf888ec4fd73a49e81160dc913c607aa`  
		Last Modified: Mon, 26 Jul 2021 21:48:44 GMT  
		Size: 60.0 MB (60018517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

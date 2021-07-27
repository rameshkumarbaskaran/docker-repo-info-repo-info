## `buildpack-deps:groovy-scm`

```console
$ docker pull buildpack-deps@sha256:0b557fb09f027d2b072868d5b97c9ff5c4c227ac5e7a1d3037831b83ca5c24d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:groovy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7440ef2be4f936796d0c0522fe040f0173577145a3a514a471273f830dcc669d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95890911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2659a59a7c999902424b9360dbfdde2d86ba21ab2b274e003af76f18011c3975`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:47 GMT
ADD file:23ff7ae476ddf97e5dbaf417c06418ae4d8d49a88acb92738bf03fb4a22eeca3 in / 
# Mon, 26 Jul 2021 21:21:47 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 21:50:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:50:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 26 Jul 2021 21:51:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:32f3531c8415258308e8d8dda886004bc90cdf4793f9b97c6f33e7903036294f`  
		Last Modified: Mon, 26 Jul 2021 21:23:27 GMT  
		Size: 31.3 MB (31342970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f6d92cca49e420ae1a96a98a170c6c6f4d0cfafc25512a58edbb283cb30eec`  
		Last Modified: Mon, 26 Jul 2021 22:12:20 GMT  
		Size: 5.4 MB (5405030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975758a58780cd2adab51b5973557d092bcde9cdd6c9d23cd120f85919671daa`  
		Last Modified: Mon, 26 Jul 2021 22:12:19 GMT  
		Size: 3.7 MB (3664052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746170fb973f7fb3cefba229af451c7bd2ef9e1410913ef79ed93718b053ed8e`  
		Last Modified: Mon, 26 Jul 2021 22:12:41 GMT  
		Size: 55.5 MB (55478859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:53588ca044217fbcc9b48049c3ff18f3d51467bc4c19295d53c6f4f118e358e8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84596700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026643c2573fc5db9cad26b98bea47cc25f33f9b38526a7385a86b0bc75be7be`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:52:12 GMT
ADD file:4e6fd0ac6d6b29ca2b3da1f10b851ca590c1c1f49f75d7ee3f4bea0a19ddc2f0 in / 
# Mon, 26 Jul 2021 22:52:13 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:21:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:21:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 27 Jul 2021 01:22:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9e2181154536b422b7147b5cbb6a307b33f02a5fe3f3660fc72d7e6616878c1`  
		Last Modified: Mon, 26 Jul 2021 22:56:47 GMT  
		Size: 26.3 MB (26313208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a97ea937524f6b2a2a0a20d2c46e1d1b24e56cd1b6b64497c03e6798cfe7da`  
		Last Modified: Tue, 27 Jul 2021 01:45:01 GMT  
		Size: 4.8 MB (4840977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6d26ddce6ed928128c0c275d4bde5cd20f11d573bd8b921b0a6268958a2f3e`  
		Last Modified: Tue, 27 Jul 2021 01:44:58 GMT  
		Size: 3.1 MB (3140837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60216b15b0d7e7af60fba9fbec52ebc8ae9912ce5691cc8037c390effe76341f`  
		Last Modified: Tue, 27 Jul 2021 01:45:49 GMT  
		Size: 50.3 MB (50301678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d8be36aeca7881f07606650471b321d1c03ff2e2a6e00eceecf98ee200369d2c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94354227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d5ff08f29c67d43acd111485d1b17a5d43727569816a4443a40b56be91cd90`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:49:05 GMT
ADD file:3a4e8fe51fe7ca76be749ef0b92043e9e9b241a7b6f196fbe2a8bcde49c5b3e7 in / 
# Mon, 26 Jul 2021 21:49:05 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:30:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:30:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 26 Jul 2021 22:31:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:06dd9de3e7a96bf4bd49de5d681cb7062c5b3012c0f1b1bcd9d059380f55a1d2`  
		Last Modified: Mon, 26 Jul 2021 21:51:22 GMT  
		Size: 29.9 MB (29876744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647214296e105ce8a92eb9ba4b666f72064bb32c3394b392673e54540e1f06d3`  
		Last Modified: Mon, 26 Jul 2021 22:41:30 GMT  
		Size: 5.4 MB (5372238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ff548ea8c26b94143a36cf8245ff00840af96ba22465a184cf4390eb135cb0`  
		Last Modified: Mon, 26 Jul 2021 22:41:29 GMT  
		Size: 3.6 MB (3634615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba06c5b905e953629da8a61f68f094e7248c4f5be8b4bc879a509cfa3c27bb0`  
		Last Modified: Mon, 26 Jul 2021 22:41:52 GMT  
		Size: 55.5 MB (55470630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b5211fbc9fa20ada826f9d69ef96cc1506171252cd447dbc891905424ef3b768
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110868826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f16886f2c971f9a7ec071ebe5d937a7f8138a740953ae9d6c98b52999233a63`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 23:13:01 GMT
ADD file:b35738b25474b22211003d40615f8d2c6f97e8e3b32ecfb1afb9966d49a8cae3 in / 
# Mon, 26 Jul 2021 23:13:05 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 03:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 03:23:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 27 Jul 2021 03:25:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:95a1187a9d6fcc0e6b6e7651cbefe95105b207b9e90cc3662d593d0c2e9c76c7`  
		Last Modified: Mon, 26 Jul 2021 23:16:15 GMT  
		Size: 36.6 MB (36563589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e382cbe40e9a2e8caff21bf0c8b258410d9bcfd27650b9c3cac8184644d8ed5e`  
		Last Modified: Tue, 27 Jul 2021 04:25:20 GMT  
		Size: 6.0 MB (6040818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31efd420b8fe330c5231d3644569568f46a6d937b7eda3b933583d04157449e`  
		Last Modified: Tue, 27 Jul 2021 04:25:20 GMT  
		Size: 4.5 MB (4521776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfbc538a6415c257a8f5474b62e48b57307e8fc6a072cef4ad1e6bc6df52c13`  
		Last Modified: Tue, 27 Jul 2021 04:25:45 GMT  
		Size: 63.7 MB (63742643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6f4a5d5e16f76d8f66d13a7ecf54e59a7960e1e3e409927c5a8332ff77524ebd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85351256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71693fd376bbe1711bb45be917fd68798a2dda4631d224c6be2d2d05efa83eeb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 23:22:55 GMT
ADD file:b6af3eb17fceb12f32687c7392bcce88c50d169e89e08ce383b0d151f15e35b4 in / 
# Mon, 26 Jul 2021 23:22:57 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:04:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:04:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 27 Jul 2021 00:08:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2854584d46af51653126c966b1f675e9fc2d73b12251e85306724f0c3caeabb0`  
		Last Modified: Mon, 26 Jul 2021 23:42:20 GMT  
		Size: 26.5 MB (26524072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22b0f3794b3c283f9fbabd391721114f4de25a212c0905b7daf2ebc9b710aee`  
		Last Modified: Tue, 27 Jul 2021 01:01:13 GMT  
		Size: 4.9 MB (4922828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743fe037d460c34fe039d04c5bb4e64cc63b97f55de632b48bdbc5320d075dfb`  
		Last Modified: Tue, 27 Jul 2021 01:01:10 GMT  
		Size: 3.2 MB (3179172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8939850a31790ac98d18e8170f151d862abcd74592a8b0d488c2b6ea0b7d29`  
		Last Modified: Tue, 27 Jul 2021 01:03:21 GMT  
		Size: 50.7 MB (50725184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:53d6b22022c007f727fe7e889d59b77cf0877268f00b9a9ac5d1fc5276ba7cb0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102032047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9def7103978beb68fb5f62404cb14ee9ed68eb5f4fbac0dcce350a0716a787c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:22 GMT
ADD file:2f05dac9c72fd83b64830702accb3e1582661b82178055406f437be01591b038 in / 
# Mon, 26 Jul 2021 20:55:24 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 21:42:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:42:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 26 Jul 2021 21:42:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ebc30c62ba1234efc4428ed9d6d0f4f9b031ce916310c2d82b099cf9d02d1dc`  
		Last Modified: Mon, 26 Jul 2021 20:57:18 GMT  
		Size: 31.6 MB (31578338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe77f2c779c381b74f333923da8ee43a24119720802950c7670ba4d2f1b887a`  
		Last Modified: Mon, 26 Jul 2021 21:49:18 GMT  
		Size: 5.6 MB (5629737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac8e5f5f1362b078cf4da3e0b61a4088d2fba405fabc3eeca03b446a08e083f`  
		Last Modified: Mon, 26 Jul 2021 21:49:18 GMT  
		Size: 4.2 MB (4156776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02853a663b300cdcbfdbee7dbb15c142f5751d95622acbf369d1cf462a63385`  
		Last Modified: Mon, 26 Jul 2021 21:49:35 GMT  
		Size: 60.7 MB (60667196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:ea8180fa5a5cdee999ff997f51fff1a01ecbc2c27254f0524c7501701db02a6c
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:8cdf7462d535d8546191e2d8be96f54c2c1fef7d271c23dd65116dab61a2ec46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49582248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8719cb48c432f25efba53ab07db24fe0980538e66cf268a41302a381fe04dcea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:20:42 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e4f1f86f75f79726c33ce6adf1bcc342c3d24b829db05c0468cb30d24ed434`  
		Last Modified: Wed, 01 Nov 2023 00:25:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:5575a06c01d82f6a90eb863f38fb8d8ebf444d1d23e76bf00caa19e9df5beadd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47355873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5cd76e865d0e3d87d9d5cb2bd927d85c4b2dcc81b5d3bf4ee1281b561a8a44`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:48:23 GMT
ADD file:963e26decfc65419428098047df29dcbf7865e13bcdd67abeb9849f99a7815e7 in / 
# Wed, 01 Nov 2023 00:48:23 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:48:26 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:53c5547a993a8adb09a632a8ae34fbc336b27a456c6b3a670865cd8bedb5e6a9`  
		Last Modified: Wed, 01 Nov 2023 00:51:04 GMT  
		Size: 47.4 MB (47355649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b677ee8ca22ed8419fdc2c369aae8a679c91bdb1e447f4d2ea16360fc2f1f4c7`  
		Last Modified: Wed, 01 Nov 2023 00:51:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:57bfe1898b1d0732c6041e348ee5eeeb34a4f1794a1e59e9d3d6d14d84bccb27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45179635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d927d96e024bf9b4d2f647e423c29434bf1e0d26b1151872dee40abfbf62a9e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:42 GMT
ADD file:3b2b4eda35d794b39d6b5567e81651625af51da3deb3f63b3ffdffa07720646e in / 
# Wed, 01 Nov 2023 00:57:42 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:57:46 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9bf855396a6f46c1cbac4e188af10f2c38474f989707b0b1b406b48c4b7284ef`  
		Last Modified: Wed, 01 Nov 2023 01:01:41 GMT  
		Size: 45.2 MB (45179410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9c5e2a56ef37a800ea76a0ca6283847b1d4e01befee5cd778a426931189aaf`  
		Last Modified: Wed, 01 Nov 2023 01:02:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:00ae739a1642559fbe0530ed8a2ab3b1c458e2694ff2faa7b8f11ef3b7bc51a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49612878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe3c3eadc850aa8121501cddf47c8c80eac58c98cbdc96757f4830566e2f6ba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:39:36 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4510e3d657240178f5ab9fcc616dedbc122c627c3acdf892f5685cf37113ecf`  
		Last Modified: Wed, 01 Nov 2023 00:42:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:124345769299cdc61e5ea9b1800b5ebdc9c2e6ae9bf1e9e28430854f315cda2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50600275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50250d7c3539b57c8555420b449cd3cad0d9fdf4e32b0d653a7f2f6397a9606`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:38:46 GMT
ADD file:4043d711d8d7d1a995aed0a6998c96230765f55d4449167107955fe4af2a31db in / 
# Wed, 01 Nov 2023 00:38:47 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:38:49 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:be8d77e28ff21732ba73253b6226e47e4e07ec2cedc803ffd62148df5d7a165b`  
		Last Modified: Wed, 01 Nov 2023 00:43:00 GMT  
		Size: 50.6 MB (50600049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdb64ffecd408edb45b445a16391377972f9c9fc9ee766c5b1c18fe121d797d`  
		Last Modified: Wed, 01 Nov 2023 00:43:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a5e743d63af44e4e0e0efd63a60439c0f7fcfc9a2f557091968b41571cbcbb92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49569039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a944970038188e0619aa6f076e4691d79d1dca8cbb930ea18c7682caaf6b6ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 01:08:17 GMT
ADD file:b181441dc28bc6879e29cd086c569c653171c681525c124ffb6277bd71732bb1 in / 
# Wed, 01 Nov 2023 01:08:24 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:08:38 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0bfbf01892d22dd14fb9536e8675cc932ff41f415a415fbf8c6199106b01240d`  
		Last Modified: Wed, 01 Nov 2023 01:19:01 GMT  
		Size: 49.6 MB (49568811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8454879d434310ae4cc07da7fd814e1b3685cf437f6236df28b05d6829b53b`  
		Last Modified: Wed, 01 Nov 2023 01:19:20 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:dfb054387f0e32f2a8b6033e306e73d650fa7552ab2d99a6161349eabc5b17ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53575589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931b25b15cd3992de1758616e45cd164295338b0cef8ff09b1a26b9a23730e31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:25 GMT
ADD file:31b995b44eb1f532fd265be3fc0c3d3b55e28db0911c86a06c83de621418db94 in / 
# Wed, 01 Nov 2023 00:21:28 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:21:31 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:071872f8f8cb44e883168d06195f8fbb330e259b415d1ab108c27bda84d6c060`  
		Last Modified: Wed, 01 Nov 2023 00:25:41 GMT  
		Size: 53.6 MB (53575361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaec77aa346d51980a69b6d2d14f945e29403c9965dc58809a493707913f3b87`  
		Last Modified: Wed, 01 Nov 2023 00:25:57 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:2d9843c8138c2e81d70b5b9d2f86971bbb9a99f5425d957ce7ba1c89a4a954eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47943395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3000cbb523d51a9c51b98f26240ef05d0629cf2d201f9cd368ef994496abd702`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:42:15 GMT
ADD file:6d8ee60b2fe4604969d8feeeb7e0dc8b9619a778d1a905c8bfdde5ede5e1eb54 in / 
# Wed, 01 Nov 2023 00:42:19 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:42:26 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bca95e393f709ba301b35c2439a815fd4fe8134d7a466bd528563bc32fd754d8`  
		Last Modified: Wed, 01 Nov 2023 00:47:43 GMT  
		Size: 47.9 MB (47943171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b1bdf5e7431407495ef74927ceaac4251347b95ed8d76606127c69c9ceaa57`  
		Last Modified: Wed, 01 Nov 2023 00:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

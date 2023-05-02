## `debian:stable-backports`

```console
$ docker pull debian@sha256:e5b1392b07c1a075145c7317f7183cc04a1e3df201fe6e8d8d54a3d9c70988c1
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:a8b478d2ce0f702ddc1093b4d04bcd04f6a9f3be0e34ecf5c877631f5d0882f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55052960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b8c0e2f2c54bd4268bac939279c45e88e5cd1a6fca7e90d19df0e363c82bf9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:21:13 GMT
ADD file:369ac96d13405f257c2c05328a0e894fe34c37a4e674f6a51d3c82ac0842aa4f in / 
# Wed, 12 Apr 2023 00:21:13 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:21:16 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5942866a8d96513aac413957820a0f8951d44dbf27618c7c8d34b8b12221e7b1`  
		Last Modified: Wed, 12 Apr 2023 00:25:39 GMT  
		Size: 55.1 MB (55052738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948f98c248f7e4c2d3363b507dffaece6ab160937174f5019ee95ca4f78fd802`  
		Last Modified: Wed, 12 Apr 2023 00:25:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:341fd50108bd3aba0518d71cd1b6e70d9539727cfa48a6293a1741ab509eaa30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52546777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d1def12edd05ed53e354e5bb80dc1f617fd509263e921243835e4db6160988`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 22:49:13 GMT
ADD file:c83b51e96ccad1a3bcb3eb66359344f33591342477906e3c6126dc64c2c5e6cb in / 
# Tue, 02 May 2023 22:49:13 GMT
CMD ["bash"]
# Tue, 02 May 2023 22:49:15 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b8f5ba560106b14d65311aa93a26b6d47c0e2897dbd43f82d54c575c8a32e890`  
		Last Modified: Tue, 02 May 2023 22:52:18 GMT  
		Size: 52.5 MB (52546555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46886077603280e7e7b77f0c493193070666352d589c920196d44a7527ee6b2c`  
		Last Modified: Tue, 02 May 2023 22:52:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b8913013a649e8fcce53905decd52caa1e104967fce5ea6324d966d730af376c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50217077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc58fa78e370331ba61d1e9bf43a51a31c4ddd39b17046e633e9d91adaac116`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:52 GMT
ADD file:b4bb2f1b3108de77905d6352b1c6446fcdeef536f43aec2500c5d09d92132028 in / 
# Wed, 12 Apr 2023 00:00:53 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:00:55 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a7c2aaabb66eb576474b0b044c66c12b46741d43d77e19973d3e55d34b10c67a`  
		Last Modified: Wed, 12 Apr 2023 00:05:13 GMT  
		Size: 50.2 MB (50216854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57f82c11da0c26157ea79613d644ddeeaabe938e1bfe7af49b02924e07f8c6`  
		Last Modified: Wed, 12 Apr 2023 00:05:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:117d9a95193164781addd93e07b80757a11c5a47d6bd7a01da2ba378aa88d880
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53705753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64a0b35dfbc8dd7213d58084e6aeb18f7a3557163e9eb80f3d5c8e6287ebf75`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:33 GMT
ADD file:03803c0d18496d0ccb6b3368180d3ad1c425a24cbe434db6378022c82fe1eca6 in / 
# Wed, 12 Apr 2023 00:40:33 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:40:35 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:de1216f34da7c14b36760b3a58f5c8126ba9aaec8968121ead56dbe5e190c612`  
		Last Modified: Wed, 12 Apr 2023 00:44:23 GMT  
		Size: 53.7 MB (53705532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe25d6b4cc40c513fd4f1d0b928e5c62e5a85179aa98ce950577fafc360aabac`  
		Last Modified: Wed, 12 Apr 2023 00:44:32 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:28945dd054c5ab54493854ae48d6e0448ad3d7d42127656003323b8bb796a041
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56033018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7b0653c4fd8be1ce9a232435c6f2f0f2b263a39bfa9bd2a5a040fa744cdddd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:10 GMT
ADD file:7fbd8b9cfbfe636d889b3ab4bc2720e1f25d78f590b245f407f52de7c435bfed in / 
# Wed, 12 Apr 2023 00:40:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:40:13 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2be01e4197de5042d4ff9d71d4067b99b9860f94b8a4c3a2694c3267add868ae`  
		Last Modified: Wed, 12 Apr 2023 00:44:56 GMT  
		Size: 56.0 MB (56032798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a428d8dda767a782952b231a9d9b0be0dc970949dc251998826634a0704c1ae`  
		Last Modified: Wed, 12 Apr 2023 00:45:06 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:bd7f8f2026f5fb36a16d95b7a6140f46f5b1bc9abf71cda7161b0da4ff72a248
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53272259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81163808fcd93cdd496a696edd78399b69e0c9391958792dafff2166a040e93a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:11:26 GMT
ADD file:f97a8376973686baa0bc1882d725fd0017178340fa66fab6b56a5c55c85661e2 in / 
# Wed, 12 Apr 2023 00:11:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:11:40 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5554f032101bb415ee146e371c8c4e52f30d3407a547de63495133b10066fb48`  
		Last Modified: Wed, 12 Apr 2023 00:19:16 GMT  
		Size: 53.3 MB (53272033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9347bda0e43c709344b14c37967995b8fc8e12bd9d6c303a23aaf528beb3ad5`  
		Last Modified: Wed, 12 Apr 2023 00:19:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5b86aef5581f3d0dfd76c4de1f4e2afdb5e659fb55f563079dd313fc0d6b44a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58926780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9da829afe3fb40a3c68dc940af50992321f5dfd2b9cc2a40ffc089181882398`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:15 GMT
ADD file:ddb1417647bba31787e1f4f459cfefcdfb20b3fe875b92e1d794de61461baaaf in / 
# Wed, 12 Apr 2023 00:09:19 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:09:25 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dbd3b161013805c0fa5ce44a765b4d5e283b9478fec508653b4b0920631543e0`  
		Last Modified: Wed, 12 Apr 2023 00:14:20 GMT  
		Size: 58.9 MB (58926557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8850d6e5f5f15afbcaa695be9f33696172febf3b641f74ed3d6b344bae1eaa9`  
		Last Modified: Wed, 12 Apr 2023 00:14:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:28906673e3c556c941f22beec0fb48999fbc973af331ab89ded0c699de79c6f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53286862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ca89831cd75c91f61e181c73bfb1a3274844d01b88fb439dc949892dd6fb26`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:02:12 GMT
ADD file:d908f7342fbc7989444ac877c02229855ecdfb585dcfbaa86226e9e113a75619 in / 
# Wed, 12 Apr 2023 00:02:21 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:02:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:961df1f0f4d8c3e7504abcbd51340fff9c1714f466859ca0077ecbcd6367b5ff`  
		Last Modified: Wed, 12 Apr 2023 00:05:50 GMT  
		Size: 53.3 MB (53286637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c9e7a2d5db75aa25aff8e34e39b762190553c497a302af8a391c56c8ac8336`  
		Last Modified: Wed, 12 Apr 2023 00:05:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

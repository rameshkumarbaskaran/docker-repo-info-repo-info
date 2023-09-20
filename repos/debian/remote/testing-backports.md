## `debian:testing-backports`

```console
$ docker pull debian@sha256:8f9e03682bfe2b66c3ff805c9925189205af382865f0b20495168d3077ec2785
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:78249bcc0fc70bd23219f9fe646518b6ef82c46dc41c6188e363ec9e46b4d8be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49514990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b059eebcf4c1b841d444fe4853a312f5011e7bbf95db06eea49fd560cb0a729`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:23:06 GMT
ADD file:76da3f2b01205bf031c5a2baa5619f5692978dddb951a74e40bb95b7153a58b3 in / 
# Thu, 07 Sep 2023 00:23:07 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:23:11 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e20a7cf08f98f931d334586c1398ad4809e12fa399f21f419a18fabc331e71b0`  
		Last Modified: Thu, 07 Sep 2023 00:29:42 GMT  
		Size: 49.5 MB (49514768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171c807390c9713d23a025de193935c88a997a7f0e8603ea06e69637de2beb0d`  
		Last Modified: Thu, 07 Sep 2023 00:29:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4c79613517abe0b6753dd081a75b4f9c33c5df5a47eabd4f9c655c2084e2c1db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47170302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216ca37bd7e82b592f29b7ca783caf13482949a3c6cba6d439dbfb6942639a27`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:51:53 GMT
ADD file:c40dbacd84c044a6cc84e52a992d1b1d5966a49aac6d3218557c6a7f82315abf in / 
# Wed, 20 Sep 2023 00:51:53 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:51:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3b42eedb8ee5a76839537b23b1a4cd51deefe233d9b4985c65ff34c3ea12831c`  
		Last Modified: Wed, 20 Sep 2023 00:58:07 GMT  
		Size: 47.2 MB (47170080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fe964b42eb583bce325bce4226b39a5fb352570aa73cfbc7aa13562a733119`  
		Last Modified: Wed, 20 Sep 2023 00:58:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:329ca0c05c03a245f1ebac8695dd872af59b49f5f9b78921e13214f67ff8e9ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45010707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa6ffea3ddd747a56e6075db34cf614e74177784f134266b8fee23daf0d7d04`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 01:00:05 GMT
ADD file:897785df1f98741acdef541f7edc68c57cf0e3eb1698a87bd0537f8f0c654609 in / 
# Thu, 07 Sep 2023 01:00:06 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:00:09 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:de3c771b38223a129831a1a42a2e847e03db1ddec7563ae811b86bfd1c2f43b6`  
		Last Modified: Thu, 07 Sep 2023 01:06:20 GMT  
		Size: 45.0 MB (45010485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae7d463cc58a4fa1f7b931ede15a093d697e3f4032aece6f89327b06dae6b03`  
		Last Modified: Thu, 07 Sep 2023 01:06:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:181c8c60a8afbb88aa675d0bfdc76e801ebcd217522368a9cdbd66faf8a262bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49404752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d346454a93ad1829db9182aeef2bdb8b01c2f026f6d6c74226b179bda0710b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:45:43 GMT
ADD file:f0c1d15ee705796bc58abf92f15b7a16aa341028b6e099383437710d3694d315 in / 
# Wed, 20 Sep 2023 02:45:44 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:45:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c80309e0a5bbe8e3c8000103b383c6a60c58a6a84681e6aa5963d565eebe59a6`  
		Last Modified: Wed, 20 Sep 2023 02:51:00 GMT  
		Size: 49.4 MB (49404531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28a7bd6548127d0396a249571cc55f534c820732c903340e6fd755544ceeefe`  
		Last Modified: Wed, 20 Sep 2023 02:51:09 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:c83516da0c19744d493a6b4b7c32e7d0e3458f7d33dcdf1db05ac1ff616180d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50484976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45b2077d5fae3005d43b34884fe4b8c60c3ef9dec14199b1bf07d6979083eef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:44:16 GMT
ADD file:4d59c3dd2ca4ba5032a14346c8fdcef109b7734aca831c189868d19ef506e4ef in / 
# Wed, 20 Sep 2023 00:44:17 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:44:20 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0c50117d452a905428fa6728201904b2d7d1008e53c0be5357dc3e3d79904b93`  
		Last Modified: Wed, 20 Sep 2023 00:51:18 GMT  
		Size: 50.5 MB (50484753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc3a7e370a360c1fb11c519270fe48b8381680de65a6fa7b2adcf75857e12a6`  
		Last Modified: Wed, 20 Sep 2023 00:51:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:02d49666d52f688aeddca66dabbf97ca5e68564bb2047ca57954186558f59f63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49302558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e21e18e60a5b951fdacccde54d78d3fc74b21682757373406590be418ead42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 03:15:27 GMT
ADD file:c279daaece8cba4369dda08fde64059093b805e0480e5d49c2ebd6031a4c3996 in / 
# Wed, 20 Sep 2023 03:15:33 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 03:15:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:41b75db22e5e70a0b45e80eb89c31691d77bd206c097f08afdbc84713af36684`  
		Last Modified: Wed, 20 Sep 2023 03:26:49 GMT  
		Size: 49.3 MB (49302333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243ec506c33c33d3ec0d6a625a3fc186a782c08ddbbcf4eb36b5e71fd5e0a6dd`  
		Last Modified: Wed, 20 Sep 2023 03:27:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:e8f125538ff43b4de7b91d687865279e76824d9940b600af435f768abeae1963
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53456239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39562874b85d2a07c5ce80cbb507fd4a407c964594d73d6a0ecc9557f9d2ce6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:20:13 GMT
ADD file:69350b5a5e94c4a556e56f265533a04f8035ebc4bd834bec57b98a246ee547a6 in / 
# Thu, 07 Sep 2023 00:20:18 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:20:25 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7c3a2b005dd31b7bb84d8511ccf37b021f6db4066b3d2136dbdc778ea24e8eac`  
		Last Modified: Thu, 07 Sep 2023 00:27:03 GMT  
		Size: 53.5 MB (53456014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920e70ede045e655cd02d6cfdbb984e2f1c4895f84cb4329cf7f50885abbdc1c`  
		Last Modified: Thu, 07 Sep 2023 00:27:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:9fdc21b062b1f4a26127271939c927cbe60ff3b86b4e1e2b9f5ffbe2a8821b0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48761031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9137e794fe37e14ce2041be00ebd8a2e4c949bc1e3ed74f8828aab77f58eab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:56:53 GMT
ADD file:55adf3f3f6b9fa65711565f1c1946ce15e33e4fe2555b494fc36ac99ffa072ac in / 
# Wed, 20 Sep 2023 02:56:56 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:57:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9de78c172a0d9b73fefa46bf099a36fd6685a84a3d5085bc4bce9d9878f7f456`  
		Last Modified: Wed, 20 Sep 2023 03:01:52 GMT  
		Size: 48.8 MB (48760809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419f5fca906dfc6e89ee84715ca2ab73d0a95da223f490c156832b045efe966c`  
		Last Modified: Wed, 20 Sep 2023 03:01:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

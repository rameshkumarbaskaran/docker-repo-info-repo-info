## `debian:testing-backports`

```console
$ docker pull debian@sha256:9094e10487f16efad5e296f02eb08f5b16f21d473cc804c62d5603654473b2eb
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
$ docker pull debian@sha256:9598abf362ebdfecd26adbe730a32f328823732206c4bbf3edd12d0973180cc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49445557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3abdcf51afa282c392d6ea615670d7fc925fd82d588cbf8bbc456506fb96fa2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:41:08 GMT
ADD file:69f87b30025e86f5acfb8429da721cfe92ff7a1c139df827231caa96a982a89a in / 
# Thu, 07 Sep 2023 00:41:09 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:41:11 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cbef94b03c52659992feffae251a9a4af30679b4e560f2f8fa84e26f3ce8140c`  
		Last Modified: Thu, 07 Sep 2023 00:46:33 GMT  
		Size: 49.4 MB (49445334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ddb18ba5259f87d88d4eb7e820e1665531edab0d313856d69867c23ebbdda1`  
		Last Modified: Thu, 07 Sep 2023 00:46:42 GMT  
		Size: 223.0 B  
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
$ docker pull debian@sha256:d7f9d0c193b1243296933d77e46368c351f748ac9f25bdf6004837362feab1d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9446609c53bc9ac46867b5b2fc2d4ad8126a269f7d25c60226bf806f8f8aeaff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 01:14:39 GMT
ADD file:c6067d8729951df2c664bbd3ecc7487e82dae7e0d0b3868624030b3c5f73fb01 in / 
# Thu, 07 Sep 2023 01:14:45 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:14:57 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f2b2f343fec7d418a01e7f9a18923cec3fd789ce3a8f4f2e038ab44322805015`  
		Last Modified: Thu, 07 Sep 2023 01:25:59 GMT  
		Size: 49.4 MB (49357489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1616c4fbbe4d180cf5e90580dd36efd3cea4840e29e85e2b27da63f3beb488`  
		Last Modified: Thu, 07 Sep 2023 01:26:10 GMT  
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
$ docker pull debian@sha256:82cc9e895cc237b0451d7862badf4992d13a8415673f32fe4f76429972e86de5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48574006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d62c03925f6443a52db33356b94e48c4a0a70bf4c21a1d4ff2361345e2c825`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:46:52 GMT
ADD file:abcf51b81cd6f9cfc93b9963d223d2066f6e087d383af2edcf8f9a577dc23efd in / 
# Thu, 07 Sep 2023 00:46:56 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:47:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ee1a4ae1256a1fd777550db8f08b55a9e6e2b2d07e77c364c53343f9f594e95e`  
		Last Modified: Thu, 07 Sep 2023 00:51:44 GMT  
		Size: 48.6 MB (48573786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f758147df3f60775dd12108aace8c6bc463e7b3ca350fd7f3d413dd3041203e3`  
		Last Modified: Thu, 07 Sep 2023 00:51:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

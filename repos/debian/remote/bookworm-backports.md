## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:cbc8abb26537cca745024c10ac85e0bcb00e70fcb05f6c2308f1ae97037bc9ac
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
$ docker pull debian@sha256:480aa48e405021523db6cef1756c65127d004bf70cc973bc13be30253eaa7cc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52944624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1d7e3175ecd8da60fec8a2f9deeb250e8677aaafd4f5b7d0dc16a6a315c941`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:19:44 GMT
ADD file:daaac4875b34dee73ff062c17a4763b2cf5726753df4e9700bbcefa0f88153e6 in / 
# Wed, 11 May 2022 01:19:45 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:19:47 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d68396ae84f0ca729923a79943893f43492725d77e7b329170777a2bdbb6752b`  
		Last Modified: Wed, 11 May 2022 01:24:08 GMT  
		Size: 52.9 MB (52944400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4aace0849c4b5772ca1b127ee42e7ce2b815d1883e45091c0c29ce801704e8`  
		Last Modified: Wed, 11 May 2022 01:24:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:a8501c9515935127315dd8c83a61d3b162f88c0150aceeead01d3fff6b6c87ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50737662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ac339cb6aaa786b3a5446a53bc3576375780a2988e5e783b9e73f84dd6890a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:02 GMT
ADD file:14b16b308b28ed8604a9f98d47e92522f709988224084eb5d2dfd30d3511e4a4 in / 
# Wed, 11 May 2022 00:49:03 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:49:15 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0baf2800ae4e68af843862199b558f14eac2766cea5651c0837cbd8ee827981f`  
		Last Modified: Wed, 11 May 2022 01:03:42 GMT  
		Size: 50.7 MB (50737437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd980aa5c298f4abd497f7d74bcbfaaa37a9105bd53353acd861dfeeac5218e`  
		Last Modified: Wed, 11 May 2022 01:03:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ed3773dcab35f75def51b4576ab98e94eede5bb60e5fba2f28f644a7b02d2efb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48476570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbdc62a252d0a15231db45518e06bf6670060c2572d762774858e5c9b571f93`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:58:07 GMT
ADD file:8f129729b10afccc69a16674ae2d85afe02706c13f7c3177672040ce01dc34a2 in / 
# Sat, 28 May 2022 00:58:08 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:58:20 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:138713cd49f1253cc6e27f92b0403100f0c5966f7a66077fd4d7c6ab6a6799df`  
		Last Modified: Sat, 28 May 2022 01:13:41 GMT  
		Size: 48.5 MB (48476343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b27bb8d76642db6eee076d0b50eac530fc4a82d291098143d722288ed3230f9`  
		Last Modified: Sat, 28 May 2022 01:13:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:bc37f527b1a8187030b964efba2d2c9cd4889c4ee167edd3627077c38114b0eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (52043016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92423f50980bc3b2085dbb80d2650cebc0605b29e79086c49e000a4c87515a03`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:39:58 GMT
ADD file:ae47b859bfb40c803f02c28e3f96af8bc788772728d65e218948bb1eaad3bde9 in / 
# Sat, 28 May 2022 00:39:59 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:40:06 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f24ab7edee1353b240b401789e816aa26f6557c18b9a3ac7edd79407f8347c7a`  
		Last Modified: Sat, 28 May 2022 00:46:24 GMT  
		Size: 52.0 MB (52042792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ea835d1ed37a70b0e9cdf993aeddf3430a7b1cf8f0589bed0aa41c02f8352d`  
		Last Modified: Sat, 28 May 2022 00:46:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:e109920ba50acfdc9b750abaf21516b3cf1b45e9d0b761a54e5c5ea9ca2176e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53948711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d941dd4e1724ff2eaed769c59069b1d6d2646ab96455465b87c30f44935ac2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:38:49 GMT
ADD file:ba6ab6618a6fab6f0a1d80573b329e26b602c060d940b76c1774ddab96982cd9 in / 
# Sat, 28 May 2022 00:38:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:38:57 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d1098d76e3f40923a061abc8c2e6697409b0a2428eab6f37ae394a7b491b1cad`  
		Last Modified: Sat, 28 May 2022 00:45:27 GMT  
		Size: 53.9 MB (53948486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce13680f03715c9981c64d8eb2ea4c1c43c31f39767230d2e896c39754a341ad`  
		Last Modified: Sat, 28 May 2022 00:45:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7228f0792c34a92098cd9bb4941b2e2a7f9d80ee761c77dfabcb9ec915d11439
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52067153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94fefdd36cb9d01a7c65e784de2ed6091d3068d91082353258a5d7c93576419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:21:42 GMT
ADD file:023ba5f785e781bda7875c3b4c2f163666fe7b1a6a0fde74103b7799380a55c3 in / 
# Wed, 11 May 2022 02:21:47 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:22:04 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1315838dc3fae911b53ad8b9fdb88cdc4a2988e4a4924922837b71b52b18d1fa`  
		Last Modified: Wed, 11 May 2022 02:31:44 GMT  
		Size: 52.1 MB (52066926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331a3fd2008c235f27643acab53e658bc853c66379aa40daf350af5b007de45e`  
		Last Modified: Wed, 11 May 2022 02:31:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:90cd0206a700ff29019715348fe34353bba280cb3a2ba8a783bcd743f189c1f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57150668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45203d37759f674b0535fd654e695f019b61893d540496238a282a154a94310c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:30:46 GMT
ADD file:151ed5fad83d0b4f27c9bb34e41c649df7b7b9cbe789e3036c44d12cf1f53a71 in / 
# Wed, 11 May 2022 01:30:51 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:31:06 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:49991d23fb52aaf7937c711b0196364a5011e41402f3ea986702027fadd27e0e`  
		Last Modified: Wed, 11 May 2022 01:41:30 GMT  
		Size: 57.2 MB (57150441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c7c04802d3e0303cdf2e095017f859003c5895804d9ca1ed1d5164bdfbe65`  
		Last Modified: Wed, 11 May 2022 01:41:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:99c08719553df4dc5d7f97df9d772109a2b62a6a0b08fe9b0a1c70ccfca50b52
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51490612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5102dc357f1825025a807485a8611005172c47fca0f8427609990f05b6cde6c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:57 GMT
ADD file:4a6691f8332d56b3f631afa5579acf89d2271614f4a4f77baa24e59c0b2b3016 in / 
# Sat, 28 May 2022 00:42:02 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:42:11 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5c219aa5bd4928fd8e410d747805f6d8a6cede332d701af0c9e39dca3b50c70d`  
		Last Modified: Sat, 28 May 2022 00:48:58 GMT  
		Size: 51.5 MB (51490385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed6e1a8940d378998d7ed515a829e391754cd12cb9397ae431d5d8672700d1`  
		Last Modified: Sat, 28 May 2022 00:49:05 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

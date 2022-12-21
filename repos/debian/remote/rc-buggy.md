## `debian:rc-buggy`

```console
$ docker pull debian@sha256:ee6244e67a5f99458c6905ac6b31925f5957da63ac47a82a923a3c0655840bc4
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:eea1404b0e494a60be6dc0b8f35ec1485eb8d2f1e419970cb1c789c71dcf3964
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50286370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47fa0817710237df5602440f1b28e8999c56be5b1147a273314c9424a7187e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:21:21 GMT
ADD file:e1060039de636fe2bfa207b8a071caa2d6ead322d1c2621e322409706dd97730 in / 
# Wed, 21 Dec 2022 01:21:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:22:33 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:fd14438c7d22fef775ab49a94c6b4c250839f557fcdd15c31806e0fd16591085`  
		Last Modified: Wed, 21 Dec 2022 01:26:09 GMT  
		Size: 50.3 MB (50286143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e8d59a622004e2a22be0e84eb1efdb86a62efb7ca5cb7f5655f7052728badd`  
		Last Modified: Wed, 21 Dec 2022 01:28:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:442172833c3d8926e512912c73e5724ca7440bcff00aab7b6b8e2d766615a8a6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49271009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dd3b62a50889b5485f303f11343708b4a67fdf20e406b72161eb8a450e53d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:19 GMT
ADD file:7e649d148f5ac98acdfce2b45b373b5b22a9792e3d365d3f1dcb2414a59f4149 in / 
# Wed, 21 Dec 2022 01:49:20 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:50:49 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3175fea42c68213e6e72826c3ee7daa4a58070ce07ae526e91c30a8743d89be1`  
		Last Modified: Wed, 21 Dec 2022 01:54:28 GMT  
		Size: 49.3 MB (49270781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bf7831826c80bcfb5ba9e80534c5af30098ca87d6c0202c9d0cc31e565f0de`  
		Last Modified: Wed, 21 Dec 2022 01:57:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:6bc5e7520e74f56604002695658b50a58c6ddb39933aa8135735f10aa9d89bf1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47080909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ae1bd5eca538805d8db82bc7c53038c23a6dd2ecd3a18c900c136a0aaef44a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:59:31 GMT
ADD file:9f6e7ad60906ff390d6369133d129df5057cc1505edafd2cccc2eefa5265ddaf in / 
# Wed, 21 Dec 2022 01:59:32 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:01:13 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4d12d04403dcef32bd0b6201954d02c0de421dabf04dd54d568898f376cb96c5`  
		Last Modified: Wed, 21 Dec 2022 02:07:07 GMT  
		Size: 47.1 MB (47080683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ebe23422c442112a0a3f871266258bf49a89cfd421c44bcb612b5ff476051a`  
		Last Modified: Wed, 21 Dec 2022 02:09:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5080664ee42f0b7c906df79642e685ed0c7cb5dd250c1144d21ebda2b2e65c7e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50336205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710a3468eaee205081c7e769983f207661935ed5733061a28f6e124180910b3e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:22 GMT
ADD file:afdb0d23dc73b5f1a887a2dfc3fb8fc2ebf210e9ac6b5d6748cd89c77d9e436c in / 
# Wed, 21 Dec 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:41:13 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:951a6c4c03238810abf592f0f3beb641ea6b4153bfa55acf62944018b9ed669b`  
		Last Modified: Wed, 21 Dec 2022 01:44:40 GMT  
		Size: 50.3 MB (50335976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e32f17c15ae579b0442856fcc37100fd3fc78707de73a3ac69bc957e707a7bf`  
		Last Modified: Wed, 21 Dec 2022 01:46:39 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:b7e16cd8e5be9e6cc3e47adb7a7163f3c059e3d108e61cc43714a2977b931592
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51340353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df8e2f10a407806de4ead3331e27288cddaf8831030fb13c6e377bc5ef3ee0d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:20 GMT
ADD file:d73a77dc412cd093f533d8c6403c7a4a629d7a7d31b1ffc8555e0f7876d98ec3 in / 
# Wed, 21 Dec 2022 01:40:21 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:41:45 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e5477ffb90e4da3fe8a2c9a63f402783b74fb55b190b59240e4d1d7e5b55a2da`  
		Last Modified: Wed, 21 Dec 2022 01:46:35 GMT  
		Size: 51.3 MB (51340127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4893750c160ac4d4a8262136ce99c0ed239823e01386d14a9fdb5f9627bcbfe4`  
		Last Modified: Wed, 21 Dec 2022 01:48:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:4784b4da74e5ecd7649c797bcd5566fc636793e2863c92cd68c8459bd1099858
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50293174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f39fd58d2a9059103f0965bf008d54f6129deae35b424bc4f1e9bc33d0026f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:11:07 GMT
ADD file:bc4f0f717f54bc1982dd6d104f684f180c7b8da660351e5be4853a56b38e374f in / 
# Wed, 21 Dec 2022 01:11:13 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:15:28 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:22a773956e0933f1a01038ae977c7c99f46cd5ce02f672c66be9a1c837de4eac`  
		Last Modified: Wed, 21 Dec 2022 01:19:25 GMT  
		Size: 50.3 MB (50292945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbac5846049f646e00726b2427a9325410332fa41ecad99b2ef194b4565aa11`  
		Last Modified: Wed, 21 Dec 2022 01:23:57 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:bdebc967c838bdeb57625c533682f1c4b07277a81911761b391378876b6d0b58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54333215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798b316c2494544076a927932f48584f1da97a100633e960dda0196e47496a3b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:58 GMT
ADD file:4af1feaa33ee2a3c1112b5ed0efbcccec637c4dc23a5af7d55343f6ab7005920 in / 
# Wed, 21 Dec 2022 01:18:01 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:20:14 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:47dc200f753ddc67a9fec80382c7c2b6f164cb907748c309862373fa8d94c504`  
		Last Modified: Wed, 21 Dec 2022 01:23:50 GMT  
		Size: 54.3 MB (54332986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56334aaa76047ddce75ea1b17b7bc1c38062b9c34153037287836794ea5eb5d5`  
		Last Modified: Wed, 21 Dec 2022 01:26:52 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:e6b5be2f5ecdd1b74aaa0a961bac31d596996a3cc1a0df8c847f8afe971a368d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48679738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c3cd5dfac33f09c58f875e7693d6058d8c9075524fd8446374583384af6221`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:28 GMT
ADD file:880ff0ee3680abb7b9e72fb9457e71f7e35b2ef7a1d47d57ca68904588756f83 in / 
# Wed, 21 Dec 2022 01:43:32 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:46:37 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9c9fbadd05736c9fdf511ecc5d2eec08182e6f9bb03d6f8f6e50bedf7a713181`  
		Last Modified: Wed, 21 Dec 2022 01:49:29 GMT  
		Size: 48.7 MB (48679509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dec76cc80613e91a15f5aabdba19f9529d280984e6e2740e83a256b9816e61c`  
		Last Modified: Wed, 21 Dec 2022 01:51:17 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

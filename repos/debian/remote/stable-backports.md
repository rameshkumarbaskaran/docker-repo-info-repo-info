## `debian:stable-backports`

```console
$ docker pull debian@sha256:79963e7cfa0e9b7c1be7339bf0a86d43a3b3a39b38b1c361ceaa17c705c7e98e
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
$ docker pull debian@sha256:13974285c0f6a42af48168dee4a740d522188a5d65aa7ec62b4c1f98a7d220cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55010098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507e89bdfe9c356ffc228ab3bcb4db70112f74ba00e0bdb431a884892a3ed792`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:21:51 GMT
ADD file:737a506e7ebc691df8a80d35c1cbb41c08ae5a5d845821fc5c8c20be3ebeca2e in / 
# Thu, 23 Jun 2022 00:21:51 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:21:54 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2e28d2612399606ad88011a02d3461010a45bb18ee475e4046f6d089d07573c3`  
		Last Modified: Thu, 23 Jun 2022 00:29:00 GMT  
		Size: 55.0 MB (55009876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6b2e249775b778ea4f5e30e5ee397d270e085c544977ee70a39b74fef92df1`  
		Last Modified: Thu, 23 Jun 2022 00:29:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:54549d00a7c21427e013ef210273fae7231ffefcc1c29a3940c49d37dd84d639
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52537083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864c3e7108acc44b7b618554d0a31c9465b218084b4411081b53ebcd5ef5b45`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:53:53 GMT
ADD file:02fd910cc563733b6b724cdb91c80a999c47ae6c9a1dbe9bb39a630159d4550c in / 
# Tue, 12 Jul 2022 00:53:54 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:54:07 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6853bb519f7a85c62eddef077f0ee097f64fe120a93583c92fddde2dc0706c7b`  
		Last Modified: Tue, 12 Jul 2022 01:07:53 GMT  
		Size: 52.5 MB (52536861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207a54dcbf5517accfb1e471b35a23ea89f64784b43caf8365d2e72c622d8ef1`  
		Last Modified: Tue, 12 Jul 2022 01:08:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ee9eed71815355d1bd6b527c080e145d217ef1d0acbd1c159861164c9550854e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50199875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28facfbe9b2e1045e1aff31fde358eb6c077c0cf9d843f71597ea1f88da7dd6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:04:05 GMT
ADD file:f123279acccd47efead5f0e2af10c98690ab4677289ea23c6503019e028338d2 in / 
# Thu, 23 Jun 2022 01:04:06 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:04:19 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:92a65b5bd5ca6a296176b083d8e798fdc70a048f0e8d2a1f44a53ebe4175c840`  
		Last Modified: Thu, 23 Jun 2022 01:20:54 GMT  
		Size: 50.2 MB (50199653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b7c11306e66ede8c35f8a3879cc20896a52ae9b9eda54f32f2d4ab8fe128ba`  
		Last Modified: Thu, 23 Jun 2022 01:21:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4231f2ea6ce40364ca7d8d1f533a32cbd6c6e7f50e4ed665079ca52419ff038e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53683372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3ca347b365d84f677dac8188a5593beca4d71e73002680a95294c9bae12b8d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:42:00 GMT
ADD file:0d6d31f56f31acdde787a277c21886ee3b25087b509730a2f2ad46110f0e4373 in / 
# Tue, 12 Jul 2022 00:42:01 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:42:07 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:daa333d9b33fef63ba6f1f9dd9160e035cd096dcc8d747c77233c000262d3467`  
		Last Modified: Tue, 12 Jul 2022 00:48:50 GMT  
		Size: 53.7 MB (53683149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57180f860626256ba8267ebf3ff8dac4cd94890975e8851566b29832fbd6cb48`  
		Last Modified: Tue, 12 Jul 2022 00:49:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:26a0da71a2ba3591115c9878f5a5edb3baf102fe91670e35ccce524a73cf43d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56002005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e5f2e3c4271fc5c379b4bae9c58638df13547177bc534439692321fc9ce1c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:53 GMT
ADD file:c7bc307cd23459ccce030ca00fc0944a4a9088bc73c3a1694c92e163dc5f938c in / 
# Tue, 12 Jul 2022 00:40:54 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:40:59 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8d1153e4af373ce56f9df7ac71b093b2594b621cb8b6fb27893261bfaa17d958`  
		Last Modified: Tue, 12 Jul 2022 00:47:56 GMT  
		Size: 56.0 MB (56001783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae97a6fee82a6e2e729687e0e0f461c928e8c39d321fd00ba2f21fa46c29c60`  
		Last Modified: Tue, 12 Jul 2022 00:48:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:0a8c24b8b378290d885217831b88b0e1543172a978fda1a4848588e875b06d6d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53273436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ee8a2d6e0c54ee0bcb8cd5049a45fbcf4f46bf103223afece48e0283c3c195`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:13:59 GMT
ADD file:6d73f22d291c834ed6cc56ec0eb8b296b7773b12982c32ebad637e87819528f2 in / 
# Thu, 23 Jun 2022 01:14:04 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:14:14 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0f8e27fff545afc69cd7fe996bfab3548a912da581edd876257b0f5be1939ca2`  
		Last Modified: Thu, 23 Jun 2022 01:24:53 GMT  
		Size: 53.3 MB (53273212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06047e3a3e1b1d3f28c295cc1d26e48dd320cb688ab4a1b66f864fae15e92099`  
		Last Modified: Thu, 23 Jun 2022 01:25:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:caa85184a93587ec62e8c83c158e5c92cb6e2cff46e2ad98c724f37c1e49b6a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58903368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1929150dfd2ba9e14363b75c59ad7c542d25983ba62c6a93ac129f10a0ddb9ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:05:32 GMT
ADD file:7da112f12df3a5ac91ce410a497119875ffbfc4cba1015584413f35a24be3f42 in / 
# Thu, 23 Jun 2022 02:05:37 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:05:51 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ad70abc1c24d1e039387b56271f6b5c28b1e69c47aaa99d207005c1732a8a5b1`  
		Last Modified: Thu, 23 Jun 2022 02:23:43 GMT  
		Size: 58.9 MB (58903145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4561ab3c6216c5a40cfebfcba442888c867c864b498394eeae868628a71bf8`  
		Last Modified: Thu, 23 Jun 2022 02:23:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:3b47334ed0d23c8e5eac5df84243d6a14aa97d43eabb34357ff97c3752cde27b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53269193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680a90575ab8e9d2acd12c9aed6e92c87c10e33acec6e42c610b82be5f92276a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:47:01 GMT
ADD file:ed009ff381c2a0d8393de98bf900ae04ba3fe2b17138f95be310ba8609739e7d in / 
# Tue, 12 Jul 2022 00:47:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:47:19 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:26177b6f29e3cc38c0e209539f17f4264317f877f4487bec96a274fdaf6d4c6d`  
		Last Modified: Tue, 12 Jul 2022 00:55:37 GMT  
		Size: 53.3 MB (53268968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f323d90a31f790b3f8a885fbcce068592a7409626f395d4dc2ffddb16dc50b71`  
		Last Modified: Tue, 12 Jul 2022 00:55:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `debian:stable-backports`

```console
$ docker pull debian@sha256:b30b111fcc2e64a2f4f98433ded542cf726f3b4440fd0798de17b0a6e6d41ca5
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
$ docker pull debian@sha256:39c267946be7ea904aad0bd7991ec521456a7113681b1c666b34c7932ef51606
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52541355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b3fcf1a03a6b40e2fbd1afc59f071d1d341df992e6b45aabf1ea324aae2f59`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:54:41 GMT
ADD file:30be18a2a0a287723b8e48a75c0582b899f1c3df76c8d5cb7ef570fa268d6ace in / 
# Thu, 23 Jun 2022 00:54:42 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:54:55 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cd8ecb2c12f965efdd0de713f1390f9ef2626c397f479f546f503a6a2e49cf5b`  
		Last Modified: Thu, 23 Jun 2022 01:11:37 GMT  
		Size: 52.5 MB (52541132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bd675c1b27bdd43c763623f2c498c8f09b21c657543c84ff0d4afac256c4d4`  
		Last Modified: Thu, 23 Jun 2022 01:11:48 GMT  
		Size: 223.0 B  
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
$ docker pull debian@sha256:8dc32c8a1f53251dc82c30425ff09b26ff0b506d860b16e04c2ab9bf052c0d08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53697057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e75edc44560ebd82f39213f43525dcd6fbc23d4faa1387591eb4670577258c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:21 GMT
ADD file:ddcae2c18fa8dd35f2057125dacd9932420163d1d4597d8a33a9f29d13f275de in / 
# Thu, 23 Jun 2022 00:42:22 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:42:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a13be41bd2ad9b92c78cedeb166a2205e88427c96a52433fce09b95e29b46d82`  
		Last Modified: Thu, 23 Jun 2022 00:50:37 GMT  
		Size: 53.7 MB (53696835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0e91ad6ab8b4623cb4f72efe4cd4c950c2ae71888cf79e1b6a35c3771954f0`  
		Last Modified: Thu, 23 Jun 2022 00:50:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:375112b66186b011486a8b7a0a704c745eb4ed9dfe6badee6ec0bbcd7b716f22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56007771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6de90e454643c3f4b16b3a9ae2851dafb834ec5d860f301682262e57644d72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:19 GMT
ADD file:ff4b29ac632aa6328e16072dfa0f3e7b66c56d1cecb34bfb18a1d1b95a2d691f in / 
# Thu, 23 Jun 2022 00:41:20 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:41:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8058a8829a35e9a90cb4a6c94fcceaffeaf71b45fbdbb6cdc36cca7b6de6ab40`  
		Last Modified: Thu, 23 Jun 2022 00:50:07 GMT  
		Size: 56.0 MB (56007548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c6ed653ebfcbef2541c92ddedbaac629a3b68a5bcc92f7b1115a595f62ef18`  
		Last Modified: Thu, 23 Jun 2022 00:50:19 GMT  
		Size: 223.0 B  
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
$ docker pull debian@sha256:081ead2774ed562ab52227456b4f0eb41f27faeadef8cfbdc7720a7ecc7929d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53277026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2fd11b1a191a86b2235d221df773b228774b217940d42ac0116d1e1f9b8e97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:46:00 GMT
ADD file:73c0b4e8a93d320e7beacb602bbd3be64261189e16d3534d40ec519b2acfbff8 in / 
# Thu, 23 Jun 2022 00:46:08 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:46:17 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c20cf944d8c43a3b78c63ae1b46b6e5070946c86ef7ef98faee10dcde4b83bc5`  
		Last Modified: Thu, 23 Jun 2022 00:53:44 GMT  
		Size: 53.3 MB (53276802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e990b7d84256d6222cd0e345c5dc76b27475416a081d5c12ab020c57d37c7d7d`  
		Last Modified: Thu, 23 Jun 2022 00:53:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

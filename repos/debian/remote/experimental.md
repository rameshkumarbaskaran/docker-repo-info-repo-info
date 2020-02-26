## `debian:experimental`

```console
$ docker pull debian@sha256:751989e2f7b5e1e84b86e8cd54e8268a1571f42c8bc58992f13cf31d43e0215f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:9bd70a01d7b07dfba776a7a01040c34eb5aa9879ac9009469b438b80728ec1f9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51549734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b51ed2ca4eff2ed600876432b65d649bb648b4f27a3ea6043e87e1d2cdb8f5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:24:40 GMT
ADD file:e2d4b6bace45e956ca8dce3677b4f87a51946f0e552bf8ccf19a3384d51d6786 in / 
# Sat, 01 Feb 2020 17:24:41 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:24:56 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e735cca5c96d58ef793c1c6314f8801066575e83c31c0945992592ea9b747912`  
		Last Modified: Sat, 01 Feb 2020 17:29:43 GMT  
		Size: 51.5 MB (51549510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840a7850088c6bf226f573b68285e8547c46a12e7d9773f10ac4d945943589c3`  
		Last Modified: Sat, 01 Feb 2020 17:29:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:cfa63ba7b2e2a343802926ce51328399f75bfa5867bd3b52ea0dd9d167e808fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49540938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1eb50495280e5cc25b6959ea073158d8db96041b7f133ab20c285ddb4888fa3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:54:50 GMT
ADD file:14d67ea17449c1020dbfca6f974bb32dfea6e28b7e01306a00d56e422cec75ac in / 
# Sat, 01 Feb 2020 16:54:51 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 16:55:10 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:aa3eb8486813709172d1cf6bf2f115717f25e61221155de8bcb887b8660d83b9`  
		Last Modified: Sat, 01 Feb 2020 17:02:10 GMT  
		Size: 49.5 MB (49540714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4667d27fcbbe5a40772af8c471b8fdd7e1bf484b9f47508e999de4730480a67d`  
		Last Modified: Sat, 01 Feb 2020 17:02:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:26bea54fb8fe149f3ff96a0b7b658f8c70d8d2199c787136770f2913c7bc10e7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47282388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b264793eb8676f7abbcb49c1bcb9c4887b0dafafbef0e65cda09b2badcaf104`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:05:32 GMT
ADD file:39d4831ca03a283e47e93615193aa1f15d66e1aec783ac1321987b9983cc4b1e in / 
# Sat, 01 Feb 2020 17:05:34 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:05:56 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:515183962bc5d1b23c6e06a5ea58a16b210603a0ae878107f1d366e715c8d7b7`  
		Last Modified: Sat, 01 Feb 2020 17:12:33 GMT  
		Size: 47.3 MB (47282168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d42f4291e3812ace199a3ee83120b65f0808d94b9e96b4232cdc7841220f26`  
		Last Modified: Sat, 01 Feb 2020 17:12:51 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3e9d049fc645606002c5e06abdb39307bc2d4e399fe31f81c734da9d3362a9e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50506195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95a8ac25c85948bfefa356235832a5a4c1b00b91d2645ae844a348facce1f9c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:44:10 GMT
ADD file:def160abf00f8ffdbbb6bed46494e2d0c63fb03d306cc343cc8a22163f3b78de in / 
# Sat, 01 Feb 2020 16:44:12 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 16:44:32 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:499607ed9c41b8045fbf7528cc9fd47849c6d7483f62ac5293687184ed19b43f`  
		Last Modified: Sat, 01 Feb 2020 16:50:09 GMT  
		Size: 50.5 MB (50505972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2633103f8a1c04f272d637e3bdea406d1ebbbf8cde1cea7932e5c8fd84f8f74`  
		Last Modified: Sat, 01 Feb 2020 16:50:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:40de0ac07cc3c36ff85df99ded8ea17377d3c9c96057fd195bcbadbf89e7005a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52999796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b44f9dd5bec05227df03b643054918a10ec74d874c5e343714f8f45805630d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:36:34 GMT
ADD file:5955a629c35b1206468485798e83690e152f5d8339418318b4bc5f98767d2df5 in / 
# Wed, 26 Feb 2020 00:36:34 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:36:53 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5367f3e8a07cb0a9f87933b63de70f98eaa2c832490cf96072fa70efc87341fa`  
		Last Modified: Wed, 26 Feb 2020 00:42:59 GMT  
		Size: 53.0 MB (52999575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7ecec61c6a38b9086cfd38dbbb7deb338135040dd4aaa6e93e1eb9d859121f`  
		Last Modified: Wed, 26 Feb 2020 00:43:18 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:715459e1eea95850b6dc00b5df7760204faf73b74d14da7b7ba794ee3ecbfac0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55349213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68af0f76c2e341b063ea68c39a9f6057e236e961da1e20221800d2f0c8e52ef2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:21:55 GMT
ADD file:06c0b626f5093d61cad3fc631312b7ba0980f5e6fcf8cbea751f9bb4b12adbb6 in / 
# Sat, 01 Feb 2020 17:22:00 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:22:27 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:eec7feff016f03cc0927eb65bba8029fea64e56e6b613b37e9c588cad1310aac`  
		Last Modified: Sat, 01 Feb 2020 17:32:51 GMT  
		Size: 55.3 MB (55348989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec9d6469c5d03d7deb183031d121aad79fec7972369db546689a305da38b965`  
		Last Modified: Sat, 01 Feb 2020 17:33:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:0d2fa3b34f4f4d8716e791af0324fd885024223a2c0e4b22aff276170ff8bbf0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50192462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b413035648af6bd3b0a3450b6a3a25d1e9df21a94d5e77287c2f403eca85d9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:44:26 GMT
ADD file:7d2aef129d19eb475274f63ebe95dcabb3764acfa95d826c2ee2f7d47c566b94 in / 
# Sat, 01 Feb 2020 16:44:28 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 16:44:41 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c566c73810a383de9fc705132d7dfd3fa934e21f11ee9f04754d1ddce23c708b`  
		Last Modified: Sat, 01 Feb 2020 16:48:18 GMT  
		Size: 50.2 MB (50192241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d618528b130ea2b14c34bf1fcd657480c9506176411d3d5567a2a00c5a7b3`  
		Last Modified: Sat, 01 Feb 2020 16:48:31 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `debian:experimental`

```console
$ docker pull debian@sha256:e560997e97ac6ff19e5934fdc10dce01caa54ba21f9b6047933c549dead3ae5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:277e0a88f463ba1885122ebb9adb881e33bf707180bb0385b13a1bdc6fd284d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53147374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1482fe2c7cb52ea1190dce699b0244f7f4d4fed96a3d1d8b57428646625d85db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:22:45 GMT
ADD file:7eff711e1a70eb1d1484892b9709814001da8a37e00431a22c03764ef9f0a5c7 in / 
# Wed, 11 May 2022 01:22:46 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:22:56 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:74eb7a1f108de67c086990b41789af4c613fa1537617a0d1858f68b66ad33a4c`  
		Last Modified: Wed, 11 May 2022 01:29:54 GMT  
		Size: 53.1 MB (53147154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53993909c717e4d013c439601f248c53a4e43664b7b42dce7a7a630f30f5c5b`  
		Last Modified: Wed, 11 May 2022 01:30:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:bddb06b0f6965ac4b7ded82ced103322547df94ecde0a7e6eeea612a9ea6d959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50940069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8b79f0bb68044d2ae1551b33743f9e106125cbeb6804cfaabb3a67ea6b8d53`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:57:31 GMT
ADD file:3b98d75470b5342f06179d466794e6a231be41b0a3d3c94b6ae0efbdcbb9a74c in / 
# Wed, 11 May 2022 00:57:32 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:58:04 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:be71d4ded79eb5a181be2fe43c5f3f8e0e79c48fcef2a4b538396eb809b84547`  
		Last Modified: Wed, 11 May 2022 01:15:47 GMT  
		Size: 50.9 MB (50939848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5c84c2be9c8faed852a449321696e10b06f0cb595e2ab1c0048bdfba46abb2`  
		Last Modified: Wed, 11 May 2022 01:16:27 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:672848b8cb15ddda5c9bf46ad7b05c1bfa447ddb1ed6f555d38da0da35381cb8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48678526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123f41bb242eb14c0b12594dca8354619a4a779504ff528e0ea245048e633f7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:56:41 GMT
ADD file:feaa047701029ef35f79de94e47613b9069921d84667ea4a3de1dfc6d195b1a8 in / 
# Wed, 11 May 2022 01:56:42 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:57:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b8663dc9a70b670066e8632337e01951b4f2400a973cb02548508d5b27b49da7`  
		Last Modified: Wed, 11 May 2022 02:13:53 GMT  
		Size: 48.7 MB (48678308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bf44f3121f10ba13592a83a999f3403e8ef1f432827bf29458b4280543b698`  
		Last Modified: Wed, 11 May 2022 02:14:31 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6a80a32d1b374717811012a410dfc52e619238796c8eed8116f33258e7c1942d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52261470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6de65e52754902f3581327bd312a08b529c22b64919cee988055cdb4a17a88`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:43:35 GMT
ADD file:2872959d1380a162e11a052911482db0c296636653647605fb8b01d15b6b84c4 in / 
# Sat, 28 May 2022 00:43:36 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:43:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:586b8a60c851194f5e17a9f5238244c2c05921eba7aa586e6c5c0751b9eb1313`  
		Last Modified: Sat, 28 May 2022 00:52:52 GMT  
		Size: 52.3 MB (52261249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ad4e25696e72a1d8837a91dbffa0c00af68f2b910b61506a6a361dd85b28f0`  
		Last Modified: Sat, 28 May 2022 00:53:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:d857809421963c75bac0df791a24fc502a9aca4db33b6fc2f50d8e05c532b0e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54158934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83e5df1e94de4d15d6c0348d65f723a7987fe3b10b9ea2a07167642bf5a42b8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:42:43 GMT
ADD file:ddbbafd9c13cb3214a5f4ac7696a1e2849d91ecdb8c1b7c67e6adf47f5b19dcf in / 
# Sat, 28 May 2022 00:42:44 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:42:59 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:45eb7531e9b10f431a1c01cc0540d78d698cf327a45b3c871e3d2cfda8cf77d8`  
		Last Modified: Sat, 28 May 2022 00:52:08 GMT  
		Size: 54.2 MB (54158713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d2389f7326fa2ce9a33fbb150ee45d7cfcb4e82c07b7d8e164ea9715bf9158`  
		Last Modified: Sat, 28 May 2022 00:52:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:adab2ad28652930d9ba4f0bae9ec059621b659030641352b3d8c21562dbdb1a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52268589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befe5f0f6bb19eb516a22e3099ff692e9ab5aa73dfe1e4b2dbb7a084e694d0c1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:29:37 GMT
ADD file:abfd357a115291ca41c0c5f26dcb21b075edd22fd8fff1174885342ee2d6be6d in / 
# Wed, 11 May 2022 02:29:42 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:30:19 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3265dad9b102c21609195de4c7b031c477dc6fe8ac02054d782fc719ca14b6bf`  
		Last Modified: Wed, 11 May 2022 02:40:36 GMT  
		Size: 52.3 MB (52268366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ee714b46e31134f953f415a6bf5bf6fc29d12c1b99cb2052ee2287ca26c36d`  
		Last Modified: Wed, 11 May 2022 02:41:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:641484f562861b68f84b7331d6e83af90c90244d8fa08ac3434ccf94f6e42fab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57352616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2276562fa92512e728c3e81f9d92dceb3a31919289ed3f6918cc76db4d312fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:37:59 GMT
ADD file:d609df19ea9759b393191a81b6f3f7908587d527836d2da5da57be6553a7f269 in / 
# Wed, 11 May 2022 01:38:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:38:46 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:54515ce7c2170e51c7779447710a1e1f0f0e40fb39cc75ff772811675b7b2f39`  
		Last Modified: Wed, 11 May 2022 01:47:47 GMT  
		Size: 57.4 MB (57352393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7e563103939da01d611631d9c6042ac9ba8841d8b3f030c1e73f77b0faee1f`  
		Last Modified: Wed, 11 May 2022 01:48:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:6a3edc349738b7b8ee1ef03b62a110d421608361d124b935715e220effbbe79a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49377941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf54f5c12ef8c1ac81e298f078d6a5527c58745721e7a2dd7929e74fc89da617`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:18:59 GMT
ADD file:7325edeeeaf5959d6f5659ad3230bcfccaf4d5c3ff57d3006bf46d1d1d7ce623 in / 
# Wed, 11 May 2022 01:19:02 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:22:38 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9be57321a5b75bf9029368d5064dd36539cd46296afd8b04bb83cb9c46cfe37d`  
		Last Modified: Wed, 11 May 2022 01:37:29 GMT  
		Size: 49.4 MB (49377715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82c54cfe4b4cc5c8f89cdc334fc315b35b169ca134d40f28b9b35ae9cdf5014`  
		Last Modified: Wed, 11 May 2022 01:40:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:90add0686b81682f4afa2adad119afbeaea8dee4f6f73ef6c6d44091264a430d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51703461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacac0f07bd4e56d2687ca7ceedd966f6d54cad580588b1c1fb018fbec07d532`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:46:25 GMT
ADD file:ca2f9e70e62257fbacb0eb455cee1752c9404754ca7f5149c70058259220b8fd in / 
# Sat, 28 May 2022 00:46:28 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:46:49 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9fb199d2a2726467db59cf4e8de4009b204a5bc0adf9d148f49c09fd9a992e28`  
		Last Modified: Sat, 28 May 2022 00:52:19 GMT  
		Size: 51.7 MB (51703240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8e8f2b28b94c6e77dd3c005049957ac0cb79b7127f87f3fceea85f39a22ddf`  
		Last Modified: Sat, 28 May 2022 00:52:37 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

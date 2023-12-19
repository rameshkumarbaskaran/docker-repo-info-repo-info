## `debian:stable-backports`

```console
$ docker pull debian@sha256:5393981cec7dbf0875493a0870e632eaafe92cea8925e5c9faf56afea66aafd1
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
$ docker pull debian@sha256:4c44ed4cfcc576ad53b4fe48c02c3edc17be44785cfb8a327dadc0ff466d5bc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49561810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd75205615c761b9acd17e95e98df6378cb672d0d366dd19a883f5d1fbf0df4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:24 GMT
ADD file:974e64d5811025cce8d9e989a8392361edbf995c23a3a768924fe3ddb4e3383c in / 
# Tue, 19 Dec 2023 01:22:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:22:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:002532ca787c14148f31b15b032c7c1cab3a5b6097a69a63c8b46324718cf247`  
		Last Modified: Tue, 19 Dec 2023 01:28:26 GMT  
		Size: 49.6 MB (49561587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e977ecd26b07cfcbf8bc4c56cac9e2e218b09c7016c90bc9016671637a9d203`  
		Last Modified: Tue, 19 Dec 2023 01:28:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ebf4e11a6f637285634fae42ecad185767dad37de8b86e6261cc418c6c1c720f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47319443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f07cfa07b66d353d99c26bcc1add3542bb4409452faeea3843b1b7d7a2748b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:15 GMT
ADD file:c97b8b18bc510a36fc7568227a3dc9feeab9f27529c81042603bf29dc7f868a7 in / 
# Tue, 19 Dec 2023 01:56:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:56:18 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:114f046377e0fe6ae226c6bcb57d65fbf59d7ebda9579444167c5b1933e27de6`  
		Last Modified: Tue, 19 Dec 2023 02:00:56 GMT  
		Size: 47.3 MB (47319219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a000a423cb1dbed74096adcc37d7b957d40a99be2dbfecf24f60958f76fb5407`  
		Last Modified: Tue, 19 Dec 2023 02:01:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:753de1e18aafaf319a010ee1aeb33c919fb550aaaea4f64f1a8b5e95450021a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45180275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18e0373d77b1984bc765ce8c6f80a295e6fd23a4043128e8c4ab0a420b35b00`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:21 GMT
ADD file:9449e70119877a15c4e32fd928c3c66d5ef3bceb73ea3ea9f42a9d37c35114b9 in / 
# Tue, 21 Nov 2023 03:59:22 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 03:59:25 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0681e3a8af101f8eacf74d0544d2d3870674cfb10dea2824fb7a397fcd472bc4`  
		Last Modified: Tue, 21 Nov 2023 04:05:24 GMT  
		Size: 45.2 MB (45180053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8d0fca79629165459821f8238ec1fe4ae3a1172c424e876e413a7e5133ad3c`  
		Last Modified: Tue, 21 Nov 2023 04:05:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:34229a7108edc5af7cb33b80840a58c0909bce213c7c37ff7e590dfd62dff362
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49592467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b62f8e78edc116660289e28295e373dabbe7ecb9b0c41897eb0eacc8cea203d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:26 GMT
ADD file:006303c48e11ab9bbbac583efcf7f43617bae74e8cb11dc00076189eaabc1a8e in / 
# Tue, 19 Dec 2023 01:42:27 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:42:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c799c94ce8e4f581440e2e3757ab64202cde97bb7234ecca8eabdf005d89acd3`  
		Last Modified: Tue, 19 Dec 2023 01:47:49 GMT  
		Size: 49.6 MB (49592244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cde444bc543d1f9af711233b73db63fcdf1d33a3228104c39aeee9a98ac31a`  
		Last Modified: Tue, 19 Dec 2023 01:47:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:d12342087ad5ff012009c44c754680c16aa6e0bf16c862da94052496c6ef7c0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50582512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313544fd1d06a3e3abef97bbc67e59614bad7dfab935068af860a0a4d058c0f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:06 GMT
ADD file:928dec1dc8385cda860622eab7a5637b4209dc1815bf72efdc9daa42c87ef48b in / 
# Tue, 19 Dec 2023 01:41:07 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:41:10 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:985bd0cb96ff99f303bf1684f14b4755022f384e8342dbf1d60a98c1032f559d`  
		Last Modified: Tue, 19 Dec 2023 01:47:33 GMT  
		Size: 50.6 MB (50582288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74029a567f9ae1e1d4bea72d24a4a13732b660e84fbf9e114b1b1d601e06247a`  
		Last Modified: Tue, 19 Dec 2023 01:47:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:b07cd493cde05727e40aae8dcdf2b9afac95cf137b0ff9216bb7f05ccf4feaff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49569426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a98d0c9b4982500fb10abd555efeb9019a3d6bf8bda0672e2adec3fe8cee14a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:13:53 GMT
ADD file:484363709951b76cab1fbf3e7caf4f006bf1917127ca9071365e8ba20c80ac88 in / 
# Tue, 21 Nov 2023 04:13:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:14:08 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:71826ad9cef5309b30c1a728078ce3b7e80a5780a5ccd856baa4c9b62d4dc295`  
		Last Modified: Tue, 21 Nov 2023 04:25:06 GMT  
		Size: 49.6 MB (49569201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ef25057da3fa431d898ed964e4ab60daa84bb674e3b118c298bad4c5726fa6`  
		Last Modified: Tue, 21 Nov 2023 04:25:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:084ec186ea31cded3e97ee579b9fee2781372ff6f3e4eceb2700484b7103d992
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53557996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718de308fc35a7ed537146576854d528c287c920bbdc0eb4608c87a88347fceb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:23 GMT
ADD file:2c624ccc003d0f4104b35cf3bf6cccfb35c9a0b709cab7aabcf1ffb0f719c5cb in / 
# Tue, 19 Dec 2023 01:23:26 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:23:30 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:22d8c758808e8ea3211f06e4878a686b3a00746270bd384d9f1149eafcfcdfae`  
		Last Modified: Tue, 19 Dec 2023 01:28:51 GMT  
		Size: 53.6 MB (53557770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89559c3fceda95cabf3bc28d81e650670c61411008392b2d15c37c2be1fe37e`  
		Last Modified: Tue, 19 Dec 2023 01:29:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:1d0db160cf5b5f49e6210d9c75123cb9ac19a634e2c60e72b5952918a126e67a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47917900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d27d3f0bbdae6844d052a9b8ec40acd809958e875eec7723b69b2c26252825f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:44:24 GMT
ADD file:0c60c17ec958129c457b177efb3a02b9aed5079a6063502e7a569ff0d0e446a4 in / 
# Tue, 19 Dec 2023 01:44:28 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:44:36 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a009a03321579bfa9e1d2f2e39000c66b62221105b6b0d80f67a5af06b8285a4`  
		Last Modified: Tue, 19 Dec 2023 01:49:05 GMT  
		Size: 47.9 MB (47917675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0dfffc600871a62f4c7966ce9f31540f967d210e0870cac450f65e02565a9c1`  
		Last Modified: Tue, 19 Dec 2023 01:49:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

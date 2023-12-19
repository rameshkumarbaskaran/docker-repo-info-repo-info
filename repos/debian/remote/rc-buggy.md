## `debian:rc-buggy`

```console
$ docker pull debian@sha256:fb7d5d88eb2d8d1bc38b9f966eeb73b5561055bfb27fe00a5c2c67638db809e4
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:2a026318e1bb6e45a48b9458bd92cb0bb53bf5073bfa68b1bbe8e4ecad694e80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3766ab6d919fc19ed884d5eb0ec2d438834925d98749008d92f9c06fa9ec73cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:05 GMT
ADD file:0e0fcf0b6bc9c9794502332cd0f45625ac991c8a06ab284afd8673f8d5ab789c in / 
# Tue, 19 Dec 2023 01:22:06 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:23:47 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:716f2525263989014ccf51727e00b6ee9f74018b7b13e996b0e06409e58a44a3`  
		Last Modified: Tue, 19 Dec 2023 01:27:57 GMT  
		Size: 52.2 MB (52246819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568fe11e3dce860454342c965dd51b99e6e835e1a5c9d576b63015b50555fc82`  
		Last Modified: Tue, 19 Dec 2023 01:30:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:969c6f434041ae3d89495225bbf4f1d98ddb8530d6f098d0c013e16c44fd1f87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47266319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2c7a39badd9c54abd462e852d7557994a42828f9e917b92f363ff98e83de3c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:00 GMT
ADD file:cd6b2b4b3b0e27503b12f67c0901ed5145dc3891d490c198b6ea77c5429c7ad7 in / 
# Tue, 19 Dec 2023 01:56:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:57:17 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d5110329ab47599ddb3bc004401c37c9cde68589c2b2734abaaef4fd51bb0f3c`  
		Last Modified: Tue, 19 Dec 2023 02:00:24 GMT  
		Size: 47.3 MB (47266091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea16ea986653d2a960c6cd03b5d884eb058bfa7b6f5d38ace956de672077496`  
		Last Modified: Tue, 19 Dec 2023 02:03:16 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:e52fedcf6edd4c706c156c0b35015aa1781236f6f866195c89c2eb9d016c5764
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44844229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303ae981dd46775d4a21637de89e227fb348692426f180c62acc6d49cb1b90d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:06 GMT
ADD file:300e7cdebaf8999cab26cc13f0caef83295eaebe10c56ff0cfdcb09387bcbedd in / 
# Tue, 21 Nov 2023 03:59:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:00:29 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f6354053edcb23852d2428872356168d7673ac95fa04b1372761f8a7903e034a`  
		Last Modified: Tue, 21 Nov 2023 04:04:58 GMT  
		Size: 44.8 MB (44844003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c7d129b9a0ddd78048ef7dc6056515f3ff8600173748ae3f38cc77663bb646`  
		Last Modified: Tue, 21 Nov 2023 04:07:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:74fc3fe5c682aa587c532eec9a3b79b914a2308fcaa55e716243fc88bf4d2c98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49690012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11a9d7fa354b376b5496725eec9290423b802ddd030148698f8d9ee9a208d86`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:13 GMT
ADD file:b95bf5556d43a8a1d79a2dbf26ab8a4a912869d65cc1b76a372ca80259a65b7b in / 
# Tue, 19 Dec 2023 01:42:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:43:20 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2f38ee39d2143cc6781c8d40b267519e59c558f7902df442f2e5ecfcefb01689`  
		Last Modified: Tue, 19 Dec 2023 01:47:24 GMT  
		Size: 49.7 MB (49689786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425bbba4e0a57512cb5fcf33f4fb9b5fa3dfb85a0987654d9dcdb56ce3b52822`  
		Last Modified: Tue, 19 Dec 2023 01:49:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:b8c876cc8672e7785253e55fd2b556662dfc0865a211685264e414f8bb12d0c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50559471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce0d84c346bc0a87f3b0a36a5825f1f1845f7a093aae23930e300fa68625f5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:40:47 GMT
ADD file:736d4b14c103f5161855a9c14b05565523005af03b61bcfb3d6bfaddee9431f3 in / 
# Tue, 19 Dec 2023 01:40:47 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:42:27 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:567001fd97421e53b722a950bba83f44d7635056bc895f0b4f77b68d779fc15e`  
		Last Modified: Tue, 19 Dec 2023 01:46:59 GMT  
		Size: 50.6 MB (50559243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b69462498819755a22188daf05d93b8d7c8ee149ad4f6ab29cfbd1467ddec2e`  
		Last Modified: Tue, 19 Dec 2023 01:50:10 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:5414ec4d9dc1530199db67dcf1f5b2b377814ca0dcfe1e7bac94bd4df4df2596
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49342076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81de3b7251029849d5a4a0b8e2e3f1fdd78b843725171398d670070649a1ffac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:12:53 GMT
ADD file:9030cb9b65f8be61ec19318a90c95afaaac8943c61f5ee6b30b90d758a8b0964 in / 
# Tue, 21 Nov 2023 04:12:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:18:24 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f090d405a1df972a813ac2207398b0e5b36cca91650c17a34fb17616a3e7fe19`  
		Last Modified: Tue, 21 Nov 2023 04:23:59 GMT  
		Size: 49.3 MB (49341847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8c2216abd403e6c3817bbb652662acd65fa5ac992c812b77595e671dac7e71`  
		Last Modified: Tue, 21 Nov 2023 04:29:32 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:c01a6aa2b7497918af872536bffb3d9766be431fe26b75a462cb324cd9f2055c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53455943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e3c38635b0ee0688b5428ecea9489c4a4e517d8588a6b9c568c5607399e7fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:00 GMT
ADD file:ebe2bb6638a51888bf27d1bb5ca609a91df94474b4abf70f874e60b653885a2e in / 
# Tue, 19 Dec 2023 01:23:03 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:25:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:97954753acf4d5cb589b2a49219ffbc5c86834cb864ed80f516370017ea3c569`  
		Last Modified: Tue, 19 Dec 2023 01:28:17 GMT  
		Size: 53.5 MB (53455717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fb21c489cefd9fc4f932b3033c97643b520d95cfd53fd638d83d4b17f44aa1`  
		Last Modified: Tue, 19 Dec 2023 01:31:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:350c66030b3c2607eceaa1f5674f3e354bd3b0a05e82e3e41d25099cfd100b49
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48206925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38251ebf979c3848dd5b5688201fe4f73140f7afa208727d1c5f1fb0fb3525f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:09:02 GMT
ADD file:6edb177cc4c3fc7c02043410bba7fabbbaa23493a2e0444ac13e281f6fd7d209 in / 
# Tue, 21 Nov 2023 04:09:04 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:10:55 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9197643899c29fb1e411101ee2f4e677b44704d5c2c8ce98f7567cb7f7a6cf58`  
		Last Modified: Tue, 21 Nov 2023 04:12:00 GMT  
		Size: 48.2 MB (48206696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87a0b1ff193b58db96549ba0868a2144983d6a34e417cf1e7a294b41d032008`  
		Last Modified: Tue, 21 Nov 2023 04:14:20 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:24d1f78c5160652c7658e48b5fdb943c11a5227e3d00152a57b71d12c42cd0eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49328407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce673deb6216c3c18f167e52ff382e054d8c03e77cf678751560a1d4c4b0e33e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:43:58 GMT
ADD file:787d19e6a77aebb4de0df132b1de8d62f9d4c2c2d0181bd2c57d043a742aba66 in / 
# Tue, 19 Dec 2023 01:44:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:46:28 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:81a71db9a04e29cf0934e3f04c4935c1dad336d34d53ea6877240b19747c865e`  
		Last Modified: Tue, 19 Dec 2023 01:48:45 GMT  
		Size: 49.3 MB (49328178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2784c847ceb2200368be66cd19887fe31ba49bf3ffe66c29c9341d0c85ec1f`  
		Last Modified: Tue, 19 Dec 2023 01:50:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

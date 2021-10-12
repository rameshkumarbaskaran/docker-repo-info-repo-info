## `debian:rc-buggy`

```console
$ docker pull debian@sha256:86dbc72e2ecf04776797974bd1b8c1bc842fc8940b2c769b8647671fea17a22c
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
$ docker pull debian@sha256:722413f4338fbd7f3c207f36253cc413329c494c41cecdfc3b61558957fbbd09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55687696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89962650274438b586fb32a8bf22cbe35391e77b387c5fae95fb0f148172429b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:58 GMT
ADD file:2d684471f088173801ff86eaf94c1d858b74220b84642d73b02bd1bfe0d54b60 in / 
# Tue, 12 Oct 2021 01:21:58 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:23:43 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ba87283d9c312600aafb7f4149986884d524aae42e0701a90d2fc23c85e977b1`  
		Last Modified: Tue, 12 Oct 2021 01:28:21 GMT  
		Size: 55.7 MB (55687470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26674154af9f7ba052f74e417b6322bb9f6e88a25c55d070d5a3c05cc3587b1`  
		Last Modified: Tue, 12 Oct 2021 01:31:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:7b6405b207f9d0e7cc57586feebe2ca61efcaf79ab2cc70db866170365157b9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53186577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ba8704ecfff8b7fac421cf93e23ee0ceaba7e4348758051819d0ea539030c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:53:53 GMT
ADD file:2918872df07d47b9a7862abf3b22f39600ab45587fcd02466bdefa775a3fc2dd in / 
# Tue, 12 Oct 2021 00:53:54 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:58:26 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8f73c109c91bd2f18faab4d6862ba33d940956d6457aaaaeeda5e8f72281edcc`  
		Last Modified: Tue, 12 Oct 2021 01:11:00 GMT  
		Size: 53.2 MB (53186352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf674df9fccabd4879c5e06d5d0e93ce0977242d5abe4ae7811fbd707df2cbb`  
		Last Modified: Tue, 12 Oct 2021 01:17:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:8a13ae66758407abb43d05380da8fad9dc85c9f8da996ae19f0bee1ccc5370c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50797295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144ae178316232a427863aecbccec0ba4392733300ca6fa591fb4c1dee73d715`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:32:13 GMT
ADD file:defbc06b1cc21db01a673f118d34d129435486fcb83814c5c987ff566c61360a in / 
# Tue, 12 Oct 2021 01:32:14 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:37:02 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:153dc8e6452cda134a8143d2ac887e7ebfa01c8568115d6b3172ca0008ef4838`  
		Last Modified: Tue, 12 Oct 2021 01:49:06 GMT  
		Size: 50.8 MB (50797066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c760bf384122a608ddf9bad0ff3fd4d156d88feb6ff4a57c7486af04b20b1def`  
		Last Modified: Tue, 12 Oct 2021 01:54:47 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c3560a23bfcd3e13cca0a86f250a88300f8155ebd4851ca8fe93cf3580a564fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54703123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1102d8396514ec2783d970021bee45096e4ff166fee918f2fdcee6d8e77b156d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:42:36 GMT
ADD file:830671e1709a0164ca60ad1012d3d0202e7e63c74bdbec7df54f308a4d4c8b11 in / 
# Tue, 12 Oct 2021 01:42:37 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:44:21 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3ed37bc205e0aad196bfd6ba235a1a5fba10e02175afd192c816df6457d06c75`  
		Last Modified: Tue, 12 Oct 2021 01:50:51 GMT  
		Size: 54.7 MB (54702895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96db8976b7344422b08e4e1070a5fdb6c26dde35253c22f707f92aecd437d20`  
		Last Modified: Tue, 12 Oct 2021 01:54:27 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:e16202c4c6bf73470ee2c337cb97f6c85e5831dabff86bb201926d1f55715211
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56716331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa85f16c497abe3b358e4a5b2f347e154d6531d11acd83c88b58fdbded6f9e38`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:27 GMT
ADD file:9ab0c16547aac0a32292246b35737ca5260c5942d5e26ca1381be39c9e321ee5 in / 
# Tue, 12 Oct 2021 01:41:27 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:43:39 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c36fe1aa4217cf0326227a0bdcadc16e85d2670bd6485518167903dfc6934c65`  
		Last Modified: Tue, 12 Oct 2021 01:50:33 GMT  
		Size: 56.7 MB (56716103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1170e260d363b1d2cdf209f09b5c8384055f728a512bb00e0f6a63b46b28df03`  
		Last Modified: Tue, 12 Oct 2021 01:54:22 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:c44e0fba235b23b0bcca787bb299f4d6592fc26b40875320de8878a32c67f07f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54313696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646adfe0abdf4cf97717d9f3bc2a761ff0da628fe34667dd3d4f08b919e5fbe5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:13:27 GMT
ADD file:27e1d46380432bbd287bef3c049b6707a409fa2f49f07e76f4826c6ee57cfca9 in / 
# Tue, 12 Oct 2021 01:13:28 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:16:38 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c7afe2e09744237d99a12c5f86f33ba55800e5acee482662abac2c64c64a7824`  
		Last Modified: Tue, 12 Oct 2021 01:23:41 GMT  
		Size: 54.3 MB (54313468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a771580da0d6914e7ca5bc4bc6f45b58872192457aff8bd17de8c5491e53bad9`  
		Last Modified: Tue, 12 Oct 2021 01:28:27 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:8871ccce0b68b6b8e2f377f59816546c7757697c61fcea960b191e44ea775001
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59889396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16346dd33fc3f506b4950f71d8af23d5ebcffdd4a66f5776c8b9748d224f2f18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:27:58 GMT
ADD file:975422ef5390ff94fc050a84a9840e39188158f1c74f7b6dfde93829787b7c8d in / 
# Tue, 12 Oct 2021 01:28:07 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:31:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3794e49fdef56187e1a7ffe8a3c0d0dda8a5b5c159e370831000df5e5f638479`  
		Last Modified: Tue, 12 Oct 2021 01:41:02 GMT  
		Size: 59.9 MB (59889168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f376a4c7a802fa7692086dc3096f4d65493c272843b8ac365023df781c43cd`  
		Last Modified: Tue, 12 Oct 2021 01:44:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:5ffb0eb3ab03534c0bfbddd6627cbde5d521e9b3faa0dda11de1065cb8732809
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53940968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c756aa74b7bcf61f84a3f6be1fbb83ed79221862f8d4491fec7edf8d71b422e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:43:35 GMT
ADD file:d0d1a83115052a10810bdba27eb855359796f604b655de31492b0699abf1d546 in / 
# Tue, 12 Oct 2021 00:43:38 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:45:17 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:979a8d8677c5949943057dfc51bfa612e3d365d71df4150210296bec00f04cf2`  
		Last Modified: Tue, 12 Oct 2021 00:49:29 GMT  
		Size: 53.9 MB (53940740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432f1b4f0043528ebb69390269b5fe14396b57669ae96173a8a5c35110eaa8ad`  
		Last Modified: Tue, 12 Oct 2021 00:51:20 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

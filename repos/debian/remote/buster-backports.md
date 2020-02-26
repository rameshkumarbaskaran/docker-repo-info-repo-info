## `debian:buster-backports`

```console
$ docker pull debian@sha256:5947c8c58ee1213b434fcbd1c4df9e2e355bb891c67bc73c01ae76fcde31e9c9
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

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:faedebd1080518f7f7c1a7bab0160caf566fab54eb0553452080ec127a091a00
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50382195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822309de5c4dc2ecdfa820cba5d2dd1b0ce1f8fb5adcf5dd49c1de574a19f413`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:37:12 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4581f5c2809f39b45193c155f2a01361e056e3bc11d60585f225c96808fde50a`  
		Last Modified: Wed, 26 Feb 2020 00:44:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:895a3b416d45846f6086a1e1c7866fd60fd0fd251a0d3eccab1ca8d53e951ab4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48095896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ee49cb2091c9602c2bd070e0d727466caa987ff4139cf3d046984b0a14c687`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:47:18 GMT
ADD file:c5d04d0713a74a05133d8fc49f69a750c709995827984d401d465d98bd5617d4 in / 
# Wed, 26 Feb 2020 00:47:22 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:47:34 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d16b9694b13fa6f8cd07399e1efcfc873f65232f05b1c9a7efabbcee33aa682a`  
		Last Modified: Wed, 26 Feb 2020 00:58:52 GMT  
		Size: 48.1 MB (48095674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84dec23752642e626b14036ddd682e50749b0b8c53ea8d57b486e78162b5db2e`  
		Last Modified: Wed, 26 Feb 2020 00:59:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8c4f6f6ad19d9372785bbb5204dc5c615c336d47c7e8a9567d80c8aa7a16852a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45862916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14e10a883fd4a9789d7ff762c5f8c7ade51585184e3b786974e8df6374668c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:58 GMT
ADD file:38fdfcc3155e437ce162aa0ed9dcdc5893b8145e2f3ede2858ed2187d79bf718 in / 
# Wed, 26 Feb 2020 00:51:08 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:51:45 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3182cf45068cd9734abd8e38dedbb9930ede35ee8c11376ca2684e86f9a1aa85`  
		Last Modified: Wed, 26 Feb 2020 01:07:03 GMT  
		Size: 45.9 MB (45862691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858e8d39797535c3ded2ce2eede93622c594e15d2a37781986adc1497edba5f8`  
		Last Modified: Wed, 26 Feb 2020 01:07:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b6a4b84f0182d587c55c9086ed72aaa67b93e00d2eb6f22207a5d07de256b0b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49170200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2be4403b217cedb1a48b309a6e1670c13d72d930de48e0b3ad629c482f0b4e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:46:17 GMT
ADD file:e3320653f0d517a6181aa46fb47407790018e2d8dee590005ffdbee3d04f72d4 in / 
# Wed, 26 Feb 2020 00:46:19 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:46:33 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:77b067f4ec14d48dbc8cd83b7a46fbb5f21fe01ea8911db256cc0168a30c1f5b`  
		Last Modified: Wed, 26 Feb 2020 00:55:50 GMT  
		Size: 49.2 MB (49169974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb0da28503234ad72e82a1b7e61771c42a1405e25f26dd741b0811cda27487a`  
		Last Modified: Wed, 26 Feb 2020 00:56:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:26453c379d6f651440e21121186880766ae46b9f362d2690a82e75d094800cf5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51146351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3051f2ced1a47433e2448118c645a4037210964d001f6de3c8a3ae0bcb6690e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:31:58 GMT
ADD file:1deff975480520310bf2c8d3708554d98c696f82689f0b67f9a834217c861803 in / 
# Wed, 26 Feb 2020 00:31:59 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:32:04 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9450e7c48681b3ba36935d4e7d891b4b180d4d223a6c938faacb41402857ebd3`  
		Last Modified: Wed, 26 Feb 2020 00:38:12 GMT  
		Size: 51.1 MB (51146129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff182f9bed243b709f73339aa44e8b60fa8ff572c6865fa6015a0ee228cd3d1`  
		Last Modified: Wed, 26 Feb 2020 00:38:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5f40143fcfbdc08eac2ed03310655da82a249311bab9a894d8459a7e47a0c9dc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54138669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24532228703568400857278f70fec240b9ab1094294e151fc04d4c0b9f6852c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 01:30:27 GMT
ADD file:b58865b3fd36d440998ef82e567179a9cd6b9ce0343d5e5a15a0b4f856f211c7 in / 
# Wed, 26 Feb 2020 01:30:35 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:31:01 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:928614537d6dedbdf79cc24c5c56bf98c3ed88f9d91a9ec1105d2a133611b0fd`  
		Last Modified: Wed, 26 Feb 2020 01:49:54 GMT  
		Size: 54.1 MB (54138444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf880a3145e71fe3013e088abefbc10173e483f18724ffafea27df2d30682db`  
		Last Modified: Wed, 26 Feb 2020 01:50:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; s390x

```console
$ docker pull debian@sha256:14b398a4716b683219345f752f902460f7604f03c00f6c37002fbcf0d238b7ef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48958254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6556e85adcc4f2ad3f0bb3dab3eca8dab431fb4db69d49e789a2859039fe823`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:42:32 GMT
ADD file:80536bfff518f6b425ad359b86a124f79ccdc82deb3e648f1746a7c87a1fcad0 in / 
# Wed, 26 Feb 2020 00:42:35 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:42:40 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0a3603da42bb9e22573006a7f894b198954caeab529e2e041660e12c4fe62462`  
		Last Modified: Wed, 26 Feb 2020 00:47:26 GMT  
		Size: 49.0 MB (48958029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace78acb29997f2507179f1fee51bab7274bf0edf5a5fdea7bde50ca63bc93eb`  
		Last Modified: Wed, 26 Feb 2020 00:47:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

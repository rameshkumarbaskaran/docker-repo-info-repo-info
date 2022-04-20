## `debian:experimental`

```console
$ docker pull debian@sha256:cb04d19d1d30b87e68709a15361dcb0f6a378589a4626ea3d6a3ae3b48f92c20
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
$ docker pull debian@sha256:220bd5d9a869e9c16f5e40369d4d95f848deb3629bdcd830ce7b245dfd558541
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56112901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baeded9577302da4d155448d989777fbbd01564a09c102e50529f25a71cc5b8f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:45:55 GMT
ADD file:b8f07060f9d2d7f5c4db9947fd089591ea261222b369890ff85325ec74bc0a6c in / 
# Wed, 20 Apr 2022 04:45:55 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:46:08 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7c26de214b349330f4067f62eaf7fbc9c2e817d82821b54e517e1456eedf3030`  
		Last Modified: Wed, 20 Apr 2022 04:53:29 GMT  
		Size: 56.1 MB (56112682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f1ad2473963dd6a11702bae6dd1105ba15fa377ce0ac90a6dc700e73c1089a`  
		Last Modified: Wed, 20 Apr 2022 04:53:53 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:97568c05d35b33eb71f48e3e947dfb64bf264990f82ec8d0877441ff7b1619f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53206651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18871ca247f13cb8b83c19bd8703dec805b23ff4f5db197e10d5e11eb65c614`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:57:32 GMT
ADD file:627cf63ff14306acc7a49cdecc211f5d763900394ac428921aaf05f33b92edc8 in / 
# Tue, 29 Mar 2022 00:57:33 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:58:06 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b56bd4af1a3d681c37d855323d49cc2c57a13df176437359f0c17d85e79b4620`  
		Last Modified: Tue, 29 Mar 2022 01:14:49 GMT  
		Size: 53.2 MB (53206427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8efc072c4de5cc13fe2fda957e77b1c10cfd79ae7a88edf399436fbee55227`  
		Last Modified: Tue, 29 Mar 2022 01:15:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:21a33ab43372dffc9b45615b42b85ce44a0bbb880b3a7bc7bd9c1a69348f7eb3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50813562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5e8922419bfca49748a0057d97ada05bf46e97203b753860d263f74faa690a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:26:03 GMT
ADD file:bb90352585198bea90f2bd0d7964e8517e01731e7c955f66ceedd059fa9ba98f in / 
# Tue, 29 Mar 2022 02:26:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 02:26:37 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b605358dcc0a53886bb25a6e929d6a2d7e4a45660e7d8dbcae9cc0b75ad566fb`  
		Last Modified: Tue, 29 Mar 2022 02:43:12 GMT  
		Size: 50.8 MB (50813338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077b8e9194028fd3aa880694b3e4ac70fab3336f2c48ff38ed7dcc305def53af`  
		Last Modified: Tue, 29 Mar 2022 02:43:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6a2de964a9853b6cd0bb86c9d4b131d6eb91de19718c82f94be97b13bccd6db9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55064029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13bf1fdf8a672da09c712249542936165a2606d4337a9a7ce95bd052f890e68`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:32:09 GMT
ADD file:ecf4c1717eb6fdd76f39aa7c85e910a5b33b82a012a3115872223977e906fc6b in / 
# Wed, 20 Apr 2022 04:32:09 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:32:24 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2b3f6be4af088219c3879fb497cd5051ae20697284c5fbf8f47d4d9f017ba3c2`  
		Last Modified: Wed, 20 Apr 2022 04:41:09 GMT  
		Size: 55.1 MB (55063807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef30381bc5727e5e206a346f30d3d3d0fc4f4adc0d9567fd094b50bf1e419ca`  
		Last Modified: Wed, 20 Apr 2022 04:41:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:9a78e7953db41c32e17dbd3d18436b61039b4d34eb28d085776e41f8b6788b5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56838728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455e4cb6b8efb9c441d178234e0a8357c113f89285a9a596d3e905b4925b9778`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:01 GMT
ADD file:0fa764533e4c7ad26fc8de3e8d581fa3bd2756f870a589cd2915ea90e02c665e in / 
# Tue, 29 Mar 2022 00:45:01 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:45:16 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6d8326cc08478b4881b9f386341d1dae7207a138e6cdb840a7287b6e87870ceb`  
		Last Modified: Tue, 29 Mar 2022 00:54:48 GMT  
		Size: 56.8 MB (56838509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bcbf4092fb985796fd50b7b3e0d06846999e5471a227837e6c87acaf3d4267`  
		Last Modified: Tue, 29 Mar 2022 00:55:16 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:380732e2f87214c28dc3c99bcef41b4a3b79975681bfb04fe37b414e7d374fe0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54453695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ead74b7d8a28f3208a7a6a89d4e79b34e267a0a49f7754baa33267ed57a75a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 07:48:39 GMT
ADD file:1f36bf26ba6ed5898744d070089c9800f3701bbe25ca8e98ba248a56b990ac09 in / 
# Tue, 29 Mar 2022 07:48:43 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:49:26 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e7de11e455a9a72d18dbadb02f9098da749f18656d04d5f21c6fbb1ea7ecbfb9`  
		Last Modified: Tue, 29 Mar 2022 08:00:01 GMT  
		Size: 54.5 MB (54453472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad296dfca336d4fc2f7f9dae99c7ee263e1a5e1d9400df740ad175173f34666b`  
		Last Modified: Tue, 29 Mar 2022 08:00:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:f068051547512ff8de3c78015a3efce0208975a42f57bfc76b836772ada33611
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60217500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984502fc84f1754535a0b881f3c9c763465a8fe5863d751e6166d54f436e7d61`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:26:38 GMT
ADD file:bab69b6323113072c808f84ca03ca757728f0805554520fd88a747cb147e2a56 in / 
# Tue, 29 Mar 2022 00:26:42 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:27:15 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a4d1ea8098199f274f1ce3dd6cb6931204d943026af0843be366bbcacb49e516`  
		Last Modified: Tue, 29 Mar 2022 00:40:30 GMT  
		Size: 60.2 MB (60217277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61927c852a7804b2882117724b4852d1a3087be0b4e5b4071b4cc768cabc779`  
		Last Modified: Tue, 29 Mar 2022 00:41:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:a1cead4d44ed77c5662eac9f2429556006120420caba2d19a63ec196fc62a185
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51757584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3dda1884db97d35d90d8cc9d6e29762b5d5a1efaa65abe6947b0ed8470c295`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 00:19:42 GMT
ADD file:eb73ccec6d534b35c3f0725251b8917d96bcd87d77d960d0a879ca91d2530a47 in / 
# Wed, 20 Apr 2022 00:19:44 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 00:23:27 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:62d036327287ffa181f78db1cedfa9a2d2ddc4c54f3c3838d75dae32e11ff1b1`  
		Last Modified: Wed, 20 Apr 2022 00:38:38 GMT  
		Size: 51.8 MB (51757356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6440a805ff86b05ccf55572b7ebe62afdf80683fe40032330d06f9f2896e63`  
		Last Modified: Wed, 20 Apr 2022 00:41:41 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:8265f8ad25b9b40703c3298c79db6bd1c12548ab733b34d590aa3a736206e8b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54056673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdc19bdf0a070f79b0bf435ded925003ef2e94f9086b401d2831e6f8bcbe6ea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:54:26 GMT
ADD file:1701ac5d9716a28d75da0001da8b427a9b13cffe483f2c3a9fdbb11f7d5d4848 in / 
# Tue, 29 Mar 2022 00:54:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:54:45 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:05291da6f57708b1e30a4e5eb1299cb2aed0b38669b61431ed6c04156317bfab`  
		Last Modified: Tue, 29 Mar 2022 01:28:40 GMT  
		Size: 54.1 MB (54056451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dabb95c9834d77d85a48f41ac0834d59aa948fb7ea95bb5f414dd9dbddbd9f9`  
		Last Modified: Tue, 29 Mar 2022 01:31:26 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

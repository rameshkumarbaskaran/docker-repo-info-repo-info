## `debian:experimental-20220418`

```console
$ docker pull debian@sha256:4a030b8cb1a36c270d4e0233f9d7680ab676dffcf3adec6c4f00dc7580cee5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; riscv64

### `debian:experimental-20220418` - linux; amd64

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

### `debian:experimental-20220418` - linux; arm64 variant v8

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

### `debian:experimental-20220418` - linux; riscv64

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

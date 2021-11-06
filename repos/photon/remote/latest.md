## `photon:latest`

```console
$ docker pull photon@sha256:e66a95522bc0e573d03e622dd60ff0287c428a9d87728493fbea0c49cf606dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:955c8907a76f84e656b698913eab9a96a08eb23743dcd328518475639dd9500e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15971814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1297f6546accd6725f4501b8ec101b0c615cb51e7be8ec9bf140da9f050c205`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 01 Nov 2021 19:01:41 GMT
ADD file:b7e352405c142091d518c44b65a3932ec47ccf2b0568027be048a580695f151e in / 
# Mon, 01 Nov 2021 19:01:41 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20211029
# Mon, 01 Nov 2021 19:01:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:53cfa89c520c131f17bc57b64c3b3d190f1dc8666010ce2ffd9b09011665bb1b`  
		Last Modified: Mon, 01 Nov 2021 19:02:31 GMT  
		Size: 16.0 MB (15971814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:f6c688586dbd1e701babdfd6c9b782724b1b09775a84560996c868d09578aee5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15011183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf03042fe34b6917d96a68733102eb1851c9c3c635bc9c27f783a3cdb10ef0b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 06 Nov 2021 00:43:47 GMT
ADD file:bf02ff7235fe3a2024f388308f9f759750cee65040c81d86f8a3a65fb6bb4618 in / 
# Sat, 06 Nov 2021 00:43:47 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20211105
# Sat, 06 Nov 2021 00:43:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:44cbf1f6bba20bd80280d7b4d63c5af59fb58527047f3d0872bcd0d82724ac99`  
		Last Modified: Sat, 06 Nov 2021 00:44:16 GMT  
		Size: 15.0 MB (15011183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

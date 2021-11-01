## `photon:latest`

```console
$ docker pull photon@sha256:e895242ac472a83d1adc8576267818c5701bf844a784e13cd80627a12e8dd708
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
$ docker pull photon@sha256:a51a7f16d9173af3cff51de6036bfd28270cd6edce00c90238828c568d33b707
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15006227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869ac28def796e4a9906633a78a77624d018d7ad9498ef8ad2bc7b581f04c80c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 01 Nov 2021 19:35:59 GMT
ADD file:dea9e85d20ecc6a5e64c8ba7a1f27d98946706d3418082cf76bd522ce6d71c74 in / 
# Mon, 01 Nov 2021 19:35:59 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20211029
# Mon, 01 Nov 2021 19:36:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:93159618a592dc6987362a88048bd615c37890bfc561618c5d9ca98f86bfe8bf`  
		Last Modified: Mon, 01 Nov 2021 19:36:28 GMT  
		Size: 15.0 MB (15006227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

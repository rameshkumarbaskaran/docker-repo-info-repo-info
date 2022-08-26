## `photon:latest`

```console
$ docker pull photon@sha256:0f74263c6d1bd2ac2c0fd85e796c2ab58071e181f91c5fda40e3440101c137bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:4e22ec014a6792dad49ea01b12dd4ddfaa05cb372f9e3991b57a717736c42108
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16053600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adbe6fe514f43fafa21954043e2864c972b6f7e53ec36588cf4a4806a9804eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 26 Aug 2022 22:26:12 GMT
ADD file:b8fc8cca974e9320a1df41fa6a6f3e979af8536e1a7367820548e8e4c1fbe972 in / 
# Fri, 26 Aug 2022 22:26:12 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20220826
# Fri, 26 Aug 2022 22:26:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d28e100d9e5c2f4e6abf459d1702a45ddd9b079a4c83e373573385ad1410563d`  
		Last Modified: Fri, 26 Aug 2022 22:26:31 GMT  
		Size: 16.1 MB (16053600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:539cb13fccf0f930a6f97378fe02ea587a407f81553c13cc9d8adf49a9712a17
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15126928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b96b0eb79837841accea9bc6c4fab2c7f310a3672f5539d7ca6bb8b04f7594`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 26 Aug 2022 22:59:30 GMT
ADD file:bfce12b37a69a2e6b6ae70b6dc8a5ed15f32369ff09ca4bda63f8159eb73d9d7 in / 
# Fri, 26 Aug 2022 22:59:31 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20220826
# Fri, 26 Aug 2022 22:59:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4a249306893b2876c04fa04eb98890bb1de6386627c5de9af666799aa25eb260`  
		Last Modified: Fri, 26 Aug 2022 22:59:55 GMT  
		Size: 15.1 MB (15126928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

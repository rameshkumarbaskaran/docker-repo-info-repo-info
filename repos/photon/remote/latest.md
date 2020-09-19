## `photon:latest`

```console
$ docker pull photon@sha256:987ba38c484536d5dbde6c7e56a5fe71b07bb16be56d6be198c3b32fa6348663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:10606fd0cdb05751c0d8302f6cf446fc8d4d8a0abe0845ab7c787d2419f1dad6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15208661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92a3b2018c8077fadd07ed0c7ae2607f3f61a8ab54b25e5e9531cc115fa3ceb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Sep 2020 00:26:45 GMT
ADD file:0a781902364db6ae1bd60ec507c647a67f747ee7f48279b1a51d8b695ae05f89 in / 
# Sat, 19 Sep 2020 00:26:45 GMT
LABEL name=Photon OS x86_64/3.0 Base Image vendor=VMware build-date=20200918
# Sat, 19 Sep 2020 00:26:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1019cf99a3e50d8f15af0f3178bc58f0074fa58c4de9cef0304e28f09164b504`  
		Last Modified: Sat, 19 Sep 2020 00:28:32 GMT  
		Size: 15.2 MB (15208661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:c70802bf03c036adb11ea53f78302e905f6f03bc26c10b63e88f2b6162e59545
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12994420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03801f0f317058e7c61e2f6a0a4cb65da8e1df62e48ecead9df8e9202165221e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Sep 2020 01:05:38 GMT
ADD file:aec7c0ded80819c2aa4ecba9cc48be150e0b23881218aae757572c57eeb099da in / 
# Sat, 19 Sep 2020 01:05:40 GMT
LABEL name=Photon OS aarch64/3.0 Base Image vendor=VMware build-date=20200918
# Sat, 19 Sep 2020 01:05:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f0acb4964b403b19c2a969071b07f348eb5ae80aad9544269f18d2fa6b33cf8f`  
		Last Modified: Sat, 19 Sep 2020 01:06:08 GMT  
		Size: 13.0 MB (12994420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

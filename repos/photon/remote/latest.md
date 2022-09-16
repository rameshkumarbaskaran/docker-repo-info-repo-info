## `photon:latest`

```console
$ docker pull photon@sha256:353688341613b5ef6e5c6bd9d0920591c35277275e023baafc78d154204f5970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:9ca372b9b5d8e0894b64eac0cdf8a718c9349d3a3538408503ca1b5a382aa2ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16076858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40036699405bcb9f44fe91436b576fce41bcfacc0a563cce27a772e4c3bacff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Sep 2022 23:20:39 GMT
ADD file:c247be22aabfb6cad460c61116a67e6661c538771d10562a4520c2fbbfc8362a in / 
# Fri, 16 Sep 2022 23:20:40 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20220916
# Fri, 16 Sep 2022 23:20:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5a1796fd7014df64ee60d6e2f3769bb55d4e2fbaca0f699d1c429f92fc835622`  
		Last Modified: Fri, 16 Sep 2022 23:21:03 GMT  
		Size: 16.1 MB (16076858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:9dbc860f55995da9a8e41ef3dcf420dd5c1499e8add1a041a3b8dc62941373ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15149038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4631120d176b57eae415bf4a00ecde555a1d5cd0ba03005cd9ff0263579a3a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Sep 2022 22:40:29 GMT
ADD file:3236f305c75f9c03fb7d4f1ccdb762c48b781258bbb304e471323b843ed18ce1 in / 
# Fri, 16 Sep 2022 22:40:29 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20220916
# Fri, 16 Sep 2022 22:40:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a1c2ddebcf32d7b4da4ae840d070d22d3681f6ad4e18385be7bc96f399e2f15b`  
		Last Modified: Fri, 16 Sep 2022 22:40:59 GMT  
		Size: 15.1 MB (15149038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

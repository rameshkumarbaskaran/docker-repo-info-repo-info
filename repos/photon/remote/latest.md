## `photon:latest`

```console
$ docker pull photon@sha256:7fe283adc49b519c070b1c21004060083c15b1924d9e94521849b05c08271c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:5fefaed41fa0652c891b9fb3350ded9737268044fdf52d2a1d8ec1bc29ff4368
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15959186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5efd5126ed4eedebd6d49056abca659f854b8973f7a7f5aee5698fd4c0e0a582`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 01 Apr 2022 23:20:28 GMT
ADD file:7f499b572a3b5445b93cd02f5da93f849a80dbc9e125411ac31cce5e84b78125 in / 
# Fri, 01 Apr 2022 23:20:28 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20220401
# Fri, 01 Apr 2022 23:20:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a2bff079975e9a13015a183aaeb39fea88ff05416e16da52c2ed4b78af1ce705`  
		Last Modified: Fri, 01 Apr 2022 23:21:04 GMT  
		Size: 16.0 MB (15959186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:7f82380e1d5c5f55dfaeebe9b29fc9b8298fba9ecaba82b45c3dc82f0094d2c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15028040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ed7824a0f7da6f15e57a078c1422e162e2c12df5d0e3dc2c6eca3233c09b0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 01 Apr 2022 22:40:19 GMT
ADD file:8b3319c3af03d3524e880f26a50d518fef8675b5871fcf1d6e281c885ddf03bd in / 
# Fri, 01 Apr 2022 22:40:19 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20220401
# Fri, 01 Apr 2022 22:40:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a3a74df1d9825e3c6b1afe9ee89a8810582cac0f4e1100b04ca2ee53cb794510`  
		Last Modified: Fri, 01 Apr 2022 22:40:49 GMT  
		Size: 15.0 MB (15028040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

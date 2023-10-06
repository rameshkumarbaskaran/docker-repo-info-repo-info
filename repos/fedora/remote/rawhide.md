## `fedora:rawhide`

```console
$ docker pull fedora@sha256:e0b22b6b0ed96b73840ba10eb81941eb2ed84f2cff6c2390b9e4e88c1631115d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:28255be7ba7de960410e8bfe9ee0d018c70f606a05e409d6a4a285f29c3cb5fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66162627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed02b470fd915b255e38e5d25703289cafe78232b2f2f27375611177e9b512aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 14 Sep 2023 19:20:17 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Fri, 06 Oct 2023 18:23:06 GMT
ADD file:14725a00094e7844923e44bc9a521d65735e42dc7f637b641220e64201b455d1 in / 
# Fri, 06 Oct 2023 18:23:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d3d9fce78c699c1725f487e624fd3f6118ff2e188bae6e2cd237d85508b84775`  
		Last Modified: Fri, 06 Oct 2023 18:24:18 GMT  
		Size: 66.2 MB (66162627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:cc11889508c00e4723dbc117cf7574b9a7213873ed3daf386257913ed59abbf4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64762552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e6ab4b09c3bdfbc9304ac81b284053390dc11324fe1cb809fbbc9ca3886048`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 14 Sep 2023 18:40:13 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Fri, 06 Oct 2023 18:43:21 GMT
ADD file:f46bd1eb04487eba2f684b2eed887ecd8f309fa31421e14fb20dddeb6473da99 in / 
# Fri, 06 Oct 2023 18:43:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e81044b2f449c6e4ee4c44621b01b5ee146281ae89fea6cf41382a0c3466bc3`  
		Last Modified: Fri, 06 Oct 2023 18:44:23 GMT  
		Size: 64.8 MB (64762552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; ppc64le

```console
$ docker pull fedora@sha256:8add5bdbbae7dc925fdd79a358a301ba1a7dd74517c2c4d62f8c7ee4736ff780
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73069210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424f5e4ce37006e745cc9c52d5b5e453f20dc6727b4bc10ca4cd01c853bf8575`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 14 Sep 2023 19:17:58 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Fri, 06 Oct 2023 18:20:43 GMT
ADD file:15002224426c93782c8fa360bf7d6911b421df9457324bb5ac84fcfcda047fc4 in / 
# Fri, 06 Oct 2023 18:20:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:73bd41eea61f9ff8d1083bc2f2f0c6304d4df8b023517fb747dff7436f5e7b30`  
		Last Modified: Fri, 06 Oct 2023 18:22:41 GMT  
		Size: 73.1 MB (73069210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; s390x

```console
$ docker pull fedora@sha256:34e1866d3556c33e087884561b780c365ee21d883f4f62e82c5b3651215796a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67262914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e3628a36431693e3d7da08cf6a9fb1e3f58f1ff8270d87fcc238db87fa41f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 14 Sep 2023 18:43:30 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Thu, 14 Sep 2023 18:43:35 GMT
ADD file:9154590dd69568344f5c457011338507e2f3ece17e26a792786fd4f3d7383ea7 in / 
# Thu, 14 Sep 2023 18:43:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c8ff0133c1d9fd4e0996df42e6662c1f3b407093dbbc536d58ad77458c919315`  
		Last Modified: Thu, 14 Sep 2023 18:44:48 GMT  
		Size: 67.3 MB (67262914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

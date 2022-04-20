## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:a19c3a02916e68f029cc710292441ca052f72bfd4a6d241c0565f88e83dc9480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:e99c785c67deec8faf233f804f7b18d787f9f2851fc39297d0dce7e0ca5ff435
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45427687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096abacdf3e787598a4806f906f8e321342157d38343d4fd281f10e655f8968e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:57 GMT
ADD file:91c1b90dda98c0f3328e5c763b36b29831467c0a0cf52df5359551154d2e6355 in / 
# Wed, 20 Apr 2022 04:43:58 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:44:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d195d42244aab04cff1a0e88441cc5fd6954f65abf0514e85b72d7c4a631445d`  
		Last Modified: Wed, 20 Apr 2022 04:49:36 GMT  
		Size: 45.4 MB (45427461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872d25904c5d3caad43216df724674640e8d212683e520aa153dcc575450739e`  
		Last Modified: Wed, 20 Apr 2022 04:49:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8b672fb3f08c9894fca2dca74766e640f755cab5c99cad325d5c47317d36a6aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44123499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef62a95f892ba73060b932bdadb285ebc58bd8747311f88508e9655747087a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:52:02 GMT
ADD file:a302deb3de42bf0b0c92ef374751f46a79f8ea2918e158ec8a6402ca17a4e3c9 in / 
# Tue, 29 Mar 2022 00:52:03 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:52:16 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e4c20269d57718c2c71bb6ec6d7a712b2cddeae105eb89540bf43cf9b7b4ba8e`  
		Last Modified: Tue, 29 Mar 2022 01:07:37 GMT  
		Size: 44.1 MB (44123271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4e4708c48fdafe109e05e200908fe22fc85060a541b37e23e309a3ca1eb3f0`  
		Last Modified: Tue, 29 Mar 2022 01:07:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b9bef32dd514404f2a8e56313e36b20d3c83ca4f76e9626661c7dd5148afa65c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba884bdd9ec69ba1af654f45cc5ae00b7b4dd7bdc974ab76bed21aaef3dece36`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:20:08 GMT
ADD file:82cf2a47571e24e1fe3a28674406c1f33e8601d4d4a324875469e66a84891f49 in / 
# Tue, 29 Mar 2022 02:20:09 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 02:20:22 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:824a32552e1b3d7fc60d23dfc4c18c7490430bb3bf5a3b2d8351f0b68e43cb40`  
		Last Modified: Tue, 29 Mar 2022 02:36:08 GMT  
		Size: 42.2 MB (42151132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79db98e1060c96479b9dbebae9db8ee6a588e618fceb77e3b65c0e362fcae6cf`  
		Last Modified: Tue, 29 Mar 2022 02:36:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a99f13b8cb03897ae7b3f384bdf5d77d91060837326b3e956a6062d556e74af7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43212265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709ddd6fce1f7082cb9dd79471ed6d039d554ed669911e1f2f12a8c5a258b00d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:47 GMT
ADD file:6eba819e0e2efda877840d26ec82d97b5cc971ac347cfa420006e49d98af40da in / 
# Wed, 20 Apr 2022 04:29:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:29:54 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3f84d18376d0447d1292f58ace6bd0081a20c00a2682f97974e0bb2caa786dab`  
		Last Modified: Wed, 20 Apr 2022 04:37:01 GMT  
		Size: 43.2 MB (43212037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6c10697208d9361ae5b3cc2f57693c758f3cf4c64ed56e86cedf5170c57259`  
		Last Modified: Wed, 20 Apr 2022 04:37:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:bfd8997421c2d1902805e6fda5888914356aee117744a49c5ba9a1d918dcacf0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46147862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89d03d487c904a934ddd953271554dc817db1675d793523e8df8f9c76a46e5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:38 GMT
ADD file:05e88221a988a6885b305a946f9fe49ce1ea6907e20e9820ebf6e4c837070e32 in / 
# Tue, 29 Mar 2022 00:42:39 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:42:44 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:77db35bd510ef164400b38c4cf9b45fec17f35d16a8058a7cdb6d5326cee1f4a`  
		Last Modified: Tue, 29 Mar 2022 00:50:26 GMT  
		Size: 46.1 MB (46147634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dd151939d46b1ee76ecf06445f76829d6cf3808a5d4f399d1723d912c3597f`  
		Last Modified: Tue, 29 Mar 2022 00:50:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

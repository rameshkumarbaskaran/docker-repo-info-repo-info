## `debian:buster-backports`

```console
$ docker pull debian@sha256:6ced1e51527172e1acfaf961807fa0ad8fc7e281d3c48c4f8352f624c1644d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:046da921bffdf4a5eec601509d7952ebf4b8ef31b6034a66d6a675a45a55e616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50499693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0381a8125017cb0ccbdb3dfd42afd58454229575503bce4a48b5f21220b2795`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 05:22:13 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468284df22e87f37190c2061d8d1609132a76308fca1c33cfe7c9347e50cc681`  
		Last Modified: Tue, 21 Nov 2023 05:27:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b6c70e145a58d84eca06af8882f2248a355684a780c8ec0a66e58b3c03e42bf6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b2cf67cd7b10d6d8424731ab620b951dcb61b9b690137345755114d91d775c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:12 GMT
ADD file:e69e944c7b28ca650586e3fa2bcb51c4c99491167bee97c4ab32982eeab66750 in / 
# Tue, 21 Nov 2023 03:58:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 03:58:16 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:859d411365ce23ca0a7fbddedc1babff0039e814c09756ad01c59527ebe62dc8`  
		Last Modified: Tue, 21 Nov 2023 04:02:56 GMT  
		Size: 46.0 MB (45966309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db21155347660f4290e33e6572b395c7f099c20f9cff08a9e238a7284db2eb`  
		Last Modified: Tue, 21 Nov 2023 04:03:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5cd0f773316bbf970a5926b8da98b72500d714a70a644bb5c11f32807a79e5cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5117898925d196031ca65736e6ae3d373130f7f334cb48be46509b402bba88c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:02 GMT
ADD file:e3f63671dca138b2b525b60f1471241941cdf4dab7f0c17cd91124978716bd93 in / 
# Wed, 01 Nov 2023 00:40:02 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:40:04 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d3db7215fb502c5873a81db7c6fd3214f199f6a1d8034da9d90918ac3220b20b`  
		Last Modified: Wed, 01 Nov 2023 00:44:04 GMT  
		Size: 49.3 MB (49291092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f888bb91f7b575111d8bd9e0ca7dfb2d781fbf84d4e0c6787e9b3021e3bea51`  
		Last Modified: Wed, 01 Nov 2023 00:44:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:4b77606913bc1d33e3a0f2ee23e2419caee3ad7b4c79d5856bbecb219fa9f10c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51256355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50ff3451597f834cfd122eda9ac1420ee89bb2f5f1abd908fef44a817b14f9f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:40:26 GMT
ADD file:3a91c3eed04829ed9d8801ae9da9d5dfb67139d59f8b98f87943131fc8953b49 in / 
# Tue, 21 Nov 2023 04:40:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:40:30 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d9ff368d73b50f922dcf47b179053552ad7a9257e80ae0ef12ba15c8ca86eb6f`  
		Last Modified: Tue, 21 Nov 2023 04:45:46 GMT  
		Size: 51.3 MB (51256132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4783eae5f635ec321510fb6e0fccf89335526bee7a495767433b744aa225b2fe`  
		Last Modified: Tue, 21 Nov 2023 04:45:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

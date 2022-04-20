## `debian:stretch-backports`

```console
$ docker pull debian@sha256:0eba6fefe70319824c9c505dbe796e550d6b41f76e4d46c172fd916615010153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:a0415b442feac68daa84c8593f6b8cde23d8ecade4ef46ccc8a3786a12cf8b90
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45427658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33386c6b36009d7d27bfe0879f50041853630fd16c3f454848232b8ae31eed03`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:45:14 GMT
ADD file:6ed691b65385dede44a92f9de9e1428af431197c66461aa0f9c61e2f7c8bade5 in / 
# Wed, 20 Apr 2022 04:45:15 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:45:18 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f5196cdf25181bc7e4411865a2e002932b7b6b0ffce787c04c1bdeaf1f204f20`  
		Last Modified: Wed, 20 Apr 2022 04:52:01 GMT  
		Size: 45.4 MB (45427434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2394e6d00af092ff7367c7fb33292903653e6cf6aabe32479e312a38bb0cb5b`  
		Last Modified: Wed, 20 Apr 2022 04:52:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:37a8411b446d12d110918e96391ed07b36aabf0edec7bb132ea9d77ad181a2bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44122895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a67b0b313d69591facedfcacb81e41c77531f53965b82e865f19f66001e835`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:22:06 GMT
ADD file:407e28120c3ae0a1012433a9787cf812e0ecc360e63ace9fe21f6728470b4db1 in / 
# Wed, 20 Apr 2022 07:22:07 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 07:22:21 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c6849d3c2fa1fe7c2c78db1c26ca92e44c119dd3e92d93450115c927ecb6dce6`  
		Last Modified: Wed, 20 Apr 2022 07:39:41 GMT  
		Size: 44.1 MB (44122673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98248ff0db11472ad62001823042f2e1f5bdeac0e6a484c74ce326e5ecc0eaba`  
		Last Modified: Wed, 20 Apr 2022 07:39:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:33b55d1d0f6c1b9d2566d7e56ee4eca8fca4b0e8873741e3f1f1dff6bbee39ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d2abf4bc3ffb9bdb1111c27de0e4c1eedb0907b98aeed3cc0ffefd8e0c01d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 13:33:15 GMT
ADD file:d237e5cd139706988e7bbc50ae542898a9b1fa1539f00322f21a71714975ccd8 in / 
# Wed, 20 Apr 2022 13:33:16 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 13:33:30 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ef9cca547ca93783f3168dc26ce42494066c74a8d5b51e766ac90a3fb5ad2931`  
		Last Modified: Wed, 20 Apr 2022 13:50:30 GMT  
		Size: 42.2 MB (42150830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdd579cc812b935db1a3ce31f9118e0bd97271509943e6f218a1f896a17f84c`  
		Last Modified: Wed, 20 Apr 2022 13:50:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:69b33411284e960871a5c65303ac7002e770fd086c9d102c39b0759509cc5c74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43212238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3af33a0b58fbfa12ec25670dea899cd58d4023aceb7c58b142ae38b7f2612bb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:31:19 GMT
ADD file:73f1db8536438ca891f4b507a569e6c561364db0f05914ebea9d3fa97e1bf837 in / 
# Wed, 20 Apr 2022 04:31:20 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:31:26 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a41fbedfa4b1547a2b4fea33de48af745d66a94741d3cf344cb2766f0e80211b`  
		Last Modified: Wed, 20 Apr 2022 04:39:38 GMT  
		Size: 43.2 MB (43212018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b96a53eb3beb1d44463d8aff37df806ccd9366541010ca13c54f965cf0267e3`  
		Last Modified: Wed, 20 Apr 2022 04:39:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:8e4e2bfd809ff66a5d33f6a8f356c4889968e30ee4f0f52a5029b62060db9945
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46147950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f444c2a94f9431981aee1e2ed6b26aa68aed33aaa74258ea84a735bf6905799b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:39:57 GMT
ADD file:e8c6a60834ed931ccc3c93b1f2c9b9ca2bf190b0d8d2474382ee8e96a7e35b5a in / 
# Wed, 20 Apr 2022 07:39:57 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 07:40:04 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cd343d4c0c2fbc67ddea33155621bdf36074fc30ffb6f917e716fbb81645f79a`  
		Last Modified: Wed, 20 Apr 2022 07:48:48 GMT  
		Size: 46.1 MB (46147730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4a0a39c21cf6cf5a561cede12d53c959a96644267af6576c061c575c761786`  
		Last Modified: Wed, 20 Apr 2022 07:49:05 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

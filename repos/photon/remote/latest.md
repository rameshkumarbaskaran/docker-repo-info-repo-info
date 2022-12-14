## `photon:latest`

```console
$ docker pull photon@sha256:91062d825c984e83c8e8745659b0a3f41a884ac3b256fa3142998b0557fb2a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:32628b89770b67191575296ff47701ba5e9b94be1e5f258c771009e2d25c0224
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16076618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0837361a584534cf10e475808159524644d91f80bf0f827cb28624d51df643`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Dec 2022 20:56:58 GMT
ADD file:0d7f338c9f1551ccf03e17676c03e83c8783e41aa2c16c11e2f7fec858538820 in / 
# Mon, 12 Dec 2022 20:56:58 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20221210
# Mon, 12 Dec 2022 20:56:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1871d44f4cdb0a7806230cace283823dd4e50d38e704264cd5ba225566cf188a`  
		Last Modified: Mon, 12 Dec 2022 20:57:16 GMT  
		Size: 16.1 MB (16076618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:28c75fdabac46783b20bada115bf5700a3b3c8614bad09b3e4d0d58c63275c66
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15161644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab105184d60b483771793182f384e1a7bdd90da93373c7887cc4af983d7ad573`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Dec 2022 20:02:19 GMT
ADD file:dceb5df380dc856fa8bb9d41887f4a68a268b443f999c795ff7a78cc9c7ed16d in / 
# Mon, 12 Dec 2022 20:02:19 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20221210
# Mon, 12 Dec 2022 20:02:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7a8a5a54091bef27b1923abf4d125bea3b6f5454d19ec213255f40c663003b03`  
		Last Modified: Mon, 12 Dec 2022 20:02:35 GMT  
		Size: 15.2 MB (15161644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

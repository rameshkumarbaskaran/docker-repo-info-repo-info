## `photon:latest`

```console
$ docker pull photon@sha256:7653a56cfcc56f18bc23d346e0807c40f841b2782d0e130c67c85d9ad978e765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:7459efd55a013aabdeffb153619c4f19b994639763f26f401d83f35d19ca3136
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15682521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1780c4734e93ba6f89950eb220443879e3ff8b1b8ad958fb2225d70b8fc85a0c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Dec 2020 00:22:51 GMT
ADD file:8173bdd255c197d714cb2e809a8fdf12e10dc98e38830cc1a89f5ba5a373fdc0 in / 
# Tue, 15 Dec 2020 00:22:51 GMT
LABEL name=Photon OS x86_64/3.0 Base Image vendor=VMware build-date=20201212
# Tue, 15 Dec 2020 00:22:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19902d7136445232da9e006dd42b71f6af3fcc33b2e9daa3b51feb645ee2d4a1`  
		Last Modified: Tue, 15 Dec 2020 00:23:38 GMT  
		Size: 15.7 MB (15682521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:94d30544341b81a0cddee5a4cf0a424ec5666d12048f55dc5817391a793ae7a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13442755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9dc8fc35f26c9a5861584e6a0d0f910e61d21870cf6dc63cfd6cc40dbc596`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 05 Dec 2020 00:45:06 GMT
ADD file:d0701a9cdcf43406b66c4e78da0ed0cd52065774929569b419ac5ba9b24ff62b in / 
# Sat, 05 Dec 2020 00:45:09 GMT
LABEL name=Photon OS aarch64/3.0 Base Image vendor=VMware build-date=20201204
# Sat, 05 Dec 2020 00:45:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bc83a45a7e576e4ed69adfe55cc308d3b01ac3c0bb8f6a239ffa1034cb8bef68`  
		Last Modified: Sat, 05 Dec 2020 00:45:28 GMT  
		Size: 13.4 MB (13442755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

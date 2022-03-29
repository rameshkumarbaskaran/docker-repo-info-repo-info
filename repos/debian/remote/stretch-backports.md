## `debian:stretch-backports`

```console
$ docker pull debian@sha256:d6fafeca5fad79ae808a584d706e7fad424a1e6a25f3af6e5d47358762adb571
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
$ docker pull debian@sha256:fe39c99586ce16a6f9f78160f8dd8e75cf35492b75455140dfb37cf6094a2493
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45427689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d506ad4b3c5f53fcd1d554f74dd46a38cd21704789434d7e82c076e8ea2127`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:24:07 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2bb0158d3ee00ea1e885d633496adcfd221f926fdef103516b63d10ee9390d`  
		Last Modified: Tue, 29 Mar 2022 00:30:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:3ac887044d60461d9796fb5297371e5c04b58d68231748c06c607bc4332f630c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44123531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1ee55acac5ec0a94a8a9a6becc3e9d7fdc1a36dcbd10d6eaa60b5bdc6342d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:55:32 GMT
ADD file:4e79cc43996ddc8062073aea4d6352c3ca3c736e9b09f1eb440f913d5a52469d in / 
# Tue, 29 Mar 2022 00:55:33 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:55:47 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a58c023b263eaa1973763831b149ed127bbe67ee8cae67d60e261db1e9d54b63`  
		Last Modified: Tue, 29 Mar 2022 01:12:11 GMT  
		Size: 44.1 MB (44123307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814bd6241600ebb6c585964f8f8feba7c0b5eba7f6cc8d5ff74846f474ad0443`  
		Last Modified: Tue, 29 Mar 2022 01:12:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b836037bbe6273f7604476661e17c884f34eaba3d24f2548f3f1ee31e8220de5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2672b97c86dde7d1c145d21738331e4c0b8eeef42a3a7dd8eadad7ec027e9e6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:25 GMT
ADD file:e869f7223f16639eccabff7b2c6a85a7e6b075d0933c31f2fecae79c1c26d5be in / 
# Thu, 17 Mar 2022 09:36:26 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:36:41 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a9f775cd9058b832779f6c0dd1ca0fbb1417961dd87ca3ba6200f41aa283371b`  
		Last Modified: Thu, 17 Mar 2022 09:53:00 GMT  
		Size: 42.2 MB (42151366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a4f50fa21ed8ac33825db2c69b90d91091109fd342607f79da6a286b909507`  
		Last Modified: Thu, 17 Mar 2022 09:53:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7e34222f0825be9b99746ea6366893cb67256a5cb7ca435de1955bd0ad712f9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43213059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02be523fec8e38d30911a96ad0e9e014a3a9820d1a01f2a110ac2f48ab6a52fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:21 GMT
ADD file:cfa91852b5b893603b656848cb1329c06041fea5cfef841978456c7266e6ac11 in / 
# Tue, 29 Mar 2022 00:45:22 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:45:29 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0b62b1ed6f218f82ac797884bd7a8c5dcdcdd8d003f3946678c53900cc537d7b`  
		Last Modified: Tue, 29 Mar 2022 00:53:52 GMT  
		Size: 43.2 MB (43212837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c931972aba0204832bcf1603bb67d3ab719071586ab51b6466a54aea17d75784`  
		Last Modified: Tue, 29 Mar 2022 00:54:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:68c2200879fa3219316478716a6219c0fd0d649a67c9d89574a474ca5a559fbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46147797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e56816e74dfe3762593bdf5afe26e464edd16b6dd4d41a6b349460aa5267ffb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:44:09 GMT
ADD file:74aa6d4005ba30e0fb6af0b75158bccd03c55e837be6f73f1c2929f62028a19d in / 
# Tue, 29 Mar 2022 00:44:10 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:44:17 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d8b8952dbc41a74d8004d044b352e7f612041bf00ab66401180cd3af79d35a14`  
		Last Modified: Tue, 29 Mar 2022 00:53:10 GMT  
		Size: 46.1 MB (46147573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7427b74f0a0807f4fdeeb783712fd33e5d9452b1937dff7df4aaed3dcea1f41d`  
		Last Modified: Tue, 29 Mar 2022 00:53:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

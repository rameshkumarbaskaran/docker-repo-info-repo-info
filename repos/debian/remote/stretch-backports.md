## `debian:stretch-backports`

```console
$ docker pull debian@sha256:349f229d693a023083a3b1c83edc21e11bc4695ad8345c42b9500c5ea18b6b1b
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
$ docker pull debian@sha256:b381ccc9cd3b0a12e13a95c0930e9185b9a0e3138bb8c85c75711a7f70dd9bfb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013e9658675a4d7dfcebd7098f9c22921e461692fcd1277f5daeba8c284765bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:23:57 GMT
ADD file:3dc1697adfcf63a288e9ec7a2c40438b8ba2ccfff0382a1ed5457f30d7a37f76 in / 
# Tue, 29 Mar 2022 02:23:57 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 02:24:12 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aecfa9e0b0179abf68bebbcfc35453928546e01ad1c8b6eaadf759360762dada`  
		Last Modified: Tue, 29 Mar 2022 02:40:33 GMT  
		Size: 42.2 MB (42151158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb87be6f1130e26d8508411eaac526000f4d19c1c67d19f897a41728962eba6c`  
		Last Modified: Tue, 29 Mar 2022 02:40:52 GMT  
		Size: 221.0 B  
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

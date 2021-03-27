## `debian:testing-backports`

```console
$ docker pull debian@sha256:c8ac2f0e1786b7991698e51aa7b914242fa2f869167a3d7ed08bcad726b5acd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:2661b1009b6a1ebcd92af4580e1e6ab02b89d0c3f483d53b6f5feb209919b292
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54868191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a962ae984a7d15199bb061d1e91a4f7c545e3fb2e97bebda7ef7827888573f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:43 GMT
ADD file:a4b7b44aa4993fa36515637472fa83cb54bbeab639f7985d05e93dd9d6aed152 in / 
# Fri, 26 Mar 2021 15:23:44 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:23:48 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c4a4a1171d4508c7745e3647d21fd2935ba3f534b82463998726686b6c5a87c9`  
		Last Modified: Fri, 26 Mar 2021 15:33:19 GMT  
		Size: 54.9 MB (54867970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314299226b372ae6745eebfdccbad7f4ddbfd9d46a52e2731e98f0b023d68dfc`  
		Last Modified: Fri, 26 Mar 2021 15:33:30 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:fd00499e7e74bf7ba64568b00f3e5594e1d415753952953dfc6df8f07bc12862
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52404639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a73d443b535fad1b132866f9e47f8ff97a1489318d88d3987526ab9af25d5e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 07:56:26 GMT
ADD file:1f0d51940060ad5be8305835a634d086ebd15deb3ed300c73daf68f5d1a76c55 in / 
# Fri, 26 Mar 2021 07:56:29 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 07:56:39 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e958077b175ca4c4330a7ec87a9f51fb1a7222a2c0693c69b34198734ec69bb2`  
		Last Modified: Fri, 26 Mar 2021 08:05:01 GMT  
		Size: 52.4 MB (52404415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab611f0599083736c1aebe57156b717f1a597f7b3b948dfcf65560c6fbb1ccfd`  
		Last Modified: Fri, 26 Mar 2021 08:05:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5a40ce3f64368446944d4b277a64b84b36673f6123d3c8995b5ababd51eaf44e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50074276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586fad6099761261f2f81b996ac44ee7ba9ac6fc0719cbd9af9069abb8fcda0c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 11:23:10 GMT
ADD file:699c64d1733568708c6338c1f05e47fc3750ff3d0153193cdf9a6362a9595b80 in / 
# Fri, 26 Mar 2021 11:23:14 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 11:23:25 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2510c5d7e5afd3b6e15d9a3ca9fd39cb9ed6aaeb830a99e794bf0ea2784f40c1`  
		Last Modified: Fri, 26 Mar 2021 11:31:59 GMT  
		Size: 50.1 MB (50074052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06ae4cab0e3808005ca82c523ac7cbb02023bcea196297e074fc8b42f561c7b`  
		Last Modified: Fri, 26 Mar 2021 11:32:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5d614f2ce38589e5a1def9f7fe1f5fda7da90beb36f9c8cfbb6d53ee640874ee
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53555420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5873ac7d0c77e9b4bfcae148f2780afc506b89101e62842e258b3c4ed0f0e29`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:45:01 GMT
ADD file:d45466eb69a99fd89d27c9750221cf0d64aa48068b953172605728544c7b519c in / 
# Fri, 26 Mar 2021 15:45:03 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:45:12 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1a9712791592c9691e0f6ee9c25c4259d1bd1ad5b9b71e0ae0e4d87aea547b03`  
		Last Modified: Fri, 26 Mar 2021 15:51:48 GMT  
		Size: 53.6 MB (53555196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29658ef46013da2b45850ae82a7adebce07bbcd46add099431a9a5c3a0a088e9`  
		Last Modified: Fri, 26 Mar 2021 15:51:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:3c88e41c5f1fb28969794bbcbcb83ea678b2ce2ba0ed33fb7f9a0777ffefcc6e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55881442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f63fe3bf03cb19eef25509a17f096625cb69ac82f00e4fcd27b4a0ede2982f7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 13:56:32 GMT
ADD file:f008fd33a3d40eba43eba5b598da09f396937ff11cc88c363e7408c78887a1aa in / 
# Fri, 26 Mar 2021 13:56:33 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:56:39 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:07b527df1f295aaec4c672cde973fdc525bf2f45076176ab891c0dd1314f9342`  
		Last Modified: Fri, 26 Mar 2021 14:07:34 GMT  
		Size: 55.9 MB (55881221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7ed090cc8231e20b59d9e11cad1e4f329e543f060d9575ba4f7344cc372345`  
		Last Modified: Fri, 26 Mar 2021 14:07:48 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:3ac39b801c23f324f12377acebd73a690aa85e0da360d329a325f5001693d472
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53128960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a575bbda06efa3127281f374b79ee0251fdfb2524018a54364c3477b3553dd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 08:11:55 GMT
ADD file:0ddc16d08c0ed8a6219e588e991a0d1456d4950b56aca1e0c650a26f238a2d00 in / 
# Fri, 26 Mar 2021 08:11:56 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 08:12:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9a58b4ed9116dc08cc6097c9827ee4d787d33e545d84c04ab503c3b1a81aabca`  
		Last Modified: Fri, 26 Mar 2021 08:19:56 GMT  
		Size: 53.1 MB (53128736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f479319c37889eb723ba8009d88d1118aed034343f70c5b50484a7df363724c5`  
		Last Modified: Fri, 26 Mar 2021 08:20:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2e0473119d110121f106a87c78bd784467c811b620d456d79703119155c57df1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58756831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e34602d8ccc4cc9cb795ebf7a13f6bf56ed6c52b3b6d9396de614b5c208257`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:16:50 GMT
ADD file:ac75303d8f14c20c653b4ce5110dd5a0869e55637165dd1fa4e141c7a1116e7f in / 
# Fri, 26 Mar 2021 15:16:59 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:17:24 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3c92ba3a187356376a2f36827325802fd75e1d91254fe3a9f4482897868b52c4`  
		Last Modified: Fri, 26 Mar 2021 15:24:10 GMT  
		Size: 58.8 MB (58756606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af9cc63306132f4e504437b89f3d3cc9f4b069e18deacd6c1c157cd6c3b039`  
		Last Modified: Fri, 26 Mar 2021 15:24:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:ef418b88caebd9fba6a99c5be72a43ce984e9b0b3e3bc40827b355c65723ce99
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53147853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd12d1453cc81b692b0b83b449e1d464ca139244ed2674a88f14b4af4bc3c168`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 10:55:05 GMT
ADD file:c68277f5942da894b87824e7be5e490cdc087530373096bc568a709716c8bd7b in / 
# Fri, 26 Mar 2021 10:55:10 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 10:55:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d49851850d45c1c8e424bfcbe79b41751f17923fe040a5364ea54e2ebe4dcbda`  
		Last Modified: Fri, 26 Mar 2021 10:58:54 GMT  
		Size: 53.1 MB (53147632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e644edbc0b49753ba4944783fed6dfa6a208456a4dcf3ea44f75bd6fbd278e`  
		Last Modified: Fri, 26 Mar 2021 10:59:03 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

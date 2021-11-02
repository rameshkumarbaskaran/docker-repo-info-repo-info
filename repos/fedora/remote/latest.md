## `fedora:latest`

```console
$ docker pull fedora@sha256:0792877176bded80ee762763f2a15a84e837486cd98adb9f593d3900a85eb45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:db8380e69336e37a94bacad856abfde03cd7060f53530be1c7de32526b00dfd0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54779887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b080de8a4da3da9ec2fdbeeb6d70d94079b27df87483039fc45abd2152109c43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 01 Oct 2021 23:02:34 GMT
ENV DISTTAG=f35container FGC=f35 FBR=f35
# Tue, 02 Nov 2021 21:29:21 GMT
ADD file:be45b9d0e66aaff43304ea2300127b0027e748b263fa26d203cd7012eddf7d19 in / 
# Tue, 02 Nov 2021 21:29:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fc811dadee2400b171b0e1eed1d973c4aa9459c6f81c77ce11c014a6104ae005`  
		Last Modified: Tue, 02 Nov 2021 21:30:16 GMT  
		Size: 54.8 MB (54779887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm variant v7

```console
$ docker pull fedora@sha256:8176a9d5562c98878b0a7c7b0d934ae350717658f3a4e655eef192aef326206c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61384186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f375ae7e82107064885042ba787adfcea1d83e2035ef6cb37a0c1f59c044d033`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 19:03:21 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 23 Jul 2021 19:04:30 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Sat, 02 Oct 2021 18:48:58 GMT
ADD file:9afffa9d8bd779bee31656a671c7e44de8bf2c2fa429d40745ceaa4067a33323 in / 
# Sat, 02 Oct 2021 18:49:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c74e150d4dd7327b2cf114c5d43af9fd9d12cec1a4b0dbba528a0895854ea92a`  
		Last Modified: Sat, 02 Oct 2021 18:52:26 GMT  
		Size: 61.4 MB (61384186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:eb6934c99216962a8860abc8cc38a5dbe26a3a823ca6a646886d02bbb7c90252
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53779450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f7c65055e723f9afeff807f84236a391f9451c2957bb960e79704fbb70b0e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Nov 2021 21:12:33 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 02 Nov 2021 21:12:58 GMT
ENV DISTTAG=f35container FGC=f35 FBR=f35
# Tue, 02 Nov 2021 21:13:02 GMT
ADD file:f692703c83a7a1b73f3b8481470a706e384ae7e385652a5ffbe604b338f1255a in / 
# Tue, 02 Nov 2021 21:13:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:55bbeef7e282fa3909a3d777b6c2bd2c965627de4d537994838627d5508ea328`  
		Last Modified: Tue, 02 Nov 2021 21:14:16 GMT  
		Size: 53.8 MB (53779450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:e27fe4cb4e5d90526b316a985d48aee2961105866639cad42893c0da0aeebb26
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70780433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3982491d60019f711b0974d8faf004c29e2a5f2b5d22d1ec91c404f3e6d0b134`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 23:32:50 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 23 Jul 2021 23:34:39 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Mon, 04 Oct 2021 19:39:42 GMT
ADD file:8904d4d3e05d9809a176a0fe99afcfa0d13d112f68f3910e988d94d0144cd063 in / 
# Mon, 04 Oct 2021 19:39:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:13aba4eb2f927ef62d712297e57579ef9d29c8c223ce9d1a4bf5887a44e40ce9`  
		Last Modified: Mon, 04 Oct 2021 19:42:16 GMT  
		Size: 70.8 MB (70780433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:6d0c2a9d93b142fc01b21e21af644be95b7e6bb5cc0ccbb0382de787e99a26b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52727110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b4a9b57271af591022ae0dd8f97e3d68a2d61c89f28a5c9a0d9395c3332033`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 01 Oct 2021 22:42:23 GMT
ENV DISTTAG=f35container FGC=f35 FBR=f35
# Tue, 02 Nov 2021 21:28:36 GMT
ADD file:21c28fd1d13df6b1e0bb57f883f8351c467ea20e05e8d36d1cc046173040c3ce in / 
# Tue, 02 Nov 2021 21:28:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ff0313afc065432177e40ce9e640fb0ded68d6be98fdd233a8cec88e2b42b69`  
		Last Modified: Tue, 02 Nov 2021 21:30:06 GMT  
		Size: 52.7 MB (52727110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

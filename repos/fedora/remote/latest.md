## `fedora:latest`

```console
$ docker pull fedora@sha256:767f042cc33740d0f7e5bfdd5d2d183380fd3cac69da308b3554a9e9f64119a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:553345aafebc934b16998202b0fdbd4cbd37c59afe83901997ff82ba8c86d924
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68440765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9fae4fa405599ad15fed7742310e91f34593a5a8d2da4c9ffe67107385e729`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 20:41:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Fri, 04 Aug 2023 18:22:55 GMT
ADD file:0ab93a3201ace45c039c7e7bad9808c9010f7a67de777fac6f141c98c9bbf73c in / 
# Fri, 04 Aug 2023 18:22:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:deb9cd9f829fea30353f8c711013769a0cacbfa6963532841501df300f8f54e6`  
		Last Modified: Fri, 04 Aug 2023 18:23:42 GMT  
		Size: 68.4 MB (68440765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:99f96b7b103c71d35b63c39bae15e93085988de8eb155ec9e22f6b5f670faaf8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67189372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f838063d816c428b612b4e599ea70d35d87ef6335d0a5bf98b9043bff3528dd6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:41 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Fri, 04 Aug 2023 18:41:08 GMT
ADD file:50785841137152691ca6dd92200a0457ea325f9f4aa41c79dec9b254878dd456 in / 
# Fri, 04 Aug 2023 18:41:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9523322a2d97b6a26a31c5c19b62d9ec9e3ea7e7ed808d90b225b9c6081ffb13`  
		Last Modified: Fri, 04 Aug 2023 18:41:48 GMT  
		Size: 67.2 MB (67189372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:1f187539f6dd8eddd9c335fe348b3a9ba25a9a0fd56838a101fe72400d9d4a09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75331160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77075937312f65bdf3894721b5c8241b264d08029b8231f93a307e0e15dd9596`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:19:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Wed, 05 Jul 2023 23:09:56 GMT
ADD file:d669b50dc1a5c7cf655afeb6f64678dd391443c470908f8adb678c82da2f01bd in / 
# Wed, 05 Jul 2023 23:10:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c51ad525f5c28bbc3af2f1cc68b9d1770e170df34ba94c0c62abb5d3b90aba7c`  
		Last Modified: Wed, 05 Jul 2023 23:11:25 GMT  
		Size: 75.3 MB (75331160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:db34d8f6f47716a92e6ad27725c035b75a9cabafdf85994e29c5461080fda021
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69054480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ddc7a451e28d1bf1502dd667da44807291659e9e2806709055a2518d9e067a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:31:13 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Fri, 04 Aug 2023 18:43:42 GMT
ADD file:5b3c686df8f54e57e343feaaa7f2bd093be7fdf31a04a0dd53132f2edd5bfb2f in / 
# Fri, 04 Aug 2023 18:43:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e74c489c75361c4e589ca861c1f7eda09012d60edc1b0f3ff884b7eac2ee52e1`  
		Last Modified: Fri, 04 Aug 2023 18:44:55 GMT  
		Size: 69.1 MB (69054480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

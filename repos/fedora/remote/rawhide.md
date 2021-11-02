## `fedora:rawhide`

```console
$ docker pull fedora@sha256:2a36ecc9a73d6a4df100b2a50a58e4839b5f85bfc9faed32e1e99c0a8a17c4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:f7bb300bcb576e73dde5a246d2b19526d43960d1f7eb47c73417a240b7ed35bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57706756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf0d0c364a631bc7dd12c8a1f59d01e4ccca6ffece5bd504e1567d057de92e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:00:32 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Tue, 02 Nov 2021 21:29:33 GMT
ADD file:acf26dfcac681503f9e26a37bb5b068a4759dc0ab17b5f1050593f335314fe36 in / 
# Tue, 02 Nov 2021 21:29:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a029976c022b471b42be8f08d0335b0464dcd02cac8f67209c40ac6e341ab301`  
		Last Modified: Tue, 02 Nov 2021 21:30:34 GMT  
		Size: 57.7 MB (57706756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; arm variant v7

```console
$ docker pull fedora@sha256:63450b59abcc6b1b08ab1d38c8428d0db56e6b878a95b96d1265785be98a3f4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54138322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130b21afbea8f95a746f5b3e72b110b2514641b4e1a7290743b72e9677fa9473`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 19:03:21 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 23 Jul 2021 19:05:03 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Sat, 02 Oct 2021 18:50:12 GMT
ADD file:4ab115b4445fa29e9e0f5737fe7c7fe476c35aa2d78cbcb0daa40dd62803cff0 in / 
# Sat, 02 Oct 2021 18:50:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9043e86b4c69f46f140bb2fdb903794f727c3d8e335fc2c2693f20e3cb8ef9d4`  
		Last Modified: Sat, 02 Oct 2021 18:53:56 GMT  
		Size: 54.1 MB (54138322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:e68bc50be57ad40bdea883ab3258ef54d31db8f040f566fb94d7c33b2dbbdbee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56500761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f231a68ffe80ee9627d48fd6d094a60ecce03b963e8e8e913b1a8232820a0c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Nov 2021 21:12:33 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 02 Nov 2021 21:13:09 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Tue, 02 Nov 2021 21:13:13 GMT
ADD file:604e2ef3b8dc32d11da1cea3535b660bc595a1edb5f2c1086044bad452f95173 in / 
# Tue, 02 Nov 2021 21:13:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:761f7e0d8b44b3ccf888adc5f0c06915c28cd89cfd49738aa57bd74c6b80fca4`  
		Last Modified: Tue, 02 Nov 2021 21:14:36 GMT  
		Size: 56.5 MB (56500761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; ppc64le

```console
$ docker pull fedora@sha256:6e7d1d2cfe3b4f80cca502cba88ff3090c5225553c77894dd42a2f0b4d24b822
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63154149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c68f089f9dbffcd8e963ff6c93159860a1b761b4155ee72495dc8986ce3fac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 23:32:50 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 04 Oct 2021 19:40:57 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Mon, 04 Oct 2021 19:41:06 GMT
ADD file:e13755d3f7d03069ba475b871a56f81a4103aa7112e7800ea94503aa313627c6 in / 
# Mon, 04 Oct 2021 19:41:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e80a53b3ac3ce9e11936314ad5adb9836a6ac578515907889435610d87804435`  
		Last Modified: Mon, 04 Oct 2021 19:43:10 GMT  
		Size: 63.2 MB (63154149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; s390x

```console
$ docker pull fedora@sha256:afafc77b4632c6750bfffaa099fc8e753b2a38e0496922956e13020cd937203e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55158170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4825a88388dd83c71d7ebe46b8bbcd412d59c160072145869ca74f23541b3a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 01 Oct 2021 22:42:38 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Tue, 02 Nov 2021 21:29:08 GMT
ADD file:8a77a81970b6a702c1b54fad57fad996bfa087b741913c5e6497f56f8e4189cb in / 
# Tue, 02 Nov 2021 21:29:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e90ab5cf9c8733234d970ca9a967d31286943996a9eb293f507785641cc7e149`  
		Last Modified: Tue, 02 Nov 2021 21:30:21 GMT  
		Size: 55.2 MB (55158170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

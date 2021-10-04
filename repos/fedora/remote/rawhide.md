## `fedora:rawhide`

```console
$ docker pull fedora@sha256:a861144bb13f81da7b0e9930c3343565f568abba6ca72d8ce2e099e35a3c48e2
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
$ docker pull fedora@sha256:d9118d70df6443c07f616b82e210567f4c16c5a806e43d2bddf2a1338115ba91
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57968283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b3bee862521dae2253de5e8ef46df10a3370dffa895a8305681fbbfe1a73c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:00:32 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Fri, 01 Oct 2021 23:02:57 GMT
ADD file:66e7def7f748f55d28240be7c22b6a5091881f220bac3f3fa6fb4150b72a21b3 in / 
# Fri, 01 Oct 2021 23:02:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:97458595fadc70d8375d262570f72aa345abb37d2ad63b5afb3119e6bfc44a31`  
		Last Modified: Fri, 01 Oct 2021 23:04:14 GMT  
		Size: 58.0 MB (57968283 bytes)  
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
$ docker pull fedora@sha256:70a53de4846bae8e7492afe31330cf0f4fe50f8a85aa8e2ad8f34f7fbaea6f59
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56748942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d727c3aa20a79786820c4fd0e54806ab8e0510aedd8d95845f5898d39c8212b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 01:32:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 23 Jul 2021 01:33:02 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Fri, 01 Oct 2021 23:29:18 GMT
ADD file:2029c4441926eef43114b03312616846ee4080b972dc772e89de8697be718100 in / 
# Fri, 01 Oct 2021 23:29:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:de84f0857d31b2d10226dd601e6d0b7d7cd2b6f249389043b5f9955ed64c2932`  
		Last Modified: Fri, 01 Oct 2021 23:30:46 GMT  
		Size: 56.7 MB (56748942 bytes)  
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
$ docker pull fedora@sha256:6cef51bfef42d0d93eba46ac18865127688b1e7305f0f681647312a3cfe11e4e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55416957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba85dcf68634f46e2252d619cf06c8f6147a05adbe65ca4ffb686f8edb497f88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 01 Oct 2021 22:42:38 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Fri, 01 Oct 2021 22:42:42 GMT
ADD file:2ad915790ee07c5526c02c099a4e87c5b3e8a1cd9d18417cd6beb0cc92772bcc in / 
# Fri, 01 Oct 2021 22:42:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5b4411df31ea2b2120251020a572a65926d8941708d23204447c5a33c028d996`  
		Last Modified: Fri, 01 Oct 2021 22:43:52 GMT  
		Size: 55.4 MB (55416957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

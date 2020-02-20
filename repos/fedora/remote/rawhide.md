## `fedora:rawhide`

```console
$ docker pull fedora@sha256:4fa73ba4d3d1819ccdcaf27a148c906ced7d8d3532c33797224231bf2509d335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:3f3fc6a4714e44fae9147bc2b9542ac627491c13c4a3375e5066bdddc7710c9e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69686779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13031c001a8b4a574e3088e2d1ab331d72d821804ccacdd41bf5662ae02cc98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Jan 2019 21:21:55 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 26 Aug 2019 23:28:07 GMT
ENV DISTTAG=f32container FGC=f32 FBR=f32
# Fri, 27 Sep 2019 21:21:30 GMT
ADD file:4c3d1262baf371dc64c5379e1d7407ab60c861140b305969ff50ab0a04ffa56e in / 
# Fri, 27 Sep 2019 21:21:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a39edc9e7bc3a586926c94144a8c7ebc83dbfaa17c2a60f4ad56df7066cba285`  
		Last Modified: Fri, 27 Sep 2019 21:22:24 GMT  
		Size: 69.7 MB (69686779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:4c6a00a76ddb6ccba220005133228d066e6093552c6503853e46b377c43e62a6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70591724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30848d24f48f9ee4070f48dae7253274c13dfd10110db6c8b1473ddd3ebb6dbf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 22:43:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 26 Aug 2019 22:57:41 GMT
ENV DISTTAG=f32container FGC=f32 FBR=f32
# Fri, 27 Sep 2019 21:41:43 GMT
ADD file:1308c14d9a8200c2399d0c5fcea67b0cd69230b5663bea234dd95d0cf863d433 in / 
# Fri, 27 Sep 2019 21:41:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0edb1851f682f85f5c4f1e7a7078e7a4e213da14383eab26a088050390a50848`  
		Last Modified: Fri, 27 Sep 2019 21:43:12 GMT  
		Size: 70.6 MB (70591724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; ppc64le

```console
$ docker pull fedora@sha256:0b37eb2d7b555ed4c0347053ebbbadc369a84892baade26bafa326d6b7e58240
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76264241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5785245ce5ac63dbde383bc4245c9a96399f63665aa0cde879439919cb0626`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 23:19:06 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 26 Aug 2019 23:28:17 GMT
ENV DISTTAG=f32container FGC=f32 FBR=f32
# Fri, 27 Sep 2019 22:09:06 GMT
ADD file:520986e48d3dc72cfc4ace1f798e49465c64f49ddf00426d35b6deb5ee5eb399 in / 
# Fri, 27 Sep 2019 22:09:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2de1a941ab8c3ce9e47cc14c22a088d306e7241dda67898ad4b12509ac0b91af`  
		Last Modified: Fri, 27 Sep 2019 22:11:21 GMT  
		Size: 76.3 MB (76264241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; s390x

```console
$ docker pull fedora@sha256:5997a85f7c06dbf986a790ad4511656bad278648c223af53e82d5ed4bd882c31
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72705997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbdd7c8d27d276958e099b9bf9d4ed0b71d53c6828bcccad133c3a92b0738c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jan 2019 12:43:09 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 20 Feb 2020 22:44:16 GMT
ENV DISTTAG=f33-updates-candidatecontainer FGC=f33-updates-candidate FBR=f33-updates-candidate
# Thu, 20 Feb 2020 22:44:27 GMT
ADD file:87e9467469d0d383b11947cdb71a0020051c10a8ef347a7135d01d14ef837e5f in / 
# Thu, 20 Feb 2020 22:44:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:604d171b62989ec666290c68cf4fb06523c96147a631ccf4fb81dcfe5e70adfc`  
		Last Modified: Thu, 20 Feb 2020 22:45:48 GMT  
		Size: 72.7 MB (72705997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

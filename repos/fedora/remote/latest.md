## `fedora:latest`

```console
$ docker pull fedora@sha256:889a85dd5afee5883bd6c396b370ad3a600984a47809a775e20c70b9e8f9e639
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
$ docker pull fedora@sha256:455fec9590de794fbc21f61dbc7e90bf9918b58492d2a03fa269c09db47b43f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59995747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7654d129a8a25626dce55adfa5d8a419b794952229ed9542968ef7faca2ee975`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sun, 20 Mar 2022 10:46:00 GMT
ENV DISTTAG=f36container FGC=f36 FBR=f36
# Thu, 03 Nov 2022 20:40:40 GMT
ADD file:8d61743db71ec38169aae6644f4ef369766e0bece381549d7530d11df9a9a214 in / 
# Thu, 03 Nov 2022 20:40:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e437052d4f94147f80c5b03d10b6d7e034a32b1db5a9f340b2c8090cec1376f8`  
		Last Modified: Thu, 03 Nov 2022 20:41:48 GMT  
		Size: 60.0 MB (59995747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm variant v7

```console
$ docker pull fedora@sha256:ce3d46c564d9145f73d1618a605e9d959ec704d409b2afb54f3517a27c818cc6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54490837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6e76519a089477b47efb6d84e8dcbc6639cc6a12e03d575b069278e4cffa88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 20:46:50 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 20:46:50 GMT
ENV DISTTAG=f36container FGC=f36 FBR=f36
# Thu, 03 Nov 2022 20:46:56 GMT
ADD file:2a100119d250f9a75cfee4425142172c6ec02864e33737f0dd9e8330ccecce4a in / 
# Thu, 03 Nov 2022 20:46:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:af068febaa0f76501a770f13db16f57d1900b8d9c746a4ec074e4c234de151b5`  
		Last Modified: Thu, 03 Nov 2022 20:47:22 GMT  
		Size: 54.5 MB (54490837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:e25982afd0124a42b8fc8029b31919f5e349e5ef6e75e7c51f5ad6175c931890
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58073695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade8b003ba4713a478328aa7c17d60571cebd32d3b49494ba316ae1696443854`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:22 GMT
ENV DISTTAG=f36container FGC=f36 FBR=f36
# Thu, 03 Nov 2022 19:58:26 GMT
ADD file:b82910bf07012170f0d5f59e76752b39c1697ba5f4f170c1e130973bb3cfd444 in / 
# Thu, 03 Nov 2022 19:58:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:abb467b93dbf4d81a9c5342c20b37ddd6b97aac043b7d58e7add918604ce9bb4`  
		Last Modified: Thu, 03 Nov 2022 19:59:18 GMT  
		Size: 58.1 MB (58073695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:18fcfed5a4dfa97dd50f16f1c3b948f207412a96a733d86d5d58f7b3a55b2a25
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64408192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36120227f469da278a8a9b29139830fc89c35000dd4014e038b73c5349a75558`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 11 Oct 2022 12:17:27 GMT
ENV DISTTAG=f36container FGC=f36 FBR=f36
# Tue, 11 Oct 2022 12:17:37 GMT
ADD file:49028a8d924ac192e7ba103ecc4b190f85f90d3ca706aa565b0862163014b5f0 in / 
# Tue, 11 Oct 2022 12:17:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7d42e44acb9fce9d0c6bf82db95a5511c20546bb5ec6a9f2dbd451676478d237`  
		Last Modified: Thu, 12 May 2022 22:32:17 GMT  
		Size: 64.4 MB (64408192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:a4a89ebb890dae892d8ba8c241a487fa91d07a26231055b7ecda408aa1c8811c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55866395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1185b4b6acae3561cf2cb14466fa70d0290abaf7f6cfa1c61cf9d7ac427bec16`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sat, 19 Mar 2022 04:31:33 GMT
ENV DISTTAG=f36container FGC=f36 FBR=f36
# Thu, 12 May 2022 18:43:32 GMT
ADD file:e8ee7a53af42a85aab0b35476966872f3783deb8471e0a8608272329a1a4a443 in / 
# Thu, 12 May 2022 18:43:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a89d4a56299d6e7abd0e5c76dfaf3d48e4d8f9141a7e23cf6ae832aae4bad2aa`  
		Last Modified: Thu, 12 May 2022 18:44:23 GMT  
		Size: 55.9 MB (55866395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

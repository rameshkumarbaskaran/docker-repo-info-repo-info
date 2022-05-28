## `debian:stretch-backports`

```console
$ docker pull debian@sha256:9d4f8aa713ec70a51f4d7676af33c27ea819ea3d0e1ed8c52d640144663a7fea
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
$ docker pull debian@sha256:57fc99afb64bf557f291af722f6f35dd6a37bc86a1b0dda7b424ce7830f634df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45428230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f09cabe5e0be350dc1bad9eb36245d644136dc65cb38438a4cce3e7cd469c93`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:22:05 GMT
ADD file:00f57642edc8479d50e6470a3509ad679eb9353761912deade33251fb3d9daa8 in / 
# Wed, 11 May 2022 01:22:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:22:08 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:06e39e28714dba08fe310ca1aafb43905427729ecf8e9586f811a7e5062fd09b`  
		Last Modified: Wed, 11 May 2022 01:28:34 GMT  
		Size: 45.4 MB (45428005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4b733396f7f38f2e0c9fd6fc52c9bf60108d00707f614c5da12f3557c2de71`  
		Last Modified: Wed, 11 May 2022 01:28:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:fb1c1235d76db690bb01da68e0402ca5d2c1ed4d111f797b75060437b46dc8a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44123080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715afcefe509b51f1e36c84c71c4a541020ec08dadc41a8f6e96a95229aa69d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:55:33 GMT
ADD file:95b054735b431afab54d50818bab5058e711871345ec62ca3036290e76c5002c in / 
# Wed, 11 May 2022 00:55:34 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:55:49 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:342be1c547ac3ac45aaed473477b6660f99f4de775e90a96d72de9ed5e557bd3`  
		Last Modified: Wed, 11 May 2022 01:13:02 GMT  
		Size: 44.1 MB (44122855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ac31a33faf1aa82d100c86ae2e3d30c0445c941b3e76de60751dd34a71f405`  
		Last Modified: Wed, 11 May 2022 01:13:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:387a9ce9b72ec1a85f0b7de1d3f54b255b44f3ff18a35deb5f8af2d3f287371f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e5434211153bc427d178be1318418e2252a3fa02d07d50fbd248521a0cda92`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:54:33 GMT
ADD file:c679388ac7a37037465302aea3117354d9746d0c50c056e826b5c8c58aea5138 in / 
# Wed, 11 May 2022 01:54:34 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:54:49 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:629c5b996bdb9cea71f1d194d7a244d4aba271133bad4f5b88bfe38c4626349a`  
		Last Modified: Wed, 11 May 2022 02:11:17 GMT  
		Size: 42.2 MB (42151163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d056a5c8cade331b4a1c18ff0ff4ec0777b13efe734adb72558eb41b5a2c1112`  
		Last Modified: Wed, 11 May 2022 02:11:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5fc7f02950bd21fcdc3a88e7acab2306525943384a4208f8db27dfdb9fbb27a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43213095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0054cf0cb32b0c8d8bcf67c5a8ea640379c6d22a6f9217ce6691c051d88448c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:42:45 GMT
ADD file:93d675ee0bc32a88dc4d6c0872276c4678dc31f0b6eb8b936cb823f191bc07f0 in / 
# Sat, 28 May 2022 00:42:46 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:42:53 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:de7fc2a3b80bcd193de687188fc9051c8be6c61ec81fec3aeae61c079f71e69e`  
		Last Modified: Sat, 28 May 2022 00:51:21 GMT  
		Size: 43.2 MB (43212871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f8a23087310eaa4a40fcd38862b1bb74716d13e50bdc96cf59508e10d4b42e`  
		Last Modified: Sat, 28 May 2022 00:51:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:45ab1f34d75df566bdf559aee28e1ea5b0a3c7dae9a5f491d36ec230cfca0c28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46150422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0672210f2f1369953379f550b600ea341f9e4c1367281d62ae9dc43c1309086c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:50 GMT
ADD file:1a448f874e606582cb67d9369c97c83c78f2327fde8089b8cb6aaf476dc51935 in / 
# Sat, 28 May 2022 00:41:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:41:58 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:99b3b0cea6c21e2e36bc4c198a72e5aa3b3ab76d26c2c63d9b0c2b0add554135`  
		Last Modified: Sat, 28 May 2022 00:50:28 GMT  
		Size: 46.2 MB (46150199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75f8839e7ceac50b1a339bbdb13213aaa13cc24fe0d1e6e17d9cb66b86b33dd`  
		Last Modified: Sat, 28 May 2022 00:50:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

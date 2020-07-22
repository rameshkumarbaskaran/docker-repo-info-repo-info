## `debian:stretch-backports`

```console
$ docker pull debian@sha256:daad45c7009b268c7ab4fc6481827bf3ecbeaf9ecd7b4501e052edf24acca9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:1fca66477cc2ff604a72c77c6d47d994a6370e604fe8c8883e19614a6366ba6d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45376018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fe1cff75f28ce6ff6162ff67edbd0ba6157eab046fa7d6f9ae12d0cc5f9833`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:20 GMT
ADD file:6e16bc9cf28c19a1fb1fb516411643e33cbd2bdb7b6c2ce2468c6583c89871a2 in / 
# Tue, 09 Jun 2020 01:23:21 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:23:25 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:81fc1918191541a2ffb6ed1cd8386ef8302aea1b0613ebc768a00e76c1f34bb9`  
		Last Modified: Tue, 09 Jun 2020 01:27:59 GMT  
		Size: 45.4 MB (45375796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd1efce3db5d73c639a3577bca09a8ba1781dba317a286aa1f5a5651c64c94`  
		Last Modified: Tue, 09 Jun 2020 01:28:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:49e535bae3ade588b4c138a6fc8a135bc7543731b4758c4da03064c9257e2313
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44069499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b23df45d787bedf52ee81fe3dcd91e8a367d5b93d952fe97281bae5e4229831`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 00:55:26 GMT
ADD file:f75089c5817628b287da52c6067110dff0b6f4efb6fecf5feafa8e2daea1fecf in / 
# Tue, 09 Jun 2020 00:55:29 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 00:55:37 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cc933a187a21289c01459e983ea69dee29bfb61a3aa7a3a8ae010865977afb50`  
		Last Modified: Tue, 09 Jun 2020 01:02:51 GMT  
		Size: 44.1 MB (44069276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5faec6622fb6ed9204d9ba5df96893b897cbe50ba5ad326f99fde28a3beb79e`  
		Last Modified: Tue, 09 Jun 2020 01:02:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:3151570ca84904b427fd1bb9cc6cf266cf916e7d0fd5d6e1604388b59580dd50
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42102726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03cea6b21ae1538e72068da31a7a29c1de3fef4a92a9376b6f2677351d171feb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:06:07 GMT
ADD file:c0b9ed1244ec0acfc9054c7cb80c768878e3da99740f981ba3a82bdd854305db in / 
# Tue, 09 Jun 2020 01:06:09 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:06:17 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2566ca784846d2d0d4f9105084d94d68d8ea1a82a06a76c5bcd991ce5a10cda1`  
		Last Modified: Tue, 09 Jun 2020 01:13:35 GMT  
		Size: 42.1 MB (42102504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7552721c2a1d47b2d1ed56c76b3fa691a89cc05b4a8c5643b20343b905320c`  
		Last Modified: Tue, 09 Jun 2020 01:13:42 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1aeb911767d0e4b2c8b78116b22d4b47590a4ccc391fcdb3d9b8a4654c458729
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43161146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96661f702d1540693f8c217cd86767fb94e2b447c29d8cf48b4d2c9dfa4425bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:22 GMT
ADD file:5cbf00485aed776e940988cadfad6853c640c13635ae54fb2b00aafccfe81a73 in / 
# Tue, 09 Jun 2020 01:54:25 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:54:35 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4c4f692ec920eecb1f30d9ef8e50125217decc872d7ada6eeccc36c6dcb49e4d`  
		Last Modified: Tue, 09 Jun 2020 02:00:09 GMT  
		Size: 43.2 MB (43160923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6534fd694f14dd2904793ce055d9ae70cd5f756f5579eb9ed51592dda8fbb02`  
		Last Modified: Tue, 09 Jun 2020 02:00:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:899b66bcf3af377dfc5d4c71d68468402999375d82f3372a9cc7d5e2242bd807
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46095076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a9cda77f1745323f6c82dfe9531a4e6aaa1038f0ec6e920ca84d2362552625`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:17 GMT
ADD file:6bbeeb0773b96fccb4cd5ba81dd19ec3580f8d8a3cdd3f1d6a3d2b514fbd6eb1 in / 
# Tue, 09 Jun 2020 01:42:18 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:42:24 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9e88f215fab896e3a7d1d2ce75c0d79960b236066e9033b97e76ca7f01ff2fdc`  
		Last Modified: Tue, 09 Jun 2020 01:48:12 GMT  
		Size: 46.1 MB (46094854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1ba1219e788f52f71700ab1dd6407e016cfaf42ae2f8914f3e6948882eb473`  
		Last Modified: Tue, 09 Jun 2020 01:48:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:d87a25305470755325ffd4d07496a66ec94d18b4d7942ab2b60ac5c9f3cf4e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:99c69d6fbd7bb7c92d7c8f429c004b21508727e72e1b7aaefedfd06bdff99020
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54917746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ef70cf5583e9af3f63e6510a1e78339ad5c7ab03d4adb3bb88208876be9daf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:30 GMT
ADD file:aea313ae50ce6474a3df142b34d4dcba4e7e0186ea6fe55389cb2ea903b9ebbb in / 
# Tue, 12 Oct 2021 01:20:30 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:20:34 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bb7d5a84853b217ac05783963f12b034243070c1c9c8d2e60ada47444f3cce04`  
		Last Modified: Tue, 12 Oct 2021 01:25:37 GMT  
		Size: 54.9 MB (54917520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799356225d6dc165ffbfa67601d6c134bce1964c3c27653dd570ce8402fbcee1`  
		Last Modified: Tue, 12 Oct 2021 01:25:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:96d16fb911e1bdb4856c459a8344f9aac828f8f0b53368378aad6732ddd19e05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52452426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c79f29141f679338338bc53354a1416ca2cd20ca9a726ef8ee3814657bee44`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:49:54 GMT
ADD file:b9969604315238de271e1769a4b8dd85cdf0d33f9fac387e940d5195ac3030a1 in / 
# Tue, 12 Oct 2021 00:49:55 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:50:12 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a97c782f2538791984ce12c859cada96e395e3950d4cb7d1238e08acd2eb74ec`  
		Last Modified: Tue, 12 Oct 2021 01:05:12 GMT  
		Size: 52.5 MB (52452198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a06514d4dff5ba89305dc9bb3d0e5da4e123193ba836b6e5b172d0c5859cfe`  
		Last Modified: Tue, 12 Oct 2021 01:05:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:013b564494f6acd7dcbe8360defaaa4a3a2fc62ffbb5cca6e979b82e0eabbd96
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50118902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c69850a1bb73676acb3ae05afe0ed632ac31bb8777e77357b0ea1111c0470f0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:27:59 GMT
ADD file:d9f40ca54fb79741d1e76c7bca9250f78453d0b39fb6c921337f3071a79a55a9 in / 
# Tue, 12 Oct 2021 01:28:00 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:28:16 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:88ce59c3081c4041f41eb407032db40c207cc2d806ba0eb12e170b697db91e52`  
		Last Modified: Tue, 12 Oct 2021 01:43:42 GMT  
		Size: 50.1 MB (50118673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08190e7f5185f893be8d7f9b6e7f0ffda23089cf4a5d4ce7c4712c738b715a32`  
		Last Modified: Tue, 12 Oct 2021 01:44:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3fd3076ecab5e5c319f83b3ea8fa270523788a404ee5675e84f39341cf3ccc8d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53603242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e165b88145286cd15b37d929ac620ba0aaf7b74c7dc8cdfd0b02bb72894f9ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:04 GMT
ADD file:1529ae12e334fd992892d3fb97c103297cff7e0115b0475bec4c093939a2bff7 in / 
# Tue, 12 Oct 2021 01:41:04 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:41:11 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1c47a423366578e5ce665d03788914bf0459485a627a27896fa9c5663ce55cdf`  
		Last Modified: Tue, 12 Oct 2021 01:47:41 GMT  
		Size: 53.6 MB (53603015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9d52455d85c315d0d0207631c92edec49bd2547a071a60682d32794c681b7b`  
		Last Modified: Tue, 12 Oct 2021 01:48:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:17a6f9d8fdd0ca7babd4e790864a43998954758bfe1f63448f52baf8fbf0e3e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55923644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1253d103f5ee0fc52c69a557fa850bdb134d2cb4a0f55f3c5ddcd549aa2114`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:39:30 GMT
ADD file:e007d6eff02dbc696e1166db315b97a77ae8aa65f2e66ca8074765dde9c70a59 in / 
# Tue, 12 Oct 2021 01:39:31 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:39:38 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6911c8f66691266d86e2cafa67ca005d919f357436fac971c694d37625b5ba90`  
		Last Modified: Tue, 12 Oct 2021 01:47:06 GMT  
		Size: 55.9 MB (55923419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e386791194a3b2c5f5bbf14267f165ec4d32db20fefaf800786554d7d2124bc`  
		Last Modified: Tue, 12 Oct 2021 01:47:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:368464ec5c56f2b640a6d9944ae7e3e1abac9c9549ae214e272cdf6a68f06bd4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53170065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3792ce1079724323b0cbf97471cd2db55c5de9a93c65803615b93fa43c1284`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:10:49 GMT
ADD file:856952232716a2e2d5069387a06a537937a1dec1bb75bc9519c60d6ad226bddb in / 
# Tue, 12 Oct 2021 01:10:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:10:57 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3d2cd78b9c44ce4eadbb0cc35b884bfd0dac51123f3c8c6645cb8dc9dc9c1512`  
		Last Modified: Tue, 12 Oct 2021 01:19:18 GMT  
		Size: 53.2 MB (53169836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e006cd97eb9073090f248bec077c5d09eb03d7f4042af018120745c0d000b843`  
		Last Modified: Tue, 12 Oct 2021 01:19:35 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:40f8b8b2e3ea477ad834637661bbddd461a2f56b32c04a1b887ed0404e85f6a8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58809106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a6877f5dd128c20503b72eb18b2926abe77cae1a58ce5df093a7814e83d067`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:25:04 GMT
ADD file:127b21494e1c790bdbb4c277638b3e16b25fbbcd1e0cdb52e60a4f55a57cd0f2 in / 
# Tue, 12 Oct 2021 01:25:10 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:25:26 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c7e7ddcf3b3abfed2b7aab50c1b68bfdfc6fcffed2f4b93ebff4d6050b3d5e72`  
		Last Modified: Tue, 12 Oct 2021 01:36:12 GMT  
		Size: 58.8 MB (58808876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56fb001a0c62f3a0c70976e2acd34e874089886aa5b0f8ee10fe1e6e579ef15f`  
		Last Modified: Tue, 12 Oct 2021 01:36:31 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:b197bc5c4de0dc464c4e04dc9afc53a974157b59b36c5eee0ed80b8994feb7e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53193120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194a980937758b4f99a072dd0852f765701e9b001b176f5ed422ba5a9a89e918`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:42:09 GMT
ADD file:a7a74f6be757ceb5e84c440e739019782df1a118264eef70aa49886a976c43f6 in / 
# Tue, 12 Oct 2021 00:42:12 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:42:20 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:081299fd984cd296112766e1cc55f44fffbf898b2900b01c0333962494a2dd80`  
		Last Modified: Tue, 12 Oct 2021 00:47:43 GMT  
		Size: 53.2 MB (53192895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659e14461d58f8fb62b8e8f7631205eb1ff6eea842d61605a55232b8583d46f3`  
		Last Modified: Tue, 12 Oct 2021 00:47:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

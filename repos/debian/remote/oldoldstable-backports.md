## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:b58a1ffd7008a50c7be8f7ea3e6c04a47ed6e0c374e88b03b8e46b94ce851bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:98cfd3bf25c3b9a58c5125686004d77090e5236b37f17aeb7aecda7cd675c3db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45428249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399941c9a74dcbe41a1e30fde26c758c0f672c66a2034b03acf3fb7843afda1c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:20:46 GMT
ADD file:618dd7abcf56d90c7ca58dc804d590f1dee02bcfee24e5050569f18bef1d4507 in / 
# Wed, 11 May 2022 01:20:47 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:20:50 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6df64da9505935dfac77000f696255b30b84c69955ca108861e34ed933468354`  
		Last Modified: Wed, 11 May 2022 01:26:17 GMT  
		Size: 45.4 MB (45428023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f989426b7d1360b59c3069cef39e4dfbda1e0101ec13c174fd7ddb41016c08e`  
		Last Modified: Wed, 11 May 2022 01:26:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:202363b9142aa105bcdac54dc4929efa949b612c19bf3651b6b50475bd1364a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44123136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07ade257156be131d51d3106c0f52f2cf46c28823f029ab47f82ec8fbab7ae4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:52:00 GMT
ADD file:2717e650680c79001502c4c4809e2c7cd3753e33264454e8af66963da07ad9d0 in / 
# Wed, 11 May 2022 00:52:01 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:52:13 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d52943f35e7763aa8e0616f91202bffda56e9f09ea728181dffb18ece7afa394`  
		Last Modified: Wed, 11 May 2022 01:08:06 GMT  
		Size: 44.1 MB (44122908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbf06e8598b7ff0740f1e21ee91cec89869371a08c8975c51fd184904068978`  
		Last Modified: Wed, 11 May 2022 01:08:19 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4f094503f5ed5348a3247736a65cac6e5028870605fb2f01185c9d2a45924cb5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74f13a7104e54a1135011c13fc65d9c59ab2d27a51fd8e00a03bdf1318147b8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:01:22 GMT
ADD file:d57d35bb2ef5ab1b89240fc0879ce8ea57a56ce03835a264175b03072bed30fc in / 
# Sat, 28 May 2022 01:01:24 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:01:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e652aa8e91b0055f8432978e043c744bd6456b290dc0741c223e254badc519e0`  
		Last Modified: Sat, 28 May 2022 01:17:40 GMT  
		Size: 42.2 MB (42150793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e5a83cfe6021a0fca422e8853c46c435323d696bab668fa64b6f4b386d4b3`  
		Last Modified: Sat, 28 May 2022 01:17:52 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5ffa04fa60d5b9ab200b5e41624cd406cf6bf187e1f25ff8e640f2ace1da163a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43213072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adc3f21cb5adabfe066c8fb981a499d2862358ddc90c64de93f2fc3551a20a0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:15 GMT
ADD file:47d38918898d0d5f23861643c07993476ceaa0fd2494ea182b005d136dbea90f in / 
# Sat, 28 May 2022 00:41:16 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:41:22 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:944dc1be71122e13738cd92a22625279fc54718f081f865944241e8ae774d619`  
		Last Modified: Sat, 28 May 2022 00:48:49 GMT  
		Size: 43.2 MB (43212844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f722c195bafaba3de1e67acc490b9bfb6c4e5d1be532340467214cd08f11082`  
		Last Modified: Sat, 28 May 2022 00:48:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:06b181756050fcbb90c0ead427b1cf9c4cbd82db98130ea405290073b498a3e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46150394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99afbdd94c05067f705b371480de79b0d73483d1f1b84a6732fe6ceab4b56e3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:12 GMT
ADD file:5b0d9d0e1f09d8658b36ea70ebf7b209faa4801f72e67b3a83d8bd0d810f7333 in / 
# Sat, 28 May 2022 00:40:13 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:40:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4f74e9e54590523cbd0703a11ecc089fe05c0f9ec8ea4d3e344eff5e4a5c2fde`  
		Last Modified: Sat, 28 May 2022 00:47:58 GMT  
		Size: 46.2 MB (46150166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba187ab79e302b885fc32323aad217b62921a55f71f89f4071392b31770d6718`  
		Last Modified: Sat, 28 May 2022 00:48:09 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

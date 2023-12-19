## `debian:trixie-backports`

```console
$ docker pull debian@sha256:f56e315debf5c80b71c6ae8987f96b661be881e87d7055da84c9340254b234ec
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:4afe3ddc85050711dd20fe95d6192c143276d0d27c1f39a8460d807516d44bfe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49583648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2331c37115f9f50128560604b9d39e5e3640c6ec1f38752123174ef172be06b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:09 GMT
ADD file:29b09152e341e5171aa28f4c4418697f0618e77dc8ad357953cb4e571071f7ef in / 
# Tue, 19 Dec 2023 01:23:09 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:23:13 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7ff2da0727c582fb559afda4ae37f2ea848c8d7098b1d441c8dd7223abd5ff94`  
		Last Modified: Tue, 19 Dec 2023 01:29:35 GMT  
		Size: 49.6 MB (49583423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66eaf40a995ea24ea47cb1cde20c76f129d3ba2c6bfea7bfb786042f8cc483f`  
		Last Modified: Tue, 19 Dec 2023 01:29:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:7cddc058435702f38a72df7992183b652581c733316fc8caa0f38dcb66d0562b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47284973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7de52309ef1afb6e32e570c1f1da580638acd35cb29cd7679bcd87329f3aa27`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:48 GMT
ADD file:4525655c4460af6f1eea7b808845971f5115dc53bd3d22e1e5b904174f4a7de3 in / 
# Tue, 19 Dec 2023 01:56:49 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:56:52 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ef1355a3f40d35583d398e1a76163ce9edc9f474167738235259b9821b4cf763`  
		Last Modified: Tue, 19 Dec 2023 02:02:10 GMT  
		Size: 47.3 MB (47284749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c730352c16708aa532bd25813c73e43c143fc322889e006a66abce2407813c53`  
		Last Modified: Tue, 19 Dec 2023 02:02:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a5bfadd62fedf5b277b58d84aaf66e222c74c4a6bcc147ce0a425b62836face8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45026003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c337f7d73e151dc97bb324b7df2a59493aea114abda44384c0511aa6588aed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:58 GMT
ADD file:59809e0abebdd1dc9132ad810fe8f3f2944fb2b6fa8df3e129a60d19cf0a0235 in / 
# Tue, 21 Nov 2023 03:59:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a13157ca2b3325f6cfce85c5d417fa81a8cf7c5536e5efd4164b11bece6ea33f`  
		Last Modified: Tue, 21 Nov 2023 04:06:34 GMT  
		Size: 45.0 MB (45025780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23497fd1d71fa03463053d8d11d92c5843ec558081c7625a6ca685950b3beefb`  
		Last Modified: Tue, 21 Nov 2023 04:06:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:736809cdcaf6b4aaa95061f2d20b296649d3824fe2b5a5e29ee2929926e30566
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49615326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c326b07ed970e68bf9bfa4a29143e5a854ebc7a4a2cc77b01a60c33885a59e74`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:55 GMT
ADD file:3a7cff48546e976afb3192375ccd816fa228a2a86ca359ad2d25968d89736a30 in / 
# Tue, 19 Dec 2023 01:42:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:42:58 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:54db10be8b28565099ed8931d6e2048335ac2a2e8633f5ee9961d35950099935`  
		Last Modified: Tue, 19 Dec 2023 01:48:52 GMT  
		Size: 49.6 MB (49615103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbcb4c662cf9bb84bf43bfb322f5b4bdf7ec25f6e4d2fd105b31692a870c57a`  
		Last Modified: Tue, 19 Dec 2023 01:49:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:726aaee8b8d133df57f780dbc6ce53cf9a4623d91ef1a8643d66d86db6fc6875
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50558742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f5fcf4bcd176985c6f0175521081a2435a8c2dc7385eb0cddd3d8c5ace30a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:50 GMT
ADD file:07e1f2376b64d47d8fc403056f0e46229ed95c88b19adf23f6eef7ed32a4efb4 in / 
# Tue, 19 Dec 2023 01:41:51 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:41:54 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:682156734dfed71ff79e9a6ecfa1d4b20e0cf3af70b52b635e877f84f0ed468d`  
		Last Modified: Tue, 19 Dec 2023 01:48:53 GMT  
		Size: 50.6 MB (50558518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ced0113e8cd7e2ac4374261e160f891395581a14212ccd5d9979f956e71e01f`  
		Last Modified: Tue, 19 Dec 2023 01:49:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:152c4da86da80278dc126099ad91c537a08847aa330b3d25631a8faa05377a9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49327743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed931655b248673a1837ac92e5054d33c1b64d63e996b73b45331b7bfa86f7a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:16:18 GMT
ADD file:5a5a104714237ebb36fb780708ec93fc6f37e226c70a6cb07acb454559074354 in / 
# Tue, 21 Nov 2023 04:16:23 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:16:33 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d49b5078b4e69925915d9f9be6cb94f93e60122ef1d800b354bcd8216ec830be`  
		Last Modified: Tue, 21 Nov 2023 04:27:30 GMT  
		Size: 49.3 MB (49327517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7563a746deb7a45411ea950de0bc22fc344bd34fb9a9e5b1efc4ac318db0b4`  
		Last Modified: Tue, 21 Nov 2023 04:27:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:aec884b732eef1974d8c10eee527275076bcf64809f3e1a0525c3b1e0497c130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53476704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54950a80c952ea38da80641c967581e6289d977294d42fc75c3b7e9c0e1813b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:24:15 GMT
ADD file:0c76fa40c0d4d6eec23b49588ff6dbe4b5563f6db327a13831ab7eb6e3f30743 in / 
# Tue, 19 Dec 2023 01:24:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:24:22 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9aa21f27abca3b3157546abcfde68519068ba019777333f48885704721c81290`  
		Last Modified: Tue, 19 Dec 2023 01:30:10 GMT  
		Size: 53.5 MB (53476480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3182b5da1746e4fdc7acb84e703e40ceb03fd77fc5bf61a413ba1c284a5db832`  
		Last Modified: Tue, 19 Dec 2023 01:30:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:f9a5f3ad766cfcb6b2ca297c061c562a797176688dd83e646741f4235a443167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49047953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a5974c842b6f2e5f66a4d8dac3b686731d20debe73c23a2402c03dcdf98a5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:45:30 GMT
ADD file:b16365f9cf7d013b9f58428c1e63b824b4c10cd69e7e4899e47af1a279108581 in / 
# Tue, 19 Dec 2023 01:45:33 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:45:39 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b824578a72fec7523b71b452ffd659ecf374f66d41368945e63eaefb55285ad8`  
		Last Modified: Tue, 19 Dec 2023 01:49:59 GMT  
		Size: 49.0 MB (49047729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba04a60e8636ce00990aa56b5148aa09e1c6f504df862ee0864186d2f3b0917`  
		Last Modified: Tue, 19 Dec 2023 01:50:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

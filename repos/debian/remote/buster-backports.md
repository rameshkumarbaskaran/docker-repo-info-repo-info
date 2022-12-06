## `debian:buster-backports`

```console
$ docker pull debian@sha256:942a56c8e2196e15e94a7dc823a6389ed2ccc76904f081544d22e4f8d81385a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:c9b2d1bb53a7e408f36e4b981ad3e809c703ee57631ae5909be8ac27653336a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50449089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f578e6a4606410f56a986bd1ebffda6073d8005cda5ade7b026db540084866b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:05 GMT
ADD file:00d8a84de32d523b936621886a10683664f38d8ec0846a60511fcf3a99d0e0c4 in / 
# Tue, 06 Dec 2022 01:21:06 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:21:09 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:620af4e91dbf80032eee9f1ff66a8b04119d7a329b2a13e007d69c8a0b337bf0`  
		Last Modified: Tue, 06 Dec 2022 01:25:30 GMT  
		Size: 50.4 MB (50448865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3a0fd6816a084b815066e668841c067c202627a873aee3d1348a85ff0b6dd3`  
		Last Modified: Tue, 06 Dec 2022 01:25:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a564114b5685a1ecae78ad6ae5e9062fb2dcb984856618de792e072ab4e0ade1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45915678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f619026b2b4ab16f482d97c66c212048ffa6db6d8572003fafe30cb2e60f278`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:59:07 GMT
ADD file:ee219183e8f6a070cc7dfe54397117bf655fa7e49d4a4bdf4263def0bf115d26 in / 
# Tue, 06 Dec 2022 00:59:08 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 00:59:16 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9b267c960f47219a48e4194e0bb9cf819bb30aeae42c7f03732421b84855f2d3`  
		Last Modified: Tue, 06 Dec 2022 01:06:29 GMT  
		Size: 45.9 MB (45915455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daecaf52883e99cfc8ebb5a7a0ef9c38cae3f674f52286c5d6ae7a238fcf580c`  
		Last Modified: Tue, 06 Dec 2022 01:06:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ce9e61651f23da52baccc82e1283504abd8eb18df6dceb1fa92fc954c8a36729
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49234007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec8946d05d31a281563762ec1e1972364cea8561bffca7a5e13c49f0adbe812`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:26 GMT
ADD file:2122642b8ad9a333f73cba41ff9cc829542740e0e3c88379a7c9511fbfc28991 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:41:30 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:34983cc1fd1c67f0d8b7b8b4320539206a1c098388b3a671abe88b45f157978d`  
		Last Modified: Tue, 15 Nov 2022 01:44:52 GMT  
		Size: 49.2 MB (49233786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95ba42c648809f33f099f8a6f0f81b1287d5ba05498322d18485d86f07cd3e4`  
		Last Modified: Tue, 15 Nov 2022 01:45:05 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:444b9a1d964b1f9e91b2e9fadf56259239497144bf26c9065ea460be474e3851
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ab75d1d070b7d11d1b50a3d7a72a5823b7c6173e855c764bed9d568e0a517a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:38 GMT
ADD file:e8c5010609ee5ceb22093e461dbe3f9748a4d6ca2fd436e635276b0f99e777e8 in / 
# Tue, 15 Nov 2022 01:41:39 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:41:46 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a9674eda0741cb717f181697e2f2695ea87fdaf557d253407a096f80ad4f9fb3`  
		Last Modified: Tue, 15 Nov 2022 01:47:27 GMT  
		Size: 51.2 MB (51207653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5563b6f1f70991b2e55043400a3da8e9f259c2c993c0dab6809f29290f545f49`  
		Last Modified: Tue, 15 Nov 2022 01:47:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:2437a1e2cad84091b2e8393d0a736af68e46f377f6c499327516e4815feea613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:00b0f3aca41e1135dc391f626f66f5b6a086ee260c995f37805f27164957691d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119954274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dd589d27b2d2d0733d458cb149600accc2ea5f8f818c903bddb738204c8426`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:23 GMT
ADD file:1efe9845e057e7029a1c2c26c148e6dc1bd9c65d0cbbb23cb49c86295d1f1f48 in / 
# Wed, 11 Oct 2023 18:35:23 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:22:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99db33be616a9a2a0b0b1bc913b548317bab7bd11cb6968d357457e201c44077`  
		Last Modified: Wed, 11 Oct 2023 18:40:37 GMT  
		Size: 50.5 MB (50499400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4df9fde773e0c195208a941f5c813fcae5310dfa340b1092a91ca3dca2f0997`  
		Last Modified: Thu, 12 Oct 2023 03:30:53 GMT  
		Size: 17.6 MB (17580739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c0008f57ffcdd8594227fc498eec4c4660fd627978baa26cf04a9a18908391`  
		Last Modified: Thu, 12 Oct 2023 03:31:09 GMT  
		Size: 51.9 MB (51874135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:23fa82b6ce62d4459c91ba9cd6a119c8132666e0e84b1bccdbc46652fdd4fa8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109590939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419a7b84b078554b5177dd14ef6a12e1a6696df651c438b2bcf3f8761077497c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:37 GMT
ADD file:90492dd68d097af40a6208353165e1b7e2bc04a31cd2270232e085416f6e940e in / 
# Wed, 11 Oct 2023 17:42:38 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:48:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:49:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ecd2705b9dde659b853da74fbe8d7227d02acd96f1d34766d44193b82468b37`  
		Last Modified: Wed, 11 Oct 2023 17:47:27 GMT  
		Size: 46.0 MB (45966353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2548d6bcf8bfe2322ed1ed9f56eeab4afd1b65e4c4a62d0be4d602f14dafc992`  
		Last Modified: Thu, 12 Oct 2023 03:58:22 GMT  
		Size: 16.2 MB (16213670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423a7661d20a90498af23198b35b85c16af055a76453a7e8392ce97b5f4e398c`  
		Last Modified: Thu, 12 Oct 2023 03:58:40 GMT  
		Size: 47.4 MB (47410916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:142a54e609ce722402983f6daa77ee12ec5baf50a191b64ef7f9a4c85262597c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118951546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b138e1d073c5b16678192fbfb7949d838e13e95902b21affb91b17aed7e9f89`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:12 GMT
ADD file:d97d8c89883987c89b2150923abea982086030e71970f5473a534e95252b4972 in / 
# Wed, 11 Oct 2023 18:25:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:47:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 19:48:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a7acee270b8289bdc6bb8836f1a4899f794d60337a0cdc46b58a717bd27ba89`  
		Last Modified: Wed, 11 Oct 2023 18:29:25 GMT  
		Size: 49.3 MB (49291086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d43a8471c221305b41e4a48fe1a36d8d976208b182f048b98aa6dc81e6fec8`  
		Last Modified: Wed, 11 Oct 2023 19:55:54 GMT  
		Size: 17.5 MB (17451818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a82d27a09b100de4594fbc9e341ab946a39a8d635f12e633b1341a1c7aaa4b`  
		Last Modified: Wed, 11 Oct 2023 19:56:09 GMT  
		Size: 52.2 MB (52208642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b9714a557ba551d0e25530e69b9c38752fec848204c2e0791697c79dacbd1d67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122841335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce745aed3b333b25b3e5c0db30d1014e3561c2f1044192ec0991f69bb7cecf8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:14 GMT
ADD file:47cece2eff96bf7383dd2a9c5632f0ad7bb31b3a459677530f77a78e22658e98 in / 
# Wed, 11 Oct 2023 17:41:14 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:14:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:14:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:62bc68699d611f4c048328a0468ebc10de528260c7823c8938796da30db31a17`  
		Last Modified: Wed, 11 Oct 2023 17:46:45 GMT  
		Size: 51.3 MB (51256071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a664405fd519ae385ebac7659c355b2c380dd5c84037f38e6d3673b2bd9795c5`  
		Last Modified: Wed, 11 Oct 2023 18:25:03 GMT  
		Size: 18.1 MB (18097310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c138636d1c51e715c73bdb28e49fb18fc2d82cca0a21d5641a911f48cd3ff695`  
		Last Modified: Wed, 11 Oct 2023 18:25:25 GMT  
		Size: 53.5 MB (53487954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

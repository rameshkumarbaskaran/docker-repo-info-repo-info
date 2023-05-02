## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:a8bd2b5b7c577b850dec3522b5381e07fd8d046ea46c52facfaf6ab2748d6f5e
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

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:22e8a94a63b1cf94bc6e69418b975d41cb9ca48640b8b3a48002eb9c65039abb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125680982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cd24e709af1ad98665077ad3ae2b89451839cb3a36350db232d6ce523d0d60`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:50:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:51:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e97b4daf784e08840a21765f0d4f251192ef2994d0e4a253490f81e63955b`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 5.2 MB (5166696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0336c50c9f6942b660e433b1086238eec37057c34b14c4e3b28bd7bf05bd84ba`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 10.9 MB (10876749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89f3c7f7da8adf032a33a75d1b659cee33179ecb88ea0ba75e4fc58ebe63a6`  
		Last Modified: Wed, 12 Apr 2023 07:57:46 GMT  
		Size: 54.6 MB (54584801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:893596fd204b9aab3c12c530383e241b51a14d600048393a40d0533689392e76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120256008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7429c5c2e47ca8766e3fc31bb3b55f5052f4dd013e929b9a0000921babd4c58`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 22:48:45 GMT
ADD file:e5816cf9c67a55e94065100a95ed3b269817a643b21e5b9c060bfde394a56889 in / 
# Tue, 02 May 2023 22:48:46 GMT
CMD ["bash"]
# Tue, 02 May 2023 22:58:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 22:58:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a091ba323f94f60ffce46d1dad6471927a6d7136843d7bbc29ede769d6cafd86`  
		Last Modified: Tue, 02 May 2023 22:51:00 GMT  
		Size: 52.5 MB (52546533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af95a5c50d56314ef6847c1ae53a11674a55f64d66644740b586d5a69ce8cb6`  
		Last Modified: Tue, 02 May 2023 23:03:56 GMT  
		Size: 15.4 MB (15368899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23e522036c22d996b09a966ac4cf5a6154b930cca1e1e7e135660324bee54b4`  
		Last Modified: Tue, 02 May 2023 23:04:15 GMT  
		Size: 52.3 MB (52340576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bca4866a43bc982429c365a3c9eae150e257f6e85a758fa3d39d843b62e8f5a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115725058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb174836486b1bffbdfcbbc82c0c81dfa80fde95c26ad135982dde37aba1e99`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:35:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:35:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f77534be142d18fb6441aad5ebb0a6b1fbd1128fee964f14c772d3f48978f`  
		Last Modified: Wed, 12 Apr 2023 09:45:07 GMT  
		Size: 4.9 MB (4934569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0797973d3ff4c7bfddd6439ceacd815ea867f868a8c75686d5b80ee1a3eca322`  
		Last Modified: Wed, 12 Apr 2023 09:45:08 GMT  
		Size: 10.2 MB (10217876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cff4fab8e209a4a8ef903baadd1f4839687988e57cef0235a447c0198ddfab`  
		Last Modified: Wed, 12 Apr 2023 09:45:28 GMT  
		Size: 50.4 MB (50355731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8932a28128c9d2abaed3ae68d2641c6738ab07bf083ca8886920e13ce37bbce3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124407974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7143247bb9728129c637c315a5d5529383d57dfbf55c6999d1479a6f6dee2b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:06:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:07:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5884e7f2c8c61aa845de4902fc29639b58861ae6c2d80bafe82082c0456c0740`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 5.2 MB (5152752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b792b01ed3c8dc1488cd8aac41ab7d49bb17f3fa22b2e6c846078cec81a1c00`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 10.9 MB (10873655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f993d5b17f32f4b8a535c25e182e5d8412625beee450e513ca57036e8fdd6dc`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 54.7 MB (54676038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2af50719cfc3c1165d1e75a99045d98388d375c4dcf2cafd5526a78d50080eab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128499065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7863e942eeec226faacc53f695802b0b24e7dd766b5e4a9498a0d7c62e92c702`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:05:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:05:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:06:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37ccf9a5e34ba2345ce265a9a11c93ee254e1f3616dfd1c1deda6e2f7d614c8`  
		Last Modified: Wed, 12 Apr 2023 01:14:53 GMT  
		Size: 5.3 MB (5293626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988d5e4328f031f6884a7351766aa8a2806c9cdca38d354477fc537eaa4911f`  
		Last Modified: Wed, 12 Apr 2023 01:14:54 GMT  
		Size: 11.2 MB (11249875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660a2befd486d43a308dd1561f57efeafe1f13defd6439d34aeb5efec783ee3d`  
		Last Modified: Wed, 12 Apr 2023 01:15:17 GMT  
		Size: 55.9 MB (55922746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cae0c78b86d9818b2acfb8edab82633baa924d1c55cf73f682790afe23194474
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122368048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2e60633ae43426dc3b6ad6b6c990668c1e5a30f73bfab6f97a660d5d16ef9d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:00:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:00:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 11:02:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed6aed7903d464c3c421335c8a4b93f11e64b669c7eab532e87e5945fd185e2`  
		Last Modified: Wed, 12 Apr 2023 11:20:32 GMT  
		Size: 5.1 MB (5127336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af3f0065ba2217f3ef903c35f7e644bd2222c1630a96ac62477510cedfa848`  
		Last Modified: Wed, 12 Apr 2023 11:20:34 GMT  
		Size: 10.7 MB (10662154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81fa7bf218e18cc100c89241735ff424465ba8caca78835fdadafcd212de62f`  
		Last Modified: Wed, 12 Apr 2023 11:21:19 GMT  
		Size: 53.3 MB (53306535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a328c66040a29e932ae7b1d267bd4b11602af4f3cf8bf7a959c2ab0b2c7b2541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134837330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1795d723a8d4b32e096f6732a2e5a3c212e5f6bb12ad9bb5c0e5dd1b4257eba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:31:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:33:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00772c18aacd8e2ae167f5f94b2e86c7b77fd3f7790dc5e6754e48fcce1ff484`  
		Last Modified: Wed, 12 Apr 2023 09:45:12 GMT  
		Size: 5.4 MB (5415380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1877fd565f7c580ab3b8fd343d19de69c9c3334787d6a3c93c9c21fe08ea32a`  
		Last Modified: Wed, 12 Apr 2023 09:45:13 GMT  
		Size: 11.6 MB (11629984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a24a9774fce2d157b32633fbd68d6d4777632ca49b0a35d2e9be9a2455d88b`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 58.9 MB (58865366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dfe7b376859cc874a19230408e2042b1d984722eca290ce8cced0e27c6bdc7bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123263942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0184582450f7852885e4f2a6aaf51c5ec9ce0ff2ce9cd9b877a945b87bfd33c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:26:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:27:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2973b8c98f9da7833ab9cd69185dd958a8939a30136cdcfedb66ce775db358ee`  
		Last Modified: Wed, 12 Apr 2023 00:32:48 GMT  
		Size: 5.1 MB (5149313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f740d13ac612bf8b6489559a7945ec1439fee2d5eba455ab0db047cd3f30a9a`  
		Last Modified: Wed, 12 Apr 2023 00:32:49 GMT  
		Size: 10.8 MB (10766104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c0067783f401b099adca196dce9e464e66236e49faba106e2f04ac73a90df7`  
		Last Modified: Wed, 12 Apr 2023 00:33:02 GMT  
		Size: 54.1 MB (54061843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

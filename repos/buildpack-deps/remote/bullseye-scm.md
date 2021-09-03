## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:ba785fc26f28074b21d0f6cf8e6dcdf477c0de5821105d048d673ca189eae38e
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
$ docker pull buildpack-deps@sha256:4482cdfc3749014ec1c6585615da606059839c6c8f5716bbfa2de11549181798
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125518492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8ce923c4bc1e83b4d6d8109a4464618211fac83f83479ff101995f9b7a40fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:07 GMT
ADD file:1fedf68870782f1b44cd50691444aab4061cc0c70f24e5fabe9c562cc46eb9af in / 
# Fri, 03 Sep 2021 01:21:08 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 06:31:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 06:31:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 06:31:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:955615a668ce169f8a1443fc6b6e6215f43fe0babfb4790712a2d3171f34d366`  
		Last Modified: Fri, 03 Sep 2021 01:26:55 GMT  
		Size: 54.9 MB (54926871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2756ef5f69a5190f4308619e0f446d95f5515eef4a814dbad0bcebbbbc7b25a8`  
		Last Modified: Fri, 03 Sep 2021 06:39:22 GMT  
		Size: 5.2 MB (5153100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911ea9f2bd51e53a455297e0631e18a72a86d7e2c8e1807176e80f991bde5d64`  
		Last Modified: Fri, 03 Sep 2021 06:39:23 GMT  
		Size: 10.9 MB (10871687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b0a22ee906271a6ce9ddd1754fdd7d3b59078e0b57b6cc054c7ed7ac301587`  
		Last Modified: Fri, 03 Sep 2021 06:39:45 GMT  
		Size: 54.6 MB (54566834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:25400321d2573328a3a4a5ca398f3e0d11056d903e39f334939e80717fd8127d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120415442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c9ec9c2d5a6c44f4f20dee32d5687a7f6699b5ad60a5fd9da4530f37f0f010`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:49:54 GMT
ADD file:1e667a7a6266f0b2af7a4c7638575e79c77fb7cdbe2034cc4673d83fe7251899 in / 
# Fri, 03 Sep 2021 00:49:56 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:31:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 02:31:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 02:32:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6dc2bdd42eeff7d4a88d4ace72cf9281d77232183d6919b4c3162051e654910`  
		Last Modified: Fri, 03 Sep 2021 01:04:48 GMT  
		Size: 52.5 MB (52461500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06f9763e0efd7dcf980819e39cb728c9f11f3c3f7dd944e21177efba57f6fe3`  
		Last Modified: Fri, 03 Sep 2021 02:51:03 GMT  
		Size: 5.1 MB (5063642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95efca74ef694ced85d684e7faecd407beb97667568054d98e5e09166a32d88a`  
		Last Modified: Fri, 03 Sep 2021 02:51:05 GMT  
		Size: 10.6 MB (10570971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1df2396712ed6cf1ebf81db19d8e162b1c621c3fca9971be211747d7e10bf8`  
		Last Modified: Fri, 03 Sep 2021 02:51:58 GMT  
		Size: 52.3 MB (52319329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5493047af5f1017876bef0d60e997163eef8b592df5dea0f53ca17ee394f496d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115594855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3296795ee994a1bde3dae9a46a66b14d50d65e857a0318ae36c2a401565880`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:59:03 GMT
ADD file:a885b024f19da3fff424486fd5495eaae458dea6a1038715198e0449b6b00518 in / 
# Fri, 03 Sep 2021 00:59:04 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:52:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 02:52:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 02:53:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ff8c004d0dc8a6ef263acdc2f23760be64e46bb9a75384a950f29b2c5d8b5c98`  
		Last Modified: Fri, 03 Sep 2021 01:14:05 GMT  
		Size: 50.1 MB (50127257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09133804e9cabca8aa15fc0b84dbfd8d87f0f01e28c315b5f5ea48ab2c913450`  
		Last Modified: Fri, 03 Sep 2021 03:13:16 GMT  
		Size: 4.9 MB (4922592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00fc4682956757d850f7d8ed7259e823f6c972e63fdcd37082e1673502aa085`  
		Last Modified: Fri, 03 Sep 2021 03:13:18 GMT  
		Size: 10.2 MB (10216805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2ed13e4cb879d0509b38f09a3fd873792d4e751b5be323450dd7b65f2b7f8a`  
		Last Modified: Fri, 03 Sep 2021 03:14:10 GMT  
		Size: 50.3 MB (50328201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:171efe411f0b2837774ac781afcd20fdf765f2740c709eb89d42e1ed40933ae3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124298234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64a1f84d5169956a41cfec43bbd75988ce70cf67bc260e13cb4abed5dbed09f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:40:18 GMT
ADD file:0b1ff9dcb90d6b787179d2e43ca534c39e0372227a3af198bab158a89fb2c966 in / 
# Fri, 03 Sep 2021 00:40:19 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:32:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 04:32:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ffacddc51d82196acb1d49f2e3c13601fc16c61c995a860b450d23b000353ca1`  
		Last Modified: Fri, 03 Sep 2021 00:48:17 GMT  
		Size: 53.6 MB (53613054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f80252dfabbfc5bdf4862b9fa8d2de7110ac4a6f08bf30e6f574f6243d0c93d`  
		Last Modified: Fri, 03 Sep 2021 04:40:56 GMT  
		Size: 5.1 MB (5142543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138e2c18ad04e197e8431cfc2923456979d5b0cfb9c6549a62bcd3732d77bd03`  
		Last Modified: Fri, 03 Sep 2021 04:40:56 GMT  
		Size: 10.9 MB (10872696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9597521670e83c9cc67fab06b99d41fef6d1d65c0515c50154a74e2e4f4c7fc5`  
		Last Modified: Fri, 03 Sep 2021 04:41:20 GMT  
		Size: 54.7 MB (54669941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ad88db1472e0c705f72cf52470e55fd98ca5e14e00e67cfa4c1ae2491f4b42ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128380780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f54f21a8eb6c7073aabdfbc66893ce44b6e77dbf73034a40c13c913bd246f5b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:39:34 GMT
ADD file:fcade9a23463d6b59cfafb811fd21f2143d482e21ea836e9c2e4796136459599 in / 
# Fri, 03 Sep 2021 00:39:35 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:10:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 01:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 01:11:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a62297bd75cc0ee79a641136889da30fb39e2d05074874bd1d73ebe2edb6f8d7`  
		Last Modified: Fri, 03 Sep 2021 00:47:28 GMT  
		Size: 55.9 MB (55930933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853d83532467d1599448d38360ea9d52789d7d10f30c6734e17728c98743435b`  
		Last Modified: Fri, 03 Sep 2021 01:19:38 GMT  
		Size: 5.3 MB (5282881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6935e9ec29feb2101753d15eca8fa2727e2b060c07d2f720f471c55fb344c2a4`  
		Last Modified: Fri, 03 Sep 2021 01:19:39 GMT  
		Size: 11.3 MB (11250633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf6b2b625a6c874fcfb0e659f71235906f8459aa36ce32066b8efe1daf7c855`  
		Last Modified: Fri, 03 Sep 2021 01:20:07 GMT  
		Size: 55.9 MB (55916333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6f7f0eda304eea56cad106a2326a1c13b9795bf40b8cb034bf22216101812a76
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122463445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472a6e379480171cbaf23c6d657f64a0656a5f76461f1ee4e7b779f4d3d2e2da`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:09:38 GMT
ADD file:aaed6c610924ac8eb3eb6be97263abde763b266a7057c9a6b5bbf8c481ddb348 in / 
# Fri, 03 Sep 2021 01:09:39 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 01:45:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 01:46:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:47d27042240b42cf414701e6bb0ab3bbf22fdf98f796e21e982bdc39dfcbfff4`  
		Last Modified: Fri, 03 Sep 2021 01:17:39 GMT  
		Size: 53.2 MB (53177233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c468c327f30e2c4a9f92e92b7d44ab0402e717f6047b932c3c187c928a59b892`  
		Last Modified: Fri, 03 Sep 2021 01:58:10 GMT  
		Size: 5.1 MB (5114874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ab3751dbc8fc081bb5a6a11049a3ab73ac7deb555b20b222aa3ca1b94bca80`  
		Last Modified: Fri, 03 Sep 2021 01:58:12 GMT  
		Size: 10.9 MB (10873363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8918f43385735f5455e955ef94ef61f2089c0caebab840605cb52e5dd7525cd4`  
		Last Modified: Fri, 03 Sep 2021 01:59:04 GMT  
		Size: 53.3 MB (53297975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0079fcd37f046fdbc47f73c68e3301b7cb70947b2a248d6c3fc28008143759bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134696289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a755e8f1b32b86a7e3c3eb1702fb2c523aacade98b66f54fdbd1dc1631465c0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:22:22 GMT
ADD file:3d1033153ba97e1c4e4f513c14db9d9f913ee4c4ce2eeb554bcaf6c5c9665c80 in / 
# Fri, 03 Sep 2021 01:22:35 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 05:56:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 05:56:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 05:59:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5180655d8cc68420b0aa96b7c8db9131c02ad0ca93c166dffc9a3a49b22005c2`  
		Last Modified: Fri, 03 Sep 2021 01:35:56 GMT  
		Size: 58.8 MB (58819434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da65065c5d0fce3d2a476e0889f0f7a8b7930d0c520fac7b518ea03e759ee66`  
		Last Modified: Fri, 03 Sep 2021 07:08:23 GMT  
		Size: 5.4 MB (5401774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae33292258b5feea63dc49d85ead1ab3ab4ec648ab4c231dc8aa7db7886e21ab`  
		Last Modified: Fri, 03 Sep 2021 07:08:26 GMT  
		Size: 11.6 MB (11625942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708d04ed929be54f33cfa94416648dcac9edd8c01746ecc6e250ce046aa54ac0`  
		Last Modified: Fri, 03 Sep 2021 07:09:38 GMT  
		Size: 58.8 MB (58849139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:485ac24b4b3a8b7585b955839727007d6a2758907be6a957c535027848236e2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123150315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa3622158c598757cde789c4df5c79291a8281dfa04b2a762e7e95f1e603db9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:43:14 GMT
ADD file:fe20239b717a5727a4629774155356432b5a2535dc21ce2df2ee00314b48132f in / 
# Fri, 03 Sep 2021 00:43:22 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 02:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 02:04:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 02:05:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:440698b773ccf4480ce07124f15edd8dc6e88ddec22635fb3aa782759f4696b8`  
		Last Modified: Fri, 03 Sep 2021 00:52:28 GMT  
		Size: 53.2 MB (53201154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f48d5133e49359781fde1a8e72c81879ba30ffcb5b6d759f0ecb28fe6bbbe8`  
		Last Modified: Fri, 03 Sep 2021 02:19:40 GMT  
		Size: 5.1 MB (5137216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab672e8b32c6e3623bde683097d4c5fe5a73090dcb963e9f5512dfc21c485f58`  
		Last Modified: Fri, 03 Sep 2021 02:19:41 GMT  
		Size: 10.8 MB (10761458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef7068e3642fc5ba5e489f8857ba725ba64ef0ce4b28acbf1545d133584bae2`  
		Last Modified: Fri, 03 Sep 2021 02:19:59 GMT  
		Size: 54.1 MB (54050487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:49cb6684ce881c41dae65834a89624b10f76ea7f50018328dd1a7f01e7b91bb7
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

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9a8dc5fb0de072162e4982b81be18e4a99362490bc9c98f73c555dcf73df7526
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134405925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117234419216a3681e04989309f0040e891a89fb4f7df17d851ec6be0c779d71`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:58:17 GMT
ADD file:cd33732baf7a8215a9cb532ae6f2fe0be64d030adb1f3e0085e461cf4f22ec4d in / 
# Wed, 20 Sep 2023 04:58:18 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:27:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:27:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3954180d94025620e480192adbba35d582d59582f662e17f992f954d83539feb`  
		Last Modified: Wed, 20 Sep 2023 05:04:48 GMT  
		Size: 49.5 MB (49467670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e565cc2b6bbf1308bd8312f40ad760a99d8567113763dec2537af6652bb673`  
		Last Modified: Wed, 20 Sep 2023 09:34:11 GMT  
		Size: 20.3 MB (20269130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd10974eceaa5affd1244428fad92105303c6661b8d09326a7a85b3f11de3125`  
		Last Modified: Wed, 20 Sep 2023 09:34:28 GMT  
		Size: 64.7 MB (64669125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0ebff169c1476a3a84b0ddec9c0d87c66ee5c9c7c790880727c23c2e387be6f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129374712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed6de9127d38f8a91bb4e3baec0e807c69c85ec95b3eb85617c79e5dfc8b6b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:39:06 GMT
ADD file:a7de42b73a4591d75c2ea2f44cdd15d34ce24fa78ca8e57ac62e4fd3ffe2019d in / 
# Wed, 11 Oct 2023 17:39:07 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:12:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a100e11229dc40f9cdcd25e779cd1f10bb500c44c5b9ae24abec0b01f4b26b1`  
		Last Modified: Wed, 11 Oct 2023 17:44:09 GMT  
		Size: 47.2 MB (47166046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f41504078ef3db4155843c88e3eb49d76721ce77692685bb502799200ff810`  
		Last Modified: Wed, 11 Oct 2023 18:18:08 GMT  
		Size: 19.4 MB (19369976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262dceb7106ef55dcd198f1f5e689fd8eb7e9ed58de15831f3c0c75dfd041123`  
		Last Modified: Wed, 11 Oct 2023 18:18:28 GMT  
		Size: 62.8 MB (62838690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:acc1ac9ccab26e28edb954d8e260875e34f182a69fbd41f4c808e6dbbcf9a925
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123464789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e25c02dfee843291189105d29a2af30aca75f3577ae0f728e0f731b908c7bb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:59:32 GMT
ADD file:48b3882ac99c385930d3ac71ac20fda8a1b071b08088814bf1a41054078ecd14 in / 
# Wed, 20 Sep 2023 04:59:32 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:32:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:33:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:219658aab374640dcbab3bd1cbe574955f68e4305522bfc19564d1ce15fed88d`  
		Last Modified: Wed, 20 Sep 2023 05:05:38 GMT  
		Size: 45.0 MB (44955127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e0f2039e0f302927a38df2eb35fc70587db403fbc14273b4fe098c21cb0969`  
		Last Modified: Wed, 20 Sep 2023 15:39:33 GMT  
		Size: 18.6 MB (18617697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba45c0e5519ac44055eac6898a4c8abe790e1be149095e9a8db5eaf719de3e2`  
		Last Modified: Wed, 20 Sep 2023 15:39:51 GMT  
		Size: 59.9 MB (59891965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5d9bcecf36028c9169e4f22dcfb0789845cf6523bd944dd55eab22dd5d4ba9aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (135021557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b7c1249c50f4b3449269dc5abe7ee5c404db73aead5b7fe4b25aff61f441f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:26:37 GMT
ADD file:ae967b7faba93d8a00f97f28b4d720835a90a27fe53b2f278072893f4cdaa8e7 in / 
# Wed, 11 Oct 2023 18:26:38 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 19:51:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ddf19dd473b427de200cf2b123540cd1dce2dcb51aeeb4a1359b7f954dc951ba`  
		Last Modified: Wed, 11 Oct 2023 18:32:45 GMT  
		Size: 49.5 MB (49505530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3234e169293a5a7c5d4630e4d414fffc649556678901730a692ba3b43cd5e618`  
		Last Modified: Wed, 11 Oct 2023 19:57:45 GMT  
		Size: 20.1 MB (20110046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71bac299e7b4e42a2756046d77fc625e1dc632615808cd1ec6bbcc2d48bf4f5`  
		Last Modified: Wed, 11 Oct 2023 19:58:01 GMT  
		Size: 65.4 MB (65405981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c68a447d1f8f8a57fc43e7455aaaabda87e8fe5f7bb01f584d260efac38c75b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138461262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e178f98ad66d50e8c497cf5503dcda5d92cae0a761c41df1e7a2d0905b93549e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:43:20 GMT
ADD file:ad97acda5f74778001aece2a9e280f0e58d2953cf8fdbd4740a049c4a595a225 in / 
# Wed, 11 Oct 2023 17:43:20 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:19:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ce8ed34eaeffdeb7ac49225c6093f421b0005558aedb2b9c429731032d156621`  
		Last Modified: Wed, 11 Oct 2023 17:50:59 GMT  
		Size: 50.5 MB (50485846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f94c813421107d5ab710ec3329c2cd90f1b42da6b64e3d4ea8428fc7802b293`  
		Last Modified: Wed, 11 Oct 2023 18:27:57 GMT  
		Size: 20.9 MB (20886277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f264142306efbcccd3638b5a3b7788249da917c198eab1e97f89a7fb7178050`  
		Last Modified: Wed, 11 Oct 2023 18:28:21 GMT  
		Size: 67.1 MB (67089139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:30a2cdeea3d62c9dd4c0e562792d7aa77f1039eed2ee98069e6905a96ca15261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133031060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fb20dd0a09ce4ea2be6a3e98e09f84f36053e6646b0f5e76821b4998265f5c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:56:15 GMT
ADD file:29bed270e296c5a95f2141f114580e0f25c1040c03609fa632757a8e48ec43fd in / 
# Wed, 11 Oct 2023 17:56:22 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 23:46:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 23:48:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f0d54eafe706e7144ea10a18a0abaa975cb4f7f92fd40e292f388c2b1321a794`  
		Last Modified: Wed, 11 Oct 2023 18:07:41 GMT  
		Size: 49.3 MB (49301729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204f5199336e47ca287487c83b254ad7b0260c5bf568e92c8927077786ee91c`  
		Last Modified: Thu, 12 Oct 2023 00:05:30 GMT  
		Size: 19.6 MB (19593645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf370881cf98cc9a8acbbacf482b90a7a2d7f3a1d96216bd4d6b824f2814f5c`  
		Last Modified: Thu, 12 Oct 2023 00:06:22 GMT  
		Size: 64.1 MB (64135686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d2b8ff9957833a55d2e2a2acb81c8ded45ed8f7cfdf2e9256ef9a8a8e4b699c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145831200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52eb015b31afb09fcb86b0b390e24b827066a43b906b3574e645b2a65406697`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:47:23 GMT
ADD file:24d4df221ce118a8059e0559a8bb2d715512fa6f5b15cd1397dbc177ceaa1bfd in / 
# Wed, 11 Oct 2023 17:47:26 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:30:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:31:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93b578febbe769059c90eaa91e9dc027d172e6088856c2c52dc3e26dfdf01d4c`  
		Last Modified: Wed, 11 Oct 2023 17:54:24 GMT  
		Size: 53.4 MB (53418134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576f9c6569231cdc2bf492ed27ab8c980261301252c26c4d6fcf8dec4fa4de9b`  
		Last Modified: Wed, 11 Oct 2023 18:41:22 GMT  
		Size: 21.6 MB (21644083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86429c6121c1cef63b4087b6359567a0aa3be523db5603dc673793266a48e8c4`  
		Last Modified: Wed, 11 Oct 2023 18:41:50 GMT  
		Size: 70.8 MB (70768983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d56b43941a28de4537dd79f70f50cdf39dd28ebab1806ed5a4fddf6ffabcbe5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135174700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db68d1b36c00eab98e91d36cd34783d7f739259d8c82262bada484ee4590aa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:53:11 GMT
ADD file:7f7d0fe596110ed400f2bbc2fe6edf5716a5a62332062c86009df0df0cc0a257 in / 
# Wed, 11 Oct 2023 17:53:14 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:25:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:26:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f47ccc9a5d62eac06dcd9bcbdf51b3bf5f494156a2c21d58d93d11f5261baf4`  
		Last Modified: Wed, 11 Oct 2023 18:01:45 GMT  
		Size: 48.9 MB (48924346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659ce526b11a7e72319632cba55fb2631fe06f2d042501bcb6fd357be98825e4`  
		Last Modified: Thu, 12 Oct 2023 00:38:24 GMT  
		Size: 20.0 MB (20041463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb87df3b4ff93b8ee1589ac6dee47871cab5b94a7b2b411694cada1830b9793`  
		Last Modified: Thu, 12 Oct 2023 00:38:56 GMT  
		Size: 66.2 MB (66208891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

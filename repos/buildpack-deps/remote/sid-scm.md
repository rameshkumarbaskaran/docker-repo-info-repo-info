## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:7bd1f0e9407a51ad76e5bdf1c64179131a37f5794bb8d82fd892f7c9f4d9c35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b677e93df12ff82852ec41168deb90d09f9f36cf6b0190b4ee4133a26613a7ec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129575885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dbcc9e957ac58b3583e5e1a961760f078620d6a7d3944203d3fc19861f6fbc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:05:41 GMT
ADD file:388f29164844b8493d30bf1feffd1158559ab161886928f977604c10f983a704 in / 
# Wed, 22 Jul 2020 02:05:41 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:09:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:09:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:10:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:babaea2ea26ef0e3e4a90ecc928d26bf25d699e1dcba843f16b8a2f0a153b3d7`  
		Last Modified: Wed, 22 Jul 2020 02:11:28 GMT  
		Size: 52.3 MB (52340330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a37a5f4c4c2303f8d9f818b910d8f9caefdb8cf414a4189c131fe87eac26c2d`  
		Last Modified: Wed, 22 Jul 2020 03:18:23 GMT  
		Size: 7.9 MB (7921724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a136692b9cb363269d4efa1edc43bf0b539b0495b6ab5f8229f02319829642`  
		Last Modified: Wed, 22 Jul 2020 03:18:24 GMT  
		Size: 10.6 MB (10580682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044462b11abaf8b753d1589c7b6b7d8c20479da7e1c06538ea604786fbbbaa62`  
		Last Modified: Wed, 22 Jul 2020 03:18:41 GMT  
		Size: 58.7 MB (58733149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:04399be3460b6dc66a8549c93731f1cb0ed6e6951a9a0e148844eed24dcfb0fb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124158455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd1605759b74788a1c581069aacfef4591b3bcbed5b09c3566a7f0248725fb6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:53:26 GMT
ADD file:72bf1dc350aa2201a007e97d34f6d8ae4edadbfae65004d87b70d8bde1ca66f6 in / 
# Wed, 22 Jul 2020 00:53:27 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:46:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:47:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:49:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3868d999f42cbdf70764edb51ce2454cdb2f061f76b646ca6b109e3294cd106a`  
		Last Modified: Wed, 22 Jul 2020 01:01:42 GMT  
		Size: 50.3 MB (50268734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f11ca48a92528806c80b7a1add7e641a3bc25a3283d24aebfe4773c1479ab72`  
		Last Modified: Wed, 22 Jul 2020 02:06:16 GMT  
		Size: 7.5 MB (7501174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b474db4689f860236c9af7f7821d8ec3e4df8bf30bfb7b4ae53cde9f435eb3`  
		Last Modified: Wed, 22 Jul 2020 02:06:16 GMT  
		Size: 10.3 MB (10266925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce30b915c952ab0005a807bbc2ae90c61bf483b7a5dce8c903239a7cceb790d0`  
		Last Modified: Wed, 22 Jul 2020 02:06:43 GMT  
		Size: 56.1 MB (56121622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9f10a49002e4952b5a00c15a1c0084653d1afb58c98f08b10a61bab15ed14f77
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118915326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438d38d3b89ac4a92da153a2f11e25019c509af577fbe9becc71a501225a2fda`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:04:25 GMT
ADD file:f137ab200a6655933430876a9a0f3c675ed39dbf4a73be4750579b0c66812888 in / 
# Tue, 09 Jun 2020 01:04:32 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:59:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:59:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:369ddd165e2326d11cacb52bac2afd8d2277bc9506399fb693a5a5eb336716ee`  
		Last Modified: Tue, 09 Jun 2020 01:12:30 GMT  
		Size: 47.3 MB (47326325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ada3ce7a1b468f31af8a1aa9f083d4521fbeedd0d46757dc5d1f97c49ebf17`  
		Last Modified: Tue, 09 Jun 2020 02:13:48 GMT  
		Size: 7.2 MB (7243269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab399397acddc3f7ce3a847871519a272a15f91ee26bd786a485bf8a41dc870`  
		Last Modified: Tue, 09 Jun 2020 02:13:50 GMT  
		Size: 9.9 MB (9916653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfd7032d9f8bf51476a074156f4ebd7aa42e52d8e07b6e899f787d2eb56a14b`  
		Last Modified: Tue, 09 Jun 2020 02:14:15 GMT  
		Size: 54.4 MB (54429079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d967ce10aaead3ebf6acd885954ab9a86cf80edeb379d9e0ba00ea8083a3d75d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128016452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12b3a4a76f67340c19269f59d12dd7ca041a7a1dbd27bfd35018e1bf84a77a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:14 GMT
ADD file:0f4a1ab6b889d98f711b241dde31787e633494e233067fe98dce73de73c2d7f3 in / 
# Wed, 22 Jul 2020 00:42:17 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:21:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:22:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:23:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3af651ddf153ddf8519b20c192d158afb60045252366ddc81e15c938b792982e`  
		Last Modified: Wed, 22 Jul 2020 00:48:41 GMT  
		Size: 50.7 MB (50699554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cbb2a684c92e31711be180ca45ac19643d88c12a51b2ffb58b6f120bc5ded2`  
		Last Modified: Wed, 22 Jul 2020 01:37:00 GMT  
		Size: 7.8 MB (7796374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdf66380a30dc7828150f57df61c812d1fd653b195e8f5d57dcfb885adedbf`  
		Last Modified: Wed, 22 Jul 2020 01:37:01 GMT  
		Size: 10.6 MB (10588039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74e3c1552e3888e748a1827b0e10da06ab4a4d5d05b69a591c812b9a0a1dcee`  
		Last Modified: Wed, 22 Jul 2020 01:37:26 GMT  
		Size: 58.9 MB (58932485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bf880e8b17890234114e3d734942c366016cc9def00d202f2b409e7847c814c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133188902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e1c55f737ea29927f9ec57f17c2b0b59f53965eb6ff5b098464681bd9765b7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:11:12 GMT
ADD file:1c3529ea5c695a0705497b4510edaf2034b3d29a608dea3db741a4298a117d33 in / 
# Wed, 22 Jul 2020 02:11:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:32:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:32:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:32:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:32126ce0c55cb16ee9848f6d067e47a287f981a106ba123e3f2590544677f0e6`  
		Last Modified: Wed, 22 Jul 2020 02:18:12 GMT  
		Size: 53.4 MB (53433577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d9e403cd592ae856cb4192dbfde1073d62172846377a957e99aa1612f15c17`  
		Last Modified: Wed, 22 Jul 2020 03:43:32 GMT  
		Size: 8.1 MB (8099028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23d35b0ead0819c716d1b9d778e65755014b69dde5807f1cf3a6c95a4a73dbe`  
		Last Modified: Wed, 22 Jul 2020 03:43:32 GMT  
		Size: 11.0 MB (10960296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a4001839767608296f1e2286d481abeca1f071afedceb18874a8f61061f2c5`  
		Last Modified: Wed, 22 Jul 2020 03:44:02 GMT  
		Size: 60.7 MB (60696001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a34a1ab183c41c55c6d1a85f6bdf604ed44f49f13e83893948d6afe406399048
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126567225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cbaceb0ab4fbbebd520594e008dd85c6a8c7621dec0420ca9811c1792f90dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:11:18 GMT
ADD file:2c0e5d72dc26223a4df660e91acd4c8c70d1b0ee1139c92fb9cb3f041d81bdc2 in / 
# Tue, 09 Jun 2020 01:11:19 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:56:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 01:56:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 01:57:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:78e0a34f3ecd34b89d20cdb0b915427acd1691184f4f7649f816759737ddb842`  
		Last Modified: Tue, 09 Jun 2020 01:20:19 GMT  
		Size: 50.3 MB (50264875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff174bb9582ec89056fe600d1820b6c6e7445d74e52537dfea39a4dd2b4324e`  
		Last Modified: Tue, 09 Jun 2020 02:14:03 GMT  
		Size: 7.4 MB (7447530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a44807d6533dba987e8712d4b69466283e5bbe760298ac86ccbe1ed4ea542e2`  
		Last Modified: Tue, 09 Jun 2020 02:14:05 GMT  
		Size: 10.6 MB (10598855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46849a421d1ddb3755126f8b58c93389f656c6533dd46480416ce5fe6af98d6`  
		Last Modified: Tue, 09 Jun 2020 02:15:04 GMT  
		Size: 58.3 MB (58255965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d639746073589cca1f4559b903b7b815b28c51ddeeb59ad263a011f45a060002
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140093207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69785aea7178aa8c1d79a63f8c01c7d9648b49e63aa085ffb75848f8fec1f92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:47 GMT
ADD file:04723d2d8de7d77c2c146c6af521e4a3124ca84c794e6ab9811528805e9f8a16 in / 
# Tue, 09 Jun 2020 01:23:54 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:13:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:13:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 03:18:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57bdb75510f480914b31ba736d52f2bab13d126b2808f87359f0678e25b38717`  
		Last Modified: Tue, 09 Jun 2020 01:33:30 GMT  
		Size: 55.3 MB (55274450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c7f2f7dc07ba0a3435ca28dca3bc46cfbf238c2fd76e208d4b394f7a1de537`  
		Last Modified: Tue, 09 Jun 2020 03:46:48 GMT  
		Size: 8.3 MB (8346012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a7d75882c1ba6c6a4c7b499aa5bd492b3bfebc6670ca2c2c3dac6675be974`  
		Last Modified: Tue, 09 Jun 2020 03:46:47 GMT  
		Size: 11.3 MB (11326929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a723bc74187577bcfba79dff09ce9808d81478c829672c29f518b83f20218c`  
		Last Modified: Tue, 09 Jun 2020 03:47:41 GMT  
		Size: 65.1 MB (65145816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:365f3ea1e3875e3cf51824c5064130c3861968f56e3ea54b788fb465afa9ae87
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126797150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a0e0b128bc5454f2b279e98cc63765db2c515c9be565c2f0a421d8d4515557`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:53 GMT
ADD file:7128ed6ae7cb1b0852460f972a83bd593194b874b85235f9646a9357791b1514 in / 
# Wed, 22 Jul 2020 00:42:56 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:08:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:08:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:08:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bcd13ccd7a5817e6de826ec69afa4d569b06c9f7beae2283db3d6ec9bf769fab`  
		Last Modified: Wed, 22 Jul 2020 00:46:01 GMT  
		Size: 50.9 MB (50903176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a0892473ebc7a0e196a8c4a4d81834a4ab9b414220c38331720f27f28c42e3`  
		Last Modified: Wed, 22 Jul 2020 01:13:10 GMT  
		Size: 7.6 MB (7590034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c697dc02560deb46fb2199992fe714a6a4f7df7f834fec55dac3ce014e699dbf`  
		Last Modified: Wed, 22 Jul 2020 01:13:15 GMT  
		Size: 10.5 MB (10456221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448e86d0e43033e3351015ecd9eb32269af3427df81d692b5ae69e826ae4232a`  
		Last Modified: Wed, 22 Jul 2020 01:13:29 GMT  
		Size: 57.8 MB (57847719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

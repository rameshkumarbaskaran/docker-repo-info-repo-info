## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:b1c03845e9465de507f5d6bf6eec82945e8f5c3a28b94e49e012786c04e48c2e
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1a9f55f71143aca2dd01ab0a365e469c3203543ff5194fb519ae5183e80af5b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72602212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60eb182876824d03f6581e048ad13b41a5f8350427642eb5671f68d4e499f3be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:34:16 GMT
ADD file:f1c9279b9eb3b88b40c4958324519afa81185c0383ed51d5138ebf2a0eff6d7e in / 
# Tue, 12 Jan 2021 00:34:17 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:59:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:abc50f4e181143f18afce1a5282914e00abd896a798d96f7514e728b30f0988d`  
		Last Modified: Tue, 12 Jan 2021 00:41:42 GMT  
		Size: 56.8 MB (56800959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e331862b1a60a0f0273b0162c4d7c2b7bbe7a7b631e4a7847799daa4d3d614ac`  
		Last Modified: Tue, 12 Jan 2021 04:07:28 GMT  
		Size: 5.2 MB (5151057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d621cee81c84693094bc652651e3d6789dd350ca0bd2dab361e7677761ef3a02`  
		Last Modified: Tue, 12 Jan 2021 04:07:29 GMT  
		Size: 10.7 MB (10650196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6d45a8d5cdbca349dfaba945341c99017175a8475fbbd0c1c984d2bae1938d6b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68593044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb9d6f862cb2e73fe6f4e74bba8eb7bc977ac1139bad31347cd22e916d6ab62`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:53:02 GMT
ADD file:8a666bde5248b085708640c42b93c850be2265e6a4db5b59c48543ddc8ad0148 in / 
# Tue, 09 Feb 2021 02:53:03 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:29:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 03:30:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3b915a09886212577bb3e4444d6bdc576b17746fa48c0239c56c968d81127e7e`  
		Last Modified: Tue, 09 Feb 2021 03:01:34 GMT  
		Size: 52.3 MB (52324134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c594f7d69077392315310232b92354eaa9652361ef5e54825e4aade3a67e2851`  
		Last Modified: Tue, 09 Feb 2021 03:41:51 GMT  
		Size: 5.1 MB (5053985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195684c55108e3d23d6b03082fa8140c8859a738918fed4410211cbac9dd2ee6`  
		Last Modified: Tue, 09 Feb 2021 03:41:52 GMT  
		Size: 11.2 MB (11214925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e356e5ac5188d78a70152f60bd21544b0644f70f6015bfe55cc9e61ed2b8c6a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66799885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726f975af02037fc20209897bada81c0761bc91cb1dc67aa9f810db4a80523e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:03:45 GMT
ADD file:a459be4601ccf608a415f6ce53ea885edd1a9a10ba1205f3e8493e277e6a7faf in / 
# Tue, 12 Jan 2021 00:03:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:18:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2fdfe7e087b5c823888d02320fcca90d4debb7a7d0ead6a978abb2de6acbbc00`  
		Last Modified: Tue, 12 Jan 2021 00:13:47 GMT  
		Size: 51.9 MB (51902171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0592e7529a748d8d0e52ef640addc32dcea717609f5c656e4399e87bdd4d9db`  
		Last Modified: Tue, 12 Jan 2021 01:31:29 GMT  
		Size: 4.9 MB (4921500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeb968aa1e6a404fcd0a89cbc65878f592c4c4067725853712ca4d00c1669ce`  
		Last Modified: Tue, 12 Jan 2021 01:31:31 GMT  
		Size: 10.0 MB (9976214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:82856d2e3fc65017f1ce3081d0afc61f78a1c72f10e1443febed08cf3f8b66f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71333978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017a27734a612b9e623d0d5b0b809b87a033a3030a7a92f734d6f17b98c6f28b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:42:27 GMT
ADD file:ba9ce45e2c6743713798982615c806de6db6d8fd9a0d8734c8a69d80f3959eb6 in / 
# Tue, 12 Jan 2021 00:42:35 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:27:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:27:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:01dba80e9024f3ac734ae74a14f2997ea67918b4de57aef778ed839a508baab1`  
		Last Modified: Tue, 12 Jan 2021 00:53:15 GMT  
		Size: 55.5 MB (55537816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8417d785c975de855b94a5c17e92b69107a02149bbd61ac1b6d1355d80b32549`  
		Last Modified: Tue, 12 Jan 2021 01:40:11 GMT  
		Size: 5.1 MB (5140360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34511ce04354db34bda0eb613bcb4990a4e262fe16307861b007423a0033c44`  
		Last Modified: Tue, 12 Jan 2021 01:40:13 GMT  
		Size: 10.7 MB (10655802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b3507e770ef2f7adac057d8e9896b7fe24b80960aef211a88e1873f52c4bc501
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72995746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d5119fcbb7587355532e25debea3367aec6b0382da887f4325f0cedf0a531a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:17 GMT
ADD file:d3470c47b61c2df201e9fe51e9dd198c152bae2eba84df9bbfcb591bfb29502a in / 
# Tue, 09 Feb 2021 02:41:18 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 03:12:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:14213d5e86eb4e1e7c43e3524429378786d8674960445945ce050c587b83884f`  
		Last Modified: Tue, 09 Feb 2021 02:48:13 GMT  
		Size: 55.8 MB (55792012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2cbabcd8ca39fd619ad8a109f0fe5eea442c6afefd108f3d2a80a49be04524`  
		Last Modified: Tue, 09 Feb 2021 03:22:39 GMT  
		Size: 5.3 MB (5271392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cacdc0d9d1ac9a69c2a336a43253fbfd3737321bf5e32c6f9ee54465cb2087`  
		Last Modified: Tue, 09 Feb 2021 03:22:40 GMT  
		Size: 11.9 MB (11932342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:90d9ec6269ba7bbe838cebf1a3f20e4dfce6db2cde4d238c2c683bf1a172c35b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70819358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee50d214753a082da0974f08ca77722e5af2f3d13867b8ee37dc17dcb6f2fae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 01:16:48 GMT
ADD file:7bfb9d47fcd2b6a553e5be3b702d34f192cd8798dd3982fc6e6e77479f0affdc in / 
# Tue, 12 Jan 2021 01:16:49 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:54:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:54:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:24a4375dbae3deddd016bd6d4372d219ba5fe4102ce643c06dd57677bc882654`  
		Last Modified: Tue, 12 Jan 2021 01:24:08 GMT  
		Size: 55.0 MB (55046139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1447ce8a926cf7692ae55e3f2edb9925e5b11be684c7fd68fe2a385a5b812880`  
		Last Modified: Tue, 12 Jan 2021 02:05:46 GMT  
		Size: 5.1 MB (5114938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfd08658a76a7d3cedb6b4760f760c0ce830104bb77dbffd92228d4d0448730`  
		Last Modified: Tue, 12 Jan 2021 02:05:49 GMT  
		Size: 10.7 MB (10658281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:da824faabb1cf2483f9dbad980dddf2f52929401bd4acbec3c9d00f8ba02bbf7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77871932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601396709b1c2887e79a72d7aae4ba82e979288ce9e936a41faffeda3a37170f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:40 GMT
ADD file:f289d6dea557bc0563fd9221c4857a56c56bb52d981a3ec90ade2f1b76980794 in / 
# Tue, 12 Jan 2021 00:25:56 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:21:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:22:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:594e638823d3ce0bbedac4d1aebea00f91d28a98d7b98ca680fd90e4c0fc8850`  
		Last Modified: Tue, 12 Jan 2021 00:34:46 GMT  
		Size: 61.0 MB (61048727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a59148553af7496dfbc29a5704e94338ac15ab898a646dcbab32076a5f00f3`  
		Last Modified: Tue, 12 Jan 2021 02:40:41 GMT  
		Size: 5.4 MB (5400394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45a065f7b5587bec16714bce093a4075fb92b291238fee1bae7d383a16a4052`  
		Last Modified: Tue, 12 Jan 2021 02:40:42 GMT  
		Size: 11.4 MB (11422811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0d24a64d963e5352a86f397b79f562b3ccea65c3594411b624cc74950e40fda9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69600752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abf3a26f1a0f83cea68fb1550140f314d137be137829cb4da272f1d8bfaa087`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:21 GMT
ADD file:6b632451421e7f0411db1927a48466a6b3bc2f7e10a53b00a06799fbec279bdd in / 
# Tue, 09 Feb 2021 02:42:24 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 03:07:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3dd2606d37926391a1e8153ffefee2aaccae04bd432c37c97187880ba3ed01ea`  
		Last Modified: Tue, 09 Feb 2021 02:45:45 GMT  
		Size: 53.1 MB (53060083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd34d7430306d4b5f56a7983d33fdce7c2f86209989ddeacc68e07134aef96e`  
		Last Modified: Tue, 09 Feb 2021 03:12:40 GMT  
		Size: 5.1 MB (5127742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b9a7cd753b983b2730894814680d1c0b77e08d7affc85900856bd036f96806`  
		Last Modified: Tue, 09 Feb 2021 03:12:41 GMT  
		Size: 11.4 MB (11412927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

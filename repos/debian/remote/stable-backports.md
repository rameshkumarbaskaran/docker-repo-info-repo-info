## `debian:stable-backports`

```console
$ docker pull debian@sha256:96cc803062da3d5d20cb841e58da3cc4d6d3eb9adeb54ee2da3ebead99e11f27
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:bf6b145efa1b559a15fb773c36016cfed6239d0a95f01d6c017d23f47260becc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49582256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9ed9cd55289e485f8f5f6291bcb428a03f1fa8616d94e751db1836f2ee64aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:47 GMT
ADD file:e4b5d0e7045f4d28d34e728d72d11e967751a1854c3b9e60811be54b1cfb2db4 in / 
# Wed, 01 Nov 2023 00:22:47 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:22:51 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ad1295602a0fc01fa0c6a8477bea89b63e96d9a707a9ac8c72a41bc2ac640f75`  
		Last Modified: Wed, 01 Nov 2023 00:28:57 GMT  
		Size: 49.6 MB (49582033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8201b6d6593829ec85e8b919775594f3d66efba02128a3bcbf8e0621318a3d15`  
		Last Modified: Wed, 01 Nov 2023 00:29:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:06f13dd9a74778de0373e7123c878b4fb277cb6b6dbff3b3eccc18ddbdc6aa21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47355853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac80b96b639327a65aebd3e38f5621ca8f6e40b2ae660b386cb4adef5ae271ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:49:24 GMT
ADD file:0423c2a6d7a31e6d3c50e52dceb01f848eb00a9c970206d97099dd187e209df5 in / 
# Wed, 01 Nov 2023 00:49:24 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:49:27 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:13fcf10d7d5dbd23a7cfdd753865b21db7524828f88bab2a3ee0d785e8fa8f78`  
		Last Modified: Wed, 01 Nov 2023 00:53:38 GMT  
		Size: 47.4 MB (47355629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f92132bb98b3ce24edefeebc8a53b3c2de510eee2456a38565eb98f94369682`  
		Last Modified: Wed, 01 Nov 2023 00:53:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8925badfecb47ba4323cbe26a815d9bc58f027e8440e02877eb4bccbbfa56de3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45179665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c746426a454d54392d7541c467ab4bf82c98a431f127c29062faa73b9dbda86c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:59:31 GMT
ADD file:ee00cdc0511833ca5bedbed613b2387c99ee4107a16fb2731ce6bdea2f1f6718 in / 
# Wed, 01 Nov 2023 00:59:31 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:59:34 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:320517144d6665fe34299e208b031c59d7de07a024eeb24899accdc8b64e6526`  
		Last Modified: Wed, 01 Nov 2023 01:05:48 GMT  
		Size: 45.2 MB (45179441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f016d9ee1a5ba43cf3f1054b745058cf981ba8359f289d4dad50a4850cb854d5`  
		Last Modified: Wed, 01 Nov 2023 01:05:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b270c7efa4ab105fbe5b7071b66f65f2d5e3543815e7a01e40faa3021c864c56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49612880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de2dbc256ac9b29f48a722b13207a3b44e6029abf521066783a24ddf1005f1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:57 GMT
ADD file:5ae606dfe6c86696bf339baae78b452a9ab14148ce79917d7910c6f4409fb8a8 in / 
# Wed, 01 Nov 2023 00:40:58 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:41:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:315f44ac156baefadff78fc8bc8a8a54964367dc79384cc2b2786c602dd062a2`  
		Last Modified: Wed, 01 Nov 2023 00:46:12 GMT  
		Size: 49.6 MB (49612659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983eb873957ff63adeb1906fd4672d8dc3f780ff244183f7cf7e2a2e8607a4a1`  
		Last Modified: Wed, 01 Nov 2023 00:46:21 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:911773b8a3debee01261d5281a4c453e8c16b0aa1eb6e588b7ce4faeb26e195a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50600227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087cc3c5e5ccc87c33605fed929adb75c3fb1dc61ce5a61efde3c2a46afe83b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:50 GMT
ADD file:507f55eb8000f3d795c330843f92d5de3a36f2e727eee9e66a30f71ee63bfe61 in / 
# Wed, 01 Nov 2023 00:40:51 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:40:54 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0cd75ed6e2a79a714d0e15266ad3d2656e2b3ae927c0e03bd8b085ff8f329709`  
		Last Modified: Wed, 01 Nov 2023 00:47:15 GMT  
		Size: 50.6 MB (50600003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e560f30a736904b5d042e61d80d6183f373209221e330b58811c5acce56635f`  
		Last Modified: Wed, 01 Nov 2023 00:47:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:d2125076bcbab6144c8bdcce972fae8033e659ebe749e5da0ef7c18a362897fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49569045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d9bb7d5a9a78b85bb9d1727fbabd411d9ed7a6753fc5bf2079551f3c75ba75`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 01:13:12 GMT
ADD file:7ba9b4448851210b7d5b755ad598d9c951ae8ab17ef57efef68bcbf3e6dc54b6 in / 
# Wed, 01 Nov 2023 01:13:17 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:32 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cdf50c77e558a8ae38b324d4a5f2a0d81bc75c0d5ebba9d2414e52781061d354`  
		Last Modified: Wed, 01 Nov 2023 01:24:18 GMT  
		Size: 49.6 MB (49568819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3a2ef7930a62e2a347012e105abd6cf5677ea32d2c15806d438143d6165ed4`  
		Last Modified: Wed, 01 Nov 2023 01:24:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:069e16162daa4762f7010954b60a64a2c2c344574de7f9353df1db309fbe956b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53575556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d741ec3dd24e37ce7c77dbbe102f5ba99555d5cf88771132a636dc19c90a537e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:23:09 GMT
ADD file:dca11fc5dd30c20682713d803d36b05130ae41d1b48c35b843e04c6f1bf63917 in / 
# Wed, 01 Nov 2023 00:23:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:23:16 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ce5d31a34131a06b953c32def4fcc3b9fd1d41301d714f9e988763cfd447dfa1`  
		Last Modified: Wed, 01 Nov 2023 00:28:31 GMT  
		Size: 53.6 MB (53575333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36df6f9afefc11fe6648ad9e383a84fed35daefd7083aa66aae8368f4a567f1`  
		Last Modified: Wed, 01 Nov 2023 00:28:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:5e5287a1ba6d7913e4e1f96ec57afb84ab40948e2e5d36036d93233ad193ad77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47943451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f21f6dbda2b982094040b79817438a1f199ad0af7fcedbf148f87e1f3fc66ae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:44:30 GMT
ADD file:6907d5589471113dca1a4a24a8c03ef5a77261b068fb7a15d7df28c417eba1f9 in / 
# Wed, 01 Nov 2023 00:44:34 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:44:42 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:717a78911c4c233c141e57612cb68d7ab52d2431d0186e7ace40fbbcc55705bd`  
		Last Modified: Wed, 01 Nov 2023 00:49:47 GMT  
		Size: 47.9 MB (47943227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b12f863ab924260be285f391e95bad636c4f5828b4226dc806f11dedc89e12`  
		Last Modified: Wed, 01 Nov 2023 00:49:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

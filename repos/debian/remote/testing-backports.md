## `debian:testing-backports`

```console
$ docker pull debian@sha256:e1f326c6cfa8803ea3b914d140eda3a33be01b795e4756d7616c1163b9fb87f5
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:0f2c53a43909c1e8d62ad31b3b302648caac571e62bca02423e8d3634def568d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54835967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46ba9fd417d55f003a891059f94e1663295cbd0056c041ae637899d338b67aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:58 GMT
ADD file:f7ba3c021cb8d4754b008c0e16ed267d3af0e2b300963191be16d6d0e46312f9 in / 
# Fri, 12 Mar 2021 02:22:58 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:23:02 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e084fead077cfeb7d41648a77bc726866fae51276550348d1337cad9637493ef`  
		Last Modified: Fri, 12 Mar 2021 02:30:52 GMT  
		Size: 54.8 MB (54835743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bb6e524c3a2b18347757d4470d6adc4ae28430a36efe12efc8514f23798550`  
		Last Modified: Fri, 12 Mar 2021 02:31:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:fd00499e7e74bf7ba64568b00f3e5594e1d415753952953dfc6df8f07bc12862
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52404639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a73d443b535fad1b132866f9e47f8ff97a1489318d88d3987526ab9af25d5e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 07:56:26 GMT
ADD file:1f0d51940060ad5be8305835a634d086ebd15deb3ed300c73daf68f5d1a76c55 in / 
# Fri, 26 Mar 2021 07:56:29 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 07:56:39 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e958077b175ca4c4330a7ec87a9f51fb1a7222a2c0693c69b34198734ec69bb2`  
		Last Modified: Fri, 26 Mar 2021 08:05:01 GMT  
		Size: 52.4 MB (52404415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab611f0599083736c1aebe57156b717f1a597f7b3b948dfcf65560c6fbb1ccfd`  
		Last Modified: Fri, 26 Mar 2021 08:05:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5a40ce3f64368446944d4b277a64b84b36673f6123d3c8995b5ababd51eaf44e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50074276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586fad6099761261f2f81b996ac44ee7ba9ac6fc0719cbd9af9069abb8fcda0c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 11:23:10 GMT
ADD file:699c64d1733568708c6338c1f05e47fc3750ff3d0153193cdf9a6362a9595b80 in / 
# Fri, 26 Mar 2021 11:23:14 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 11:23:25 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2510c5d7e5afd3b6e15d9a3ca9fd39cb9ed6aaeb830a99e794bf0ea2784f40c1`  
		Last Modified: Fri, 26 Mar 2021 11:31:59 GMT  
		Size: 50.1 MB (50074052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06ae4cab0e3808005ca82c523ac7cbb02023bcea196297e074fc8b42f561c7b`  
		Last Modified: Fri, 26 Mar 2021 11:32:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f8aefbbc490bc86bb24f7b066a30b06efea95aad0cb233afd78203be6aee0642
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53521373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c262e4faa3871cc64af48b8293c2d022ff104e35ef8d7023ecb57ba7db519e8e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:57:43 GMT
ADD file:22a6957379e9e833185367bde98358ddb39fa0d834fe1ef9b10d19361a9f52e0 in / 
# Fri, 12 Mar 2021 01:57:44 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 01:57:55 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e1386d46900c29cd2b6bae92f6d6d5f608591bc0a86997705f2b1208414bd7cd`  
		Last Modified: Fri, 12 Mar 2021 02:04:37 GMT  
		Size: 53.5 MB (53521148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492576baa1aa1abab3ef98f18b41fc9fc7834f42e3243ad05dd9f6c8f65fe91a`  
		Last Modified: Fri, 12 Mar 2021 02:04:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:41487d75e0eb248c5f6abb746f17586b65a2d1a9464ca15f556f890377d81a88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55847737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b6456de9384218947887545e26d13215cbed65b7d94e01fde3d42e2b91fac4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:47:19 GMT
ADD file:bdca387a35098c10fce82b6222779f702f7297a8d8280064fbae9e64b561ead6 in / 
# Fri, 12 Mar 2021 01:47:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 01:47:26 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5c71e094894ce7f3b31cfba339088fb427927e0943742620636e85f2e769f828`  
		Last Modified: Fri, 12 Mar 2021 01:57:32 GMT  
		Size: 55.8 MB (55847517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d563c2a31ede357fab0bff11a7a2f74751b2efb0f70f75a75bf1a57dd06332de`  
		Last Modified: Fri, 12 Mar 2021 01:57:44 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:3ac39b801c23f324f12377acebd73a690aa85e0da360d329a325f5001693d472
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53128960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a575bbda06efa3127281f374b79ee0251fdfb2524018a54364c3477b3553dd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 08:11:55 GMT
ADD file:0ddc16d08c0ed8a6219e588e991a0d1456d4950b56aca1e0c650a26f238a2d00 in / 
# Fri, 26 Mar 2021 08:11:56 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 08:12:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9a58b4ed9116dc08cc6097c9827ee4d787d33e545d84c04ab503c3b1a81aabca`  
		Last Modified: Fri, 26 Mar 2021 08:19:56 GMT  
		Size: 53.1 MB (53128736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f479319c37889eb723ba8009d88d1118aed034343f70c5b50484a7df363724c5`  
		Last Modified: Fri, 26 Mar 2021 08:20:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4bff91923014cecaed657c65ccb0ae651e0c3645483334557cbf43612c6076a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58746771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0691ee62ef9578a6688ef97dd3668c8362ef3c4928fa98af1975db616d5af200`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:35:13 GMT
ADD file:f51fc83967d32c95b96fdcd3bb01770be009f079b97ead429f2d914a4463e9af in / 
# Fri, 12 Mar 2021 02:35:25 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:35:51 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c73595d876be0af8bade8ed657ff774b66282afd5232e3d0803c40419cad1267`  
		Last Modified: Fri, 12 Mar 2021 02:53:04 GMT  
		Size: 58.7 MB (58746547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a323e2e5f76a31fd3e2cc373d6c2bdc6b0fecaae7fca11e6127799bad7cd7960`  
		Last Modified: Fri, 12 Mar 2021 02:53:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:ef418b88caebd9fba6a99c5be72a43ce984e9b0b3e3bc40827b355c65723ce99
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53147853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd12d1453cc81b692b0b83b449e1d464ca139244ed2674a88f14b4af4bc3c168`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 10:55:05 GMT
ADD file:c68277f5942da894b87824e7be5e490cdc087530373096bc568a709716c8bd7b in / 
# Fri, 26 Mar 2021 10:55:10 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 10:55:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d49851850d45c1c8e424bfcbe79b41751f17923fe040a5364ea54e2ebe4dcbda`  
		Last Modified: Fri, 26 Mar 2021 10:58:54 GMT  
		Size: 53.1 MB (53147632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e644edbc0b49753ba4944783fed6dfa6a208456a4dcf3ea44f75bd6fbd278e`  
		Last Modified: Fri, 26 Mar 2021 10:59:03 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

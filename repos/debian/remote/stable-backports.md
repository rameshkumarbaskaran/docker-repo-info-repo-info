## `debian:stable-backports`

```console
$ docker pull debian@sha256:383df6bb9b1f641dde4f24f4ae3948e00a469c7ce8ddec45d7ed123eac4dac1f
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
$ docker pull debian@sha256:ac790459e0ed53ca7bdb054d2b1fae28e4c95e2c1a9d6edf26133db21f7c9292
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49557400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368d56b3969cecc5f964eea81d55fdc695a834ef4110661e8bb3dabdf7123f21`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:22:44 GMT
ADD file:3b4850bdbeda4f6d961dfd39270718629c9294e17fb6544aa1d589e267c15598 in / 
# Thu, 07 Sep 2023 00:22:44 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:22:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6a1c5bff52cff72e59992ac0a97323470e2ba408b87d78984bd278e9cdfc4273`  
		Last Modified: Thu, 07 Sep 2023 00:29:04 GMT  
		Size: 49.6 MB (49557178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bcfa9b77e759a69099456101efbd22dcf23482204f13f600f465efcfbba955`  
		Last Modified: Thu, 07 Sep 2023 00:29:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c1f07d71fbe30eee6f9815354f333faecebae2625087b17abf84f4381cea1265
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47415215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d52b1365c190c01e79023eaea411c355565736a77d1c53b6df7ae5bacc3534`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:51:25 GMT
ADD file:53ceb96e5672e219aca6daea64bd7cfac4dd9ef4811d93e8f1425341c0b5143c in / 
# Wed, 20 Sep 2023 00:51:26 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:51:31 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1360ba697847ba50544626e2fdf28d6189f0906348cc31ecb1f8ae807f15a790`  
		Last Modified: Wed, 20 Sep 2023 00:57:23 GMT  
		Size: 47.4 MB (47414993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82384d58a25e38f5b3c0107a834b251df6167c28353743617ced7d51385a58a6`  
		Last Modified: Wed, 20 Sep 2023 00:57:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b9cece93d0aeab6fc7177ca62c73b11fdd9a557b96237de5c3b10ff308f3d646
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45233453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61b005a40bfe183974608ea9bfc7c0171155cde07c45d5b3995b930b431531e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:59:44 GMT
ADD file:de1cee8ae1fbc859725e0aee9a6c96b5319fc347f43f1a2c6d6f222639d7e022 in / 
# Thu, 07 Sep 2023 00:59:45 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:59:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2b21511435baa8f5c4133af9b49f91568e4bed6fc53b194df341e968994bfcb9`  
		Last Modified: Thu, 07 Sep 2023 01:05:48 GMT  
		Size: 45.2 MB (45233231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98df0876940f27bdb992bb68388dd121f9ebfce177774f6c1725b53ad639ba13`  
		Last Modified: Thu, 07 Sep 2023 01:05:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:876a17b9df71b58c121f48701c7afe6e0a9d3e75b252fcd647e9860b1346faa1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49590973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bd50674f2af6f7986bfeee1bb1c65a941df964c89acc6d3cf384e586770f10`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:40:54 GMT
ADD file:f8e8e784b14494b10e08820e70397f805d30253f947ad90ab77f90bf0fedbe98 in / 
# Thu, 07 Sep 2023 00:40:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:40:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:355c6e63f919e54c9f765cec91f5c0585d31782fce7a36951973a3c579f3271c`  
		Last Modified: Thu, 07 Sep 2023 00:46:02 GMT  
		Size: 49.6 MB (49590748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfd0e8fdc202178b7ee6caaffcb81d90d53ed678ce9ba54d7df1337ba1194b6`  
		Last Modified: Thu, 07 Sep 2023 00:46:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:24347bd56442601a884eaf625cbdfe0fb4ca25e298ae4e0c776e395434f7766a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50569192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd2fc574aebdd8c4223b3ab84a09b64b3005ae3136a468e910d6cb8487f9eb0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:43:55 GMT
ADD file:a4f2fa3e98a8185764341fd63ac3591952b23182853ddd2ebf84ca98a3169ebf in / 
# Wed, 20 Sep 2023 00:43:56 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:43:58 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e4737eadb65c1f5f944f365a8626d47a469de86152a9f43f1178dd43ee1507fc`  
		Last Modified: Wed, 20 Sep 2023 00:50:38 GMT  
		Size: 50.6 MB (50568969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461c1d5dda8eb5ef020bf7a9130f1f9080afd3804c54012f114d2c13e5028390`  
		Last Modified: Wed, 20 Sep 2023 00:50:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:447136ca08b9405d6e7d2ac255bcbad8ba7736217142fa7408aaf595fc45f448
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49542263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2a4fa8470a9d0419347e30b1bd5c2c3778a740d49bd6730821cd38eb9ac5dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 01:13:22 GMT
ADD file:20183d5e516d5dc709ea3e532b4ee0a5e4c02e4bd4316161868fc646490f7ebb in / 
# Thu, 07 Sep 2023 01:13:29 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:13:42 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8ada4ee02d74ba726f0f39147f4d37a61709382c69d77d443e18df0e1941e0e6`  
		Last Modified: Thu, 07 Sep 2023 01:24:46 GMT  
		Size: 49.5 MB (49542039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92e7274f6e984cf6ceeb85416ad3e3bb88f9330908f4c5755fc600a11aa8b85`  
		Last Modified: Thu, 07 Sep 2023 01:24:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d42576ff152c81a37ccfdbbc4ddffeb7bfaac739004f3d99a73539102d7f85e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53542988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3cf09e1ccccc7cdadf5ff2213f6da461d73e9ef71d3be2f8953586334acf59`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:19:35 GMT
ADD file:98a533946d5ec81f51bed0170ddbc76778b25d23606300ef1b71439482282b88 in / 
# Thu, 07 Sep 2023 00:19:38 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:19:43 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c66f8f37cec4a11beaf7390ea808b815dc23493bee08237c260705d7f08bb452`  
		Last Modified: Thu, 07 Sep 2023 00:26:18 GMT  
		Size: 53.5 MB (53542765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155a4e8be8cbe542df6a13987febe75cd54b0524141836b517f6cbaed184295c`  
		Last Modified: Thu, 07 Sep 2023 00:26:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:1ae8907e3450524dd76254b11c89712f11d07bfcdbb3d958eee1dbf0dda90327
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47922218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30dd151635f84ef1b30b9c09b96fdd5780d0eeb9d26d74e7d1dfcd08e18b828`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:46:19 GMT
ADD file:67f27a3d083f09096de7bbbb9a82e0b9e04946dd1daaa92b6fe6a0c5ad20cf9d in / 
# Thu, 07 Sep 2023 00:46:24 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:46:31 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5f58dd60a81272be1d2ac21522f5f2703674c3ae705d210024a7fba2ce1a08a9`  
		Last Modified: Thu, 07 Sep 2023 00:51:16 GMT  
		Size: 47.9 MB (47921995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4eab20b4067fab62ba057d795548226fe72672971f58db90862b1ffa101c12`  
		Last Modified: Thu, 07 Sep 2023 00:51:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

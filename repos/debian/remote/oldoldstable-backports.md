## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:1b4d254b0d757f3f870af3fb49a98f7f2f6ff780db3acb74fc633165222ea776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:b83ec837da9114cfc6d9fb9f53d5f104394745542330cae0d75c833e1f7f7a10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50498385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e79a1b894610ee7b17f2ac95157df70bd5cecbda203d2a9d85c52f0b99ae4c4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:34 GMT
ADD file:f64ab63dc255930e81f2e96163f32f2d728a31fec0480825144f9735136598e2 in / 
# Wed, 20 Sep 2023 04:56:35 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 04:56:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9c856da886d2b8776640bf119702f18c864788b4e096973c87e45a74c4270f9d`  
		Last Modified: Wed, 20 Sep 2023 05:02:03 GMT  
		Size: 50.5 MB (50498157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fb5a8b8c30c83ac9e5348aaf754b63fdf379b41210cd791e389f75ef10aca3`  
		Last Modified: Wed, 20 Sep 2023 05:02:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6bd53d1bc14a1060c6125342914dff4daabdb14b2c8c8c06369ca1c3618197b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99f981c5ed9b91ec1ab002ce0f95da60816829f12cfb241883660586c84151c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:58:02 GMT
ADD file:14046268d50e6eb660df6ad896236f651fd7973440a5334378d52eab3276993a in / 
# Wed, 20 Sep 2023 04:58:02 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 04:58:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a45ba2593a8657ba242b6475b1e9052ed1b73db093a84c00a4449689d18ff40e`  
		Last Modified: Wed, 20 Sep 2023 05:02:53 GMT  
		Size: 46.0 MB (45966232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d16538bbeeda338247c2dd111bdd1741f5222a500dc556f931d36e4e3f801cb`  
		Last Modified: Wed, 20 Sep 2023 05:03:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:86c95bc2e233769138cb04ffa304fd63a431733ca2c56bce2c58e158b6737ca2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e810868a61c94090fc25d8e2504171cdfbf714b4a673624ede3f48767d7bcd6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:48 GMT
ADD file:c668c7566bad38acdb4cf94903133ade5ae2602eaa3bb92123e69173e4d3bffa in / 
# Wed, 20 Sep 2023 02:44:48 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:44:51 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:51fc984e0490aa8d77ad122fecef1f9ce0ff384dd3acca4001f69a1ac8068918`  
		Last Modified: Wed, 20 Sep 2023 02:49:06 GMT  
		Size: 49.3 MB (49290912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c514941c74706b5272c0b3530b0a1941299b6c6eb3e4a388e550d173890da24`  
		Last Modified: Wed, 20 Sep 2023 02:49:14 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:90b9400546ddc6e36fee14cbb119b8425bbdc0a379cc1cb217d7fd8f9a2e316c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e87a2b298b4489b95b2f5475da220585ae660fe08bc934584bc9ac58d7749f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:42:54 GMT
ADD file:b87f3f07a723e87d90b68c40c013ef63eb20e4cd00411cc2d451db9ebe11fbfd in / 
# Wed, 20 Sep 2023 00:42:54 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:42:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e1039ad7b1b29f5886c8db391794e5be16e8cf8fa37f81c4c77009faf0a1521c`  
		Last Modified: Wed, 20 Sep 2023 00:48:45 GMT  
		Size: 51.3 MB (51255444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd300e8269debdf98b66c9baae97103eb7fc478cf7843bdf3ec28d9ac797e97`  
		Last Modified: Wed, 20 Sep 2023 00:48:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

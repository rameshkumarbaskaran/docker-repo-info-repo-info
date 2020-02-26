## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:860e3c061c870c583e9083dd1280ba8d06a32b4023aac2f7b2bc711b9c29ccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:f5bce7024b5420259a86c98d009816d6dcd744c731fa4bffcb8866489805b260
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45376146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37a51c85620a9d14f8ed19362637e2d8a35731da854a7dff3cbea2bbca1c074`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:39:28 GMT
ADD file:215657fe2bf1cb581572219bcec98cff51725af6f70aca48903e1c9c791a4dc1 in / 
# Wed, 26 Feb 2020 00:39:28 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:39:33 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:48a9becdd7ed4348e42a2a1417f9686c2f4579b98a685b619df07287e6ec0827`  
		Last Modified: Wed, 26 Feb 2020 00:45:36 GMT  
		Size: 45.4 MB (45375923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0380e4c9a2ee0dd66954e4f1ab8b93a6be8ba816fe38cd708369cfbeacaf23`  
		Last Modified: Wed, 26 Feb 2020 00:45:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:293ec0b3a8062377f2a6b0b6f4842c3772a7ffca8a4c37314fe0e062fe42ce9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44073580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4f92619705f5636d52eb619ccf2c07a0b8de3a518066eafabd2168d2d1dbfe`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:51:58 GMT
ADD file:88eb6a2e036ee9675ba9e65e679fbe4498013a75a8bdf854c41d913024843e8b in / 
# Sat, 01 Feb 2020 16:51:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 16:52:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bf05242add63765c1b791f1875da9e55bf5c7528a9b950bf661e4f991c40a886`  
		Last Modified: Sat, 01 Feb 2020 16:58:47 GMT  
		Size: 44.1 MB (44073355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d365130ae380bc4b1ddc560427de62c0407dd50da57cbea610b6f0be80382f07`  
		Last Modified: Sat, 01 Feb 2020 16:58:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:581a9f0221236896d92d9d47f29c71f6437ae56fb223fec363438d11046f6759
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42108543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ef4938bbf2fb05be9320da022a6611acacc6ef264e06a28f7af4b28d34e4dd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:02:07 GMT
ADD file:da5b8147307bb96330166bcc3789cef5b43e32f78c07fa38ce29c5fbe30ffdb0 in / 
# Sat, 01 Feb 2020 17:02:09 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:02:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f7582a3e720acb71b6bc2309735b30135604ff8fc4ad9027900150ea3ed7ab34`  
		Last Modified: Sat, 01 Feb 2020 17:09:18 GMT  
		Size: 42.1 MB (42108316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6d8f0f705cae1183de1d9eb7de4c0350793a716cdee38129ded5ff16691661`  
		Last Modified: Sat, 01 Feb 2020 17:09:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5c75010ea38a1186531263433c5842b0cbe50f80f0909345bf0bd470d7fb2d34
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43166913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7605c4ca47eeb17efdebd0918e4952593866a5b695709dc3d0e604eb114eea6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:24 GMT
ADD file:a33bb00e072b52fadbd86b9c212134f038075273127368b7bf4df6bff5d30e61 in / 
# Sat, 01 Feb 2020 16:41:26 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 16:41:32 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b604eb8d5c86debd6cc978e8e37dd21d4cb833841dd775994aeeae65ca1fee4f`  
		Last Modified: Sat, 01 Feb 2020 16:46:46 GMT  
		Size: 43.2 MB (43166686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f5c20819b6d2a294b06d06df3a3f249c7f9d12c75e31eceb0d97dfc5a747d4`  
		Last Modified: Sat, 01 Feb 2020 16:46:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:6c9ba1b72550c4d259389c57fd9ac905bed31f6b49802ae1dcc0bfa25bb4323f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46095269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61180abd08d874efd94e05621197df22a89d355a62c6565cdf75b8d7c6521728`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:33:39 GMT
ADD file:dbab529950d972d5a962759dcb52af085c334b562db9f7f2e3056df55fde45c6 in / 
# Wed, 26 Feb 2020 00:33:39 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:33:45 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b61e457edace805c0c3acf0b3b7d3a6b1e9b42c148ef58a20235fc6b86fe0b05`  
		Last Modified: Wed, 26 Feb 2020 00:40:02 GMT  
		Size: 46.1 MB (46095043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829675ea2362de3c92765db8c7449bc276e6ca6d32ac503b660867fa06c9de8a`  
		Last Modified: Wed, 26 Feb 2020 00:40:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:51482bc99a560e6ddddf51103228391e2223e80ed1fd2b02ca16c589b6b8d0b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45652525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0026dd86f98a89742e5eabab80349eb99eee434b9fba1ae574c3767b51b353`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:18:18 GMT
ADD file:24c12c7f45c024e1138996ab61af1c5e2587bb1b331616115d84ac4f35ec9458 in / 
# Sat, 01 Feb 2020 17:18:22 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:18:32 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5528c959a212e9d2a2d5b79cd417ad6498f5313fe82c7f9bb4fc7bf8142da4c2`  
		Last Modified: Sat, 01 Feb 2020 17:26:51 GMT  
		Size: 45.7 MB (45652297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd0d5487d6387d1aec4cafa98d86908b8d0892ed5afbfbe7d3f1b107a93905f`  
		Last Modified: Sat, 01 Feb 2020 17:27:06 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:5bd4acb4b9d6408c7e354c85cb00fdd569facf90e0534f361881fdb7b4f0eb22
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45233136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba69c9485c65632d97f51584f1e4f7dd3a0a7fdcff0b2d0848f5bf77c6c0722`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:43:00 GMT
ADD file:b4bac5bef83395e35dc722c11b35230d3615d4f63cb7822efa9b06750742feb6 in / 
# Wed, 26 Feb 2020 00:43:06 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:43:13 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5017f0ea4c6343f1edec38cd35ba1f92341ae92a0aa071fb24b5f4d53e93cb24`  
		Last Modified: Wed, 26 Feb 2020 00:47:56 GMT  
		Size: 45.2 MB (45232912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeaa10aaf3aa13df3d7b2596fb6e75a75f2334e45f3b9872ffe685fb4e96ebcb`  
		Last Modified: Wed, 26 Feb 2020 00:48:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

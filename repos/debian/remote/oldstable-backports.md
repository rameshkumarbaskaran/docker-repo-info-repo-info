## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:6f9926ddac4b78a94927c3f5ebb6396e8aa3cb5e6402bed4f834b87667adfac7
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
$ docker pull debian@sha256:60dbd20910d1abf7dcb4b98c50165d0df2719efa8d261549fedb48bbd99954fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44066768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374d96cea4088dd424bfdb95d691a778e417341f29d55afaa650ed30e973a4b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:49:44 GMT
ADD file:595c9089d9c60c3a5c5a395699ca1dca2989bd373e8f0893e4b9e33d26905ced in / 
# Wed, 26 Feb 2020 00:49:46 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:49:54 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e86bd3a4081f329cf3b59716ac8e65f2f2faa0d4c7224cc889cec32ea90e9867`  
		Last Modified: Wed, 26 Feb 2020 01:01:22 GMT  
		Size: 44.1 MB (44066542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02750b7446f147d25d972d54431d432db1f68e7a6cdef63016d7c69cfc1c2ccf`  
		Last Modified: Wed, 26 Feb 2020 01:01:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:dbb9b51566f0c77cbd2d05b48d609fe04c57e7ff090ce05105b5cf7d04e86ccd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42100472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e9fce551049f3d5d04c8c0ccfb73db6cf2caa03c46e2c2628a20eb9caf827a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:55:03 GMT
ADD file:6044d39495da6773531ddfc3db92bb84d40b219476a96d5fcd388e08b6f6915c in / 
# Wed, 26 Feb 2020 00:55:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:55:51 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3347cb00338e9d29b6e49691f0839bfa575583dad9bb5d187debb419494baf39`  
		Last Modified: Wed, 26 Feb 2020 01:09:14 GMT  
		Size: 42.1 MB (42100243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6172f08c8dfa102ebdd299e5e68f3264c88580a62b10a41ed7d7552a06a448b5`  
		Last Modified: Wed, 26 Feb 2020 01:09:28 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c202ca180aa7b5085fd398c44c40827b9cb3d1d439a086cb5c0992891e9cde89
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43158342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91dcc5eef2e495b3db97ddd18db593f5b804df349ac41c531e0c9ae683addbe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:47:15 GMT
ADD file:6e315a7191f360bef51be6ecc4d2515cda754ec2bd946bd9c00cae913db34a85 in / 
# Wed, 26 Feb 2020 00:47:21 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:47:34 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3eb70a8bb983bcdc1ea028a0a213f28d25ac978c8aad5289d07b0770222c6cce`  
		Last Modified: Wed, 26 Feb 2020 00:56:34 GMT  
		Size: 43.2 MB (43158119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c73f0c6a4371a6b8dba959f3c31f1225ddf2f909976fe74b090d658c20a2fe`  
		Last Modified: Wed, 26 Feb 2020 00:56:42 GMT  
		Size: 223.0 B  
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
$ docker pull debian@sha256:20d5b82f3995122a8f3c77c7923d61d6136e5d1b4a00c647488d911fdffd1f4e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45647332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c2a7455c9f9aa22e9245abc46446b7aa73afd0516a0c37aced87b9f85d898`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 01:32:04 GMT
ADD file:a1e8321978754a557128e3d6a76b5b6e9c8eaa057b952bb5b2f6499a5e815ded in / 
# Wed, 26 Feb 2020 01:32:11 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:32:35 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9012683918944f6eeb78636e92a0f28ef43208cfc8cc777308355f850a739514`  
		Last Modified: Wed, 26 Feb 2020 01:55:30 GMT  
		Size: 45.6 MB (45647109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fe457c5a0c46cc41048ffaeef3d161ce02bfd9b3f844f1e861e937533ad20d`  
		Last Modified: Wed, 26 Feb 2020 01:55:42 GMT  
		Size: 223.0 B  
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

## `debian:testing-backports`

```console
$ docker pull debian@sha256:ec14f1fd47e7f68b05d315fd27a2643f26bf7f2d4bb85eeefe3369eccb94b326
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:3438cf3d1b3f6f66b5d28bc476ea2c9f7011a15d95c83366f5644aac85d1ccc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52994201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916bfac9005b659481c493a0539c5c70d231e92f87f5f14beb456e03612c16f0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:29 GMT
ADD file:5c4e113e3abcb5aeb9438cdaf07c7d900b95e2a30e114fab835f40ea836e1ecb in / 
# Thu, 23 Jun 2022 00:22:30 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:22:33 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d21669d6bdb9702ceaeab2d3a60e86f23e6da7994b114ec5e684413e2628cb52`  
		Last Modified: Thu, 23 Jun 2022 00:30:22 GMT  
		Size: 53.0 MB (52993978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c05dfa858a179e24a8038674c39414380cc0f2129fdb387626e0a723a7ffed`  
		Last Modified: Thu, 23 Jun 2022 00:30:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:880213b506db4e544227ecc456856d9d4b2cc7ec53483538159122e162e4e710
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50768074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19c8a0278cfd5a6f131d21cf953445d0a85d5d42bc9cece10ab03a32233bf75`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:56:37 GMT
ADD file:c07e7c61fd09302fad7297860b6b3eba1cb39f1f856c07f548a7bc5f178da0e0 in / 
# Thu, 23 Jun 2022 00:56:38 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:56:50 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b74fe02a543a99a7a06712e27d16ef69b0202ee328e6c8c07d7ccce5e20cfa2f`  
		Last Modified: Thu, 23 Jun 2022 01:14:21 GMT  
		Size: 50.8 MB (50767848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487cacba5354225ba46f595d9d6def0437b680f75c48aa626ebf302409279e37`  
		Last Modified: Thu, 23 Jun 2022 01:14:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:37cce85736aca7622e685fb655f485dc3aa66a7c1712904493305a56cc9686f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48506773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140620c6abbeb6959bf56532d98e24cd9e84b9b52e197c2c3fc3d5cad841a5a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:06:07 GMT
ADD file:c264fb6c0b350bb6b9f8bde53eb0df81a52d4e298d687ace83936841c50cf075 in / 
# Thu, 23 Jun 2022 01:06:08 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:21 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5d4568b83e21c5428163af618ed809e52016ecd27fbcf7d0c64676bb1bc714ea`  
		Last Modified: Thu, 23 Jun 2022 01:23:28 GMT  
		Size: 48.5 MB (48506548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a848d32c1b7354143b1cbf99018b59f83a884d1c53250dd5894d989ff974e0f`  
		Last Modified: Thu, 23 Jun 2022 01:23:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:51e8924a6441ce56fafaf6680aa291ed679452f44637fa0d585d334d9c3ab6cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52074824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16ae8deac41a04b094b140ad36e71888fac52ceef14aedcd2019cfbac3b31a3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:43:09 GMT
ADD file:53311373f4d1abfcaa16b8c6fdad786327061f1e5003db1d3c6bdbf5b2c73333 in / 
# Thu, 23 Jun 2022 00:43:10 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:43:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:04df16d59bbc997b9cf53108e57268f1beac69c21eb10fac7036d92a38799d9c`  
		Last Modified: Thu, 23 Jun 2022 00:52:10 GMT  
		Size: 52.1 MB (52074599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0564e9c76d53dbb4e40f436f0c4b1197b15b93c2a37bab43aa0e5dd8748f1f6`  
		Last Modified: Thu, 23 Jun 2022 00:52:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:2bc32807dc95e5a7cabc012a80b1c9d9c33a6e4dfd6df1eabc49dd25e94026eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53963722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87eb8c81cd0eb5431796d16ff0ad559dfb647a8e73b65dbe285c25fecf3aeb0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:09 GMT
ADD file:375ae69f0d485e805c6f4304159d9a397d793c68b3a88d1a357ed44c47ecde68 in / 
# Thu, 23 Jun 2022 00:42:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:42:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b381ba72dd0238fbfeb4804fc30597036ee80aa0ecbfb82beb546f1824fcc671`  
		Last Modified: Thu, 23 Jun 2022 00:51:45 GMT  
		Size: 54.0 MB (53963500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1899152a2b46e827ff41b524a0287f235e877377352f23d6e6296930d16235`  
		Last Modified: Thu, 23 Jun 2022 00:51:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:e38d9cd5657923aae519c818821385a899be8f3d536f4463e8e364f829a37670
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52089514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4775211e36919e64a931d01fe140266bc42666b423ca0f8d281657ce74dae0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:15:02 GMT
ADD file:a6850978f5e25d773f40ca9939294a600ad78a1836fd3043e584faba009f694c in / 
# Thu, 23 Jun 2022 01:15:07 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:15:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1267c8779b3d8d2c17dc3900141ea554a243292f3668d672179b5ae3b9fb2cb7`  
		Last Modified: Thu, 23 Jun 2022 01:26:10 GMT  
		Size: 52.1 MB (52089290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ce0c05ec25dd6efc8e315ec180cbd4f8be36ad7cb3e73a7072022558c88956`  
		Last Modified: Thu, 23 Jun 2022 01:26:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:b7fb31241777fd9e78ed608f15083b6386adb8f492bc1bcdcf7bcea3ece64235
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57198164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fedaeecc21a356f243dff2b91b0fe4056ffdd30989e46810eb42ca4a5d444f2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:06:23 GMT
ADD file:6b57042319e6754088a350cd5d59a65eea1803676855cbd8a213235a99265706 in / 
# Thu, 23 Jun 2022 02:06:30 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:06:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ce15fa5088edeb9e0f23575722f7dd5131de1e7db0c2c79521f4bb51bba92c45`  
		Last Modified: Thu, 23 Jun 2022 02:25:28 GMT  
		Size: 57.2 MB (57197940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fa8ff60fe8d96ce4c538d804c197cf5b1ace2cbbbc08f646c1dee048edf22`  
		Last Modified: Thu, 23 Jun 2022 02:25:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:52f20e6869b38ebfce5e2fd7c614671990da821d7f3dbdc7e5e0ac1fa8198ec3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51530871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fa17c39ea9f064ca9827c0795624307c565664c30fee3e6d7d42ed400cf1b0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:46:56 GMT
ADD file:c00b81c115a6c1391868dbe0ec890701d2f39e6559e809c5bb3713590bd1108e in / 
# Thu, 23 Jun 2022 00:47:03 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:47:12 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a020494a73fce189d7327ea16251dde415c3d854a3d9f6bd50af5d239febdb9f`  
		Last Modified: Thu, 23 Jun 2022 00:54:13 GMT  
		Size: 51.5 MB (51530646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db29084806c4e0854decc5ece0e74a15234fd4d3a1f751e52e5e8ab44fd0750`  
		Last Modified: Thu, 23 Jun 2022 00:54:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

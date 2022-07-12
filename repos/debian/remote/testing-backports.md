## `debian:testing-backports`

```console
$ docker pull debian@sha256:805b26141c434f81f2d7ceff870441103b438e052f5f107a24bd43bf764ea7fc
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
$ docker pull debian@sha256:153f6ded171d49ffd6e9d0e2ba13af934fcf48b5ab80b309d610e5443b25fa37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50821791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a259877548c2c206b96197d1907323ec77115d1d09d300a1342a049d35a5d04c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:54:53 GMT
ADD file:c6179c8aec0b762efe1793ad6195ffc725215a2119b032d1083c0519745e2b08 in / 
# Tue, 12 Jul 2022 00:54:55 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:55:08 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f83dfb1f058c2677da0ae8544263be98b5478b5809f125d62cde7b5b1b4dd644`  
		Last Modified: Tue, 12 Jul 2022 01:09:10 GMT  
		Size: 50.8 MB (50821566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9443e5d4b71b078269476c3aa045dbe1c30aa0b2d5014a08b6e72ac86f64f232`  
		Last Modified: Tue, 12 Jul 2022 01:09:21 GMT  
		Size: 225.0 B  
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
$ docker pull debian@sha256:ef5fc77d03219497588bd63cffb032567804922e6857167f8d26e75a1593f4e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52128852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fec8e0cfa072c5c027914a9c043d33014f000c9f89708e213cf15779d6169a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:42:26 GMT
ADD file:52b0a411bbddbc5a40d2288e5189606bd2fb03bdba9ab2dfa0b29ee90195a43b in / 
# Tue, 12 Jul 2022 00:42:26 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:42:32 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:370af700e1ed84d7809745357ae1357e57448bf6e682ad1ff1a41f20c19fe232`  
		Last Modified: Tue, 12 Jul 2022 00:49:31 GMT  
		Size: 52.1 MB (52128630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6029c6655172b28d7933cba26bc204e2f8553098c11e8ef26a605b7e620f937`  
		Last Modified: Tue, 12 Jul 2022 00:49:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:fa335b6c78cdaee9fdd4fc3076d9bb392f4ac0e5e47998e5155749d1dc806aab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54004242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd898a178c006df4e0a2d6886db385c530ef172aa37faa86b9e3c200018e3e8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:19 GMT
ADD file:044345c3015d2fe1cae3b8a12314680146d341abe9874bd58fdcbc1589642c13 in / 
# Tue, 12 Jul 2022 00:41:19 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:41:25 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e40b58f267b2fc10cacd56d0f087127ea8b9dde1c3708ff2b4f4650a5ed2d08a`  
		Last Modified: Tue, 12 Jul 2022 00:48:38 GMT  
		Size: 54.0 MB (54004020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d8a37281c18e3d31e1221661b8b496c03dd550e4e93b66c80cbfaecb5f3a76`  
		Last Modified: Tue, 12 Jul 2022 00:48:49 GMT  
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
$ docker pull debian@sha256:215d881beefb93b2aa019b733b1faaf76f6ebb1720b9e801461184c846467946
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51554349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663cbbd57a0d7a95aa3fd14fd6367aeeac1959f24b599080ee768798c9503487`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:48:02 GMT
ADD file:d73eeeaa444d7c8255cd2ca31c00a952231237fc5487b1e6772c5f70cafd440a in / 
# Tue, 12 Jul 2022 00:48:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:48:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:80dbf564ccdb8d822debfb926a7eaccbc64bd2365e4541f63e07fdf1295dd5f1`  
		Last Modified: Tue, 12 Jul 2022 00:56:09 GMT  
		Size: 51.6 MB (51554124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c3d2a0890f66ceefb89fd3d66a144187e7641f7d47fdfd95e251762fd76466`  
		Last Modified: Tue, 12 Jul 2022 00:56:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

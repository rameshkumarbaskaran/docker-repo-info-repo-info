## `debian:experimental`

```console
$ docker pull debian@sha256:c93987cce80daab70b95c2d0d0a029c5a3182d2ce9e4e51031ca0e54478a25a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:301b6e0eb1383ba70a19e6366f278a51943df574b8121379158452b56fcda779
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49261502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc97ee223ae605e070a611b7dd86fbeefea71a25aa9fd82e0b73c9da453ff43`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:12:06 GMT
ADD file:dbf92bee170231a4a80e859bf48510468217880ed900ff23441d1324af2051b7 in / 
# Wed, 01 Mar 2023 04:12:06 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:12:20 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e5691ea88f53395815d6a2372cd7927234a45ab112cf06f5b9a0cb650d48e406`  
		Last Modified: Wed, 01 Mar 2023 04:17:32 GMT  
		Size: 49.3 MB (49261279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d237338c28e89e89f278d6c1f7895b269194a4175cb03a6d80426604e545e203`  
		Last Modified: Wed, 01 Mar 2023 04:17:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:3179a8c3a858f622fe52a61f2b2fb26388e39e0a21a0e0b5aff85221f8b05c8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48107946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dda7d7a9ae00da59e82175de7bff20e7c7b2a46f14126d654778fb9493aa9ae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:49:52 GMT
ADD file:c3e085c3dff5f8a26c459819fec4fdc2ea28a857d84f1b06ea2536ab2c11f178 in / 
# Wed, 01 Mar 2023 01:49:52 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:50:02 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d9e0e6decf94a96d3649bc9614fd0ea25205676ea5004891847e53ead7e8b5f7`  
		Last Modified: Wed, 01 Mar 2023 01:55:14 GMT  
		Size: 48.1 MB (48107725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e529ac0697461ad7c874d3a0f17f7b81df8ad55567c76439918604add3a00d6`  
		Last Modified: Wed, 01 Mar 2023 01:55:39 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:bfe53e149bebc51e24fc14a73abdc3316704c8a0d0d4112604b0714543e9eda6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45879161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b047ad9cd600da9876ef2226f922a2868c16cd4499fa1ce3cc8bec3b053082a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:59:29 GMT
ADD file:a37e569a76cd9d80fe83d6cc15d442ea2ffc849415455cb6a8e017724ff6d05b in / 
# Wed, 01 Mar 2023 01:59:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:59:39 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:46b58fd36a9d0d3ccb7b3f47d82fbca683b31e8aaef9797a987b82692eb81560`  
		Last Modified: Wed, 01 Mar 2023 02:06:40 GMT  
		Size: 45.9 MB (45878940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f7667e455d107f9682da2ecb8d284066858f2c8059130be67f763d3fe31b88`  
		Last Modified: Wed, 01 Mar 2023 02:07:06 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:efc8c53c7e8ec804a3fdb97e5d41f1b87b6f03c1c262411cf5f14e7930fad5a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49319208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64b496c658ef5ff8b09f4eb071f87a0192c7692fdbf8c883d0ea56c91adaeb9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:46:25 GMT
ADD file:0affcb10430712dd73055564d3fe7c0548bcc203c6e8a0c200c4b48ba52900f8 in / 
# Thu, 23 Mar 2023 00:46:25 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:46:33 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b400817afa0c1b0b5323fe5eb38a334172ba17ead32c49762767d869161603f4`  
		Last Modified: Thu, 23 Mar 2023 00:51:02 GMT  
		Size: 49.3 MB (49318987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4cd8709e1cb452a702dbef9012d6bb8eaae94069e7e2436cb0ac527ed5856`  
		Last Modified: Thu, 23 Mar 2023 00:51:24 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:715da7bbf5f20a42f1bf9e3965de1761da0a4fb3641e8d64f11006067e9f1b85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50314767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d355426c99a7371bf868453a8ba6b543b110c4f84c4221ec52c2ed493d92e32`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:41:14 GMT
ADD file:91051a34bcb35ee9e94090f813b07bf915da58d01acb1e1a51031171a6eb0ce0 in / 
# Thu, 23 Mar 2023 00:41:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:41:27 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:350e50626198efaebb626c28f35f6aab6f02ce94e1bda1166f63672ca9c13303`  
		Last Modified: Thu, 23 Mar 2023 00:46:39 GMT  
		Size: 50.3 MB (50314547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562cf269bd2f25740bc81e36165a927c8907b0eb6d643c883ebf01dcc3adee47`  
		Last Modified: Thu, 23 Mar 2023 00:47:01 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:fc93a8eeee50d7bf701c17102fe5cb17db6868127f799c58e304909d654f5624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49270843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05fa24d6011f6260fbb995ca100cf36b4c6f24bdc1eff3d36882d878e3776d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:14:57 GMT
ADD file:3c9761555a5ea142351615b9c67fa1d733eb4055b0a7ce13452185d0a0569a8a in / 
# Wed, 01 Mar 2023 02:15:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:15:40 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:488a223217255f1854f177e926f43908918ca067d20ac1205a5c8058bacba304`  
		Last Modified: Wed, 01 Mar 2023 02:23:05 GMT  
		Size: 49.3 MB (49270620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3335a1cbe608936e7e2ce0033bb81a3db2d76717e791d353e05fda95808900`  
		Last Modified: Wed, 01 Mar 2023 02:23:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:590122cb8cec4c19179b1038682311340c5a53b85640d1a5aed137503f6e573a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53273224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e6ca9ff1803b155501a5c81cb48a550256df7d91862b08ee47692c148a7794`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:50:06 GMT
ADD file:87be7e9eb6e59aed9d270ac466c0aaae2e1219c0962ea77878d0e1e2e379e7a7 in / 
# Wed, 01 Mar 2023 04:50:09 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:50:34 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a42971a48e8c57e8ab7b8b69dbe1b5e1fba784a37174b997fd813ec5c6279335`  
		Last Modified: Wed, 01 Mar 2023 04:56:55 GMT  
		Size: 53.3 MB (53273002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49beef18431296b3488de0b924aa7dcda58263a5ae78cbcfd1330eafa9103c4a`  
		Last Modified: Wed, 01 Mar 2023 04:57:26 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:a06a701457b4670cf4f18d6da80dd1fecb47ca22bc5a3f9f878344a1b8f306ed
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45466086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b368ee73ad2a4a9b89883a652b8c57eb1eab319715ea1653b1adfac3147e0b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Mar 2023 00:48:37 GMT
ADD file:d0560983a185cdf6ebef2da4efe5ac6b804d9b8fa6867bc392f79d2fafea80bb in / 
# Thu, 02 Mar 2023 00:48:39 GMT
CMD ["bash"]
# Thu, 02 Mar 2023 00:49:25 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6099a9d003adb0e56c4120bda00747d08bec9165f923f82dee3953e229a34e97`  
		Last Modified: Thu, 02 Mar 2023 00:51:59 GMT  
		Size: 45.5 MB (45465860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ac86c59767fa84a0668f66ca16fc0c03e496b9f4809727ef325ac0d499cee3`  
		Last Modified: Thu, 02 Mar 2023 00:52:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:4946ca3720705048b10646de1f54f8721815c13b48f54535a3465ea8db6a8f5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47648248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb210152ae579ea153dd4c8c32cf41606fc0c7ec5d3ec25b3bdbed57caae101`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:40 GMT
ADD file:87a1c5a697c0ce402d70710d206bfb13b0399785b6b9120109f7099c256199a8 in / 
# Thu, 23 Mar 2023 00:45:43 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:45:56 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bc794848966cb11ec8c207602b033a6a5b7e3c9334d0481e4d332bba4c4cd57a`  
		Last Modified: Thu, 23 Mar 2023 00:48:40 GMT  
		Size: 47.6 MB (47648028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efff8fb6d8c9f34679dad324583c9e11c7365702cc08af1adae4de7644503b6`  
		Last Modified: Thu, 23 Mar 2023 00:48:56 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `debian:stable-backports`

```console
$ docker pull debian@sha256:b58027974f91ddc38dd3c9df75cd4509ed813a57fa645a9c54e45d1739885b51
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
$ docker pull debian@sha256:ab4b74aa336d446dfd67d592f71b8a5880ca4e91279ccd7c70f20fae0144ac42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49551632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78ffbc19732f9a6d6685627ceeef9cba3a8d01d8448f4a7e2896a03db1af77a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:22:10 GMT
ADD file:2de2d7c41413b3d58634c92893c3e99f0d1464f1ab02785208509245497be121 in / 
# Tue, 04 Jul 2023 01:22:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:22:15 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b5be7a721d800e1ee6428736cfb46f85cb70c4f1a7c06d144f60f929ceaaf5fc`  
		Last Modified: Tue, 04 Jul 2023 01:28:13 GMT  
		Size: 49.6 MB (49551410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05229969914fdc6497982179b7fde002dd1b5025f5928b59355b1b7d61de2e88`  
		Last Modified: Tue, 04 Jul 2023 01:28:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:babf895d3ea280fe191ecdf7a9932bcd705890639af081a7f569aaf341afbf1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47402957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2ac8f1bbe838c17afe4be2928b58147acb8ffff5d2749f24d5ab0a5d211217`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:49:24 GMT
ADD file:4560973449ae95ba135b1d2a4749ce4d278066080d92407b8fac46bc17e195db in / 
# Tue, 04 Jul 2023 00:49:25 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 00:49:27 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a1441b766c0384e637ebb6bcf7156542cf9e9a87c03d36822c1081d39c369d79`  
		Last Modified: Tue, 04 Jul 2023 00:54:02 GMT  
		Size: 47.4 MB (47402733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827eacccd25a8db7c434c06efb03b120ad7f207524d6fe2551274faf715d3b74`  
		Last Modified: Tue, 04 Jul 2023 00:54:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:26ae0aaa0539df8eee4df5f60c72cdbb324536d7b7180001f89699cbe8855f0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45236446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8b5302cd8505b9d6fde743fb043d478cd468be6175f97f074cec44409a3f47`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:00:12 GMT
ADD file:79a37c77c46d6158e0050823174255b2fbd19b7b2a6321b195fc725519a2e82b in / 
# Tue, 04 Jul 2023 01:00:13 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:00:17 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0fbd4a02f7e9523396cfcce42fa09a0e010c6757aac4ee88a5814ba28b86e098`  
		Last Modified: Tue, 04 Jul 2023 01:06:13 GMT  
		Size: 45.2 MB (45236225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c724686e9580217c87bac7f99dd29b7e9ff7ec915783bfb903225ef27183802c`  
		Last Modified: Tue, 04 Jul 2023 01:06:24 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:cc6469b6f5189d5f18edf3d7b9f616bf6ea16747c7320df9df8d8949b660cf28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49572965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d235017a1f10a213eb0843f71a980519387cd032a509bbeb00ba91bb09512a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:59:04 GMT
ADD file:79e09e609b23970908767f4254ae6453b2f2cb678a7639912cf4ae8823781aa0 in / 
# Tue, 04 Jul 2023 01:59:04 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:59:07 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8cb8a2ff9f84a753ab1cef3aebe7f6b4f4fe4dd799c343046673687ad1e123b1`  
		Last Modified: Tue, 04 Jul 2023 02:04:24 GMT  
		Size: 49.6 MB (49572742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408b4bb8dbbbb9bee90e757119f781bb71929f810dba5f6cdae9a13af86c4288`  
		Last Modified: Tue, 04 Jul 2023 02:04:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:06ea90f3196b5a18d1259fae567079fa5b8d7e7f186ade3e792ecd085a65d49a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50562618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08564de710239fbd3efcb5f72f8c8efb2ff76d043c045a9c6e3ce51c0e539131`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:40:40 GMT
ADD file:7b0bf2dc9519a1e02da67dbad17f5970b273f7d8e8616afb763c8f3707d1d4e9 in / 
# Tue, 04 Jul 2023 01:40:41 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:40:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ab8c19d79aca410e867102a952a06f0eff14354ef8cda03aa635a7355236a4e5`  
		Last Modified: Tue, 04 Jul 2023 01:47:03 GMT  
		Size: 50.6 MB (50562395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38be7543a670d269201c15aa919443e6d4c4b1efe95eb5db14818b29eaccd95`  
		Last Modified: Tue, 04 Jul 2023 01:47:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7daf2a257cbdc97e5d9c32c40839b4205722a3c6db1e52af651aa154e36cfdb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49542395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ed6d8cdb64c939560e5971216daab2b6c184b2b9e8749267eb14164a5df140`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:13:31 GMT
ADD file:b3dc9cc8ccd9367e0ad281da5eb70296ffac2f063ef44d86aba57316b35d4cb4 in / 
# Tue, 04 Jul 2023 01:13:37 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:13:50 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eefef2cdc8981171afeb848988d75520dd7c7b357a56c47f68f8bb38b6b8df54`  
		Last Modified: Tue, 04 Jul 2023 01:24:22 GMT  
		Size: 49.5 MB (49542171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d61d5db650c9c31dcaebf07697eea7a8a16dc977e1a50072a851b3cfe8be01a`  
		Last Modified: Tue, 04 Jul 2023 01:24:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3dbb7864f84410db3d33ad2ee533acbb588124e0cb71938cef6cbdef2042fcd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53536962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7c4cdacfedc01abbd14f76b626844bbc8b6b0e6f865f35506535e59e5ec581`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:068cd55f1f48b9f120a5ab83c28b77cac6aca0c6d09a83d7d69f35e9d4511d19 in / 
# Tue, 04 Jul 2023 01:20:13 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:20:18 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0b83f823e9aba68f5128f9af5447ebbcdb46e043ff0e79fca69f4ab36adbf7e0`  
		Last Modified: Tue, 04 Jul 2023 01:27:47 GMT  
		Size: 53.5 MB (53536738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe7ea9ff408b8f4cbbefd7a104a7d931d80d984e6535163fa5353003ec71ce2`  
		Last Modified: Tue, 04 Jul 2023 01:27:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:10217786d71e03c38589592e5fe8bc14ca29edd6da25818de3da37846ceb4db3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47921947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b01a7df9ed46601329ae17b23f5c9ce0ce4275dfd32f751211a76dd4cd36aee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:33:50 GMT
ADD file:9788171ce0f336dccbeeac19aa7fb65ec93cf7774a2893c0532b3ddcadaee9c6 in / 
# Tue, 04 Jul 2023 01:33:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:34:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8a02e2c90ded98ee4201c0b941febbd8d4e1ba1a83af3c904c62f9b019abfa9f`  
		Last Modified: Tue, 04 Jul 2023 01:38:36 GMT  
		Size: 47.9 MB (47921726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f23ed1db943771efea04e1c1da4614765e2b28822fe90f2ad636bb11410b4e2`  
		Last Modified: Tue, 04 Jul 2023 01:38:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

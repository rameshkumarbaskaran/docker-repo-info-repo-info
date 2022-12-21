## `debian:stable-backports`

```console
$ docker pull debian@sha256:5390159bc3699e32763d32fd7f61b4666c8bd7d75ff54d51f5853d7bf342173e
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
$ docker pull debian@sha256:4b7100b67b57c579b07e1eaab7d1b5400cd21e644292e63675b1d660a6d66d15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55025365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b738a931fc351e539618c7c653286189471093ec0e9866ed48d1889e480275`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:21:39 GMT
ADD file:d9c343f4dfe91e0e31ff144c5418c1ed52aada034a440c32ae0cf296c0fa9d5f in / 
# Wed, 21 Dec 2022 01:21:40 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:21:42 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:68be6800823f00619f0eb565e96687c02b92276176d6b9f8343d4051b74fff46`  
		Last Modified: Wed, 21 Dec 2022 01:26:38 GMT  
		Size: 55.0 MB (55025144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed7e1bb5912023bafa0f14c45871eb17eeb96cc1b85c250edd441c88d9cb56a`  
		Last Modified: Wed, 21 Dec 2022 01:26:47 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:98df7f8da93d35952ee7002163d4b45f002efe9e52ac13e455f4d8dbf53d5317
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52530211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4273278a659dde7488924789f8aabd96e7f4613a432267faedb2a79e68b769e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:40 GMT
ADD file:07adcc5b3eadbb8ae7c813a5b9b4fd0f5561682a868c7d53f46b0a1801a511d6 in / 
# Wed, 21 Dec 2022 01:49:40 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:49:45 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2b3ae89abaec33de158b0755bba5f91a97ae7e54aca02f351158e27322a3a377`  
		Last Modified: Wed, 21 Dec 2022 01:55:05 GMT  
		Size: 52.5 MB (52529988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efa9394bf541fbe078013b7da9712b93cefe4d61b933a20e6f6761da304aac3`  
		Last Modified: Wed, 21 Dec 2022 01:55:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c5692652ec2c052730565934da8047542d2f32911929f94df6641aa6ba83879a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50190971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09960f12bc55a0e7f173ae04be7bb8c14a9a9e600c4e7f54d2c6dd888d3c0e7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:59:54 GMT
ADD file:f3dec37c083d4cada65590fae6ac2bd7c9a61ce7a0df2d52e6051aba39e2b1b6 in / 
# Wed, 21 Dec 2022 01:59:55 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:00:02 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:31c269211ae719b12c6c079d7498d98789b5cd4f09753a31ea5446405c64afb6`  
		Last Modified: Wed, 21 Dec 2022 02:07:43 GMT  
		Size: 50.2 MB (50190748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e046c8d60e6dbb98c77bcbcfdd097d1c93491919d8b73dd959281e0f6b5290`  
		Last Modified: Wed, 21 Dec 2022 02:07:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d8bcdd3a3efbb45e3fce484b7aebacde164a7e3956d55f950b5c316618d8907d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53682030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47faf41a8becbcd116239335027a32f00cbc9213e65af4bc1c105267209b70ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:34 GMT
ADD file:b3ebe2c2e392f5fc5b185ae4017a1f0ede3af91960e170f7290eb7991fb48a8f in / 
# Wed, 21 Dec 2022 01:40:35 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:40:37 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:46e383a3bc7ec8c7f2e22cd5f1510e66192d9d932e4305e83640b096f51bbc55`  
		Last Modified: Wed, 21 Dec 2022 01:45:07 GMT  
		Size: 53.7 MB (53681806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea83e6c17e211155743b9cb3e77abb7526d3e9b56d53ae0476b96e4300a2e8d`  
		Last Modified: Wed, 21 Dec 2022 01:45:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:7ff62efd86859b6a0aba7943dba18a87474bbbbeb3a0da620c88ccba3bc31694
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56005466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99aa56a6d266ac2a9848664128f00d4a780b9ca29349d33def17f85984aa879`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:38 GMT
ADD file:120ff72489f2e74bceacd040dc22a252035f8742389b75ecb6cd804737f603a2 in / 
# Wed, 21 Dec 2022 01:40:39 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:40:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:379393af86cb5439c757cd76cecc85bdda743e868da169a274943629fa9d7e61`  
		Last Modified: Wed, 21 Dec 2022 01:47:06 GMT  
		Size: 56.0 MB (56005242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6f99c1211153f906892d4550f508e07367ee30bac4a9635f22ae8b0754adb4`  
		Last Modified: Wed, 21 Dec 2022 01:47:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:9aab52a589fe9adb13fcae676a04bfae7b99c57300e7cc8a700dc807dfc78502
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53245305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff1625ba8424f4f61766c62a44446a217c11a7d2208c23a61833205b56486ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:12:11 GMT
ADD file:c78307398a21ca1a1eb99dad7c1e47578e8459d4a935d7f9d83dba7df1982d97 in / 
# Wed, 21 Dec 2022 01:12:17 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:12:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:06854a7b3b78f7102b75c303383d67d86ada6d9dff67c9ee5ca3200abeaa24f6`  
		Last Modified: Wed, 21 Dec 2022 01:20:35 GMT  
		Size: 53.2 MB (53245078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c90e6970b771356c4b72159d74bf6b3a025f3cceac9fd0f3b8747958bd15dce`  
		Last Modified: Wed, 21 Dec 2022 01:20:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2ab361d2f1462eff62998668becc3a16cf51cdd45e465c97b1f845a724324fdb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58897292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8eb595f963d86a2e03d4acb7d1ef9374d1a4e526bd789c511369845f5ae968`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:18:31 GMT
ADD file:da548841c930bdff2631803f71e8342f09fce4bef48c7ee19db898e27a783063 in / 
# Wed, 21 Dec 2022 01:18:34 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:18:39 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4d49780a65e59eb79da041fcde3221638d4bdbe77fe9f061d5314ccad957b043`  
		Last Modified: Wed, 21 Dec 2022 01:24:34 GMT  
		Size: 58.9 MB (58897069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23d611550b60cac2f25538cef1b6e6367521bac888d980205368deb312cd06c`  
		Last Modified: Wed, 21 Dec 2022 01:24:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:835c8043a36788b2f7c4da8bc15e9ef6e5939f4901e9225f6bcc1409f7c1f290
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53258718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259d9c42e3fe2e93c9e816250c8d55203e0d6aa67aec0fa04c6a539095530a2d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:44:04 GMT
ADD file:be916266b79f79601d1669a69d087bc9af65d2d5980415651b56101df0d518b9 in / 
# Wed, 21 Dec 2022 01:44:13 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:44:22 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:09c13e87c7dd5cb6486cf055337163ddc8cc55fd371742709f8373bb0887e239`  
		Last Modified: Wed, 21 Dec 2022 01:49:53 GMT  
		Size: 53.3 MB (53258492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a9abe4cae3bd18ac6f4d6a7fcfaee123f552cee690566fb6ca6e0165cfa101`  
		Last Modified: Wed, 21 Dec 2022 01:50:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

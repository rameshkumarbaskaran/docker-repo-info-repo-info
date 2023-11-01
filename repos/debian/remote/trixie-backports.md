## `debian:trixie-backports`

```console
$ docker pull debian@sha256:56f72d3edf6d6fddb7c8663eaa6e262f959ba5a62b691723a104ca5cc15bee63
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:bdc804b709f9f08d29f5714c321007d3c7d73a4457818153ab6d197a49471281
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49487111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cc365e6d64f1fa99f644a3d349d49b2e0253b34a2ed505fa8ec0d47e4d579d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:23:31 GMT
ADD file:00d06a447c9580e05c2514d623a6906f35419629a74e8f29f8627b620df970f3 in / 
# Wed, 01 Nov 2023 00:23:32 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:23:36 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9f30dcdc5629f1d2f740d6a704db5e6f29ed782df4486ef49cdbddb30250312f`  
		Last Modified: Wed, 01 Nov 2023 00:30:07 GMT  
		Size: 49.5 MB (49486885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0cec7452f61de8db69b39ff009d17ba7e574e5f249fab5834ce1264cac1b59`  
		Last Modified: Wed, 01 Nov 2023 00:30:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:3e8786fde4f3cb233a58d7f3377ed5349e40961ae5882012cad77e654d94ed21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47142341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c5714adab648f4fa0b6c7c23cf7c98671bc7501a31583cef728687015a3215`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:49:55 GMT
ADD file:c8135c4f5f4b7815dc29bb93d73adb514649c5dfb72bfc1c072a7a9ae53653f1 in / 
# Wed, 01 Nov 2023 00:49:55 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:49:58 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:136f2fd3e12dd347dbdab54d5a79402eda3c65de7050120b6c1d86345bcc99da`  
		Last Modified: Wed, 01 Nov 2023 00:54:48 GMT  
		Size: 47.1 MB (47142117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fadab712cd84b379a4a8b623fd340eacda8fb0733493f900d1b28f40e9c035`  
		Last Modified: Wed, 01 Nov 2023 00:54:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ba95d214a64ddeab1619b10a1334664db895aedacbbf0aa0dd31600909929632
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44936420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fd2c88ae3ebf4f1527344f63903506a141cc4cea01df9933a72dd1253303c3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 01:00:07 GMT
ADD file:035b362840f9210e5a7bfde4a95079958d9f57f5b5a556d22b48ad6abcdf2134 in / 
# Wed, 01 Nov 2023 01:00:07 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:00:11 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b403287e0cd0f39bef349bb68bed383fd0582cc2ae9137aac1969a41c84e30db`  
		Last Modified: Wed, 01 Nov 2023 01:06:58 GMT  
		Size: 44.9 MB (44936197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670c2a12d2df56375abcb699597789cb8929c915c6546f9c2c34c0d2f603607d`  
		Last Modified: Wed, 01 Nov 2023 01:07:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4a93adbb154f1fad647745da547c4ff41af2d385204e6500415c5bd9c9418f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49495451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d12d053b207ab6585fdfb5efd1d250f1a4cae53dcfb2429e466c0b0091b10e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:41:27 GMT
ADD file:d0c94454bffd347b60b86607fe3aea27f4afc57648c812d80575bc9d7d71a1fc in / 
# Wed, 01 Nov 2023 00:41:28 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:41:30 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6bbd151733a83c3c4e1747562a07b8dc0d6b9a1a38140e050fec86a0e73e1f0e`  
		Last Modified: Wed, 01 Nov 2023 00:47:15 GMT  
		Size: 49.5 MB (49495227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4e8ed1638a7121f3e41c0aa7ae4707ed08f4e2eac9ba94a29c394ee1650c59`  
		Last Modified: Wed, 01 Nov 2023 00:47:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:1fe06754c9500a1ddec557ac865834b21f5f5dcbe7daec8cd3cf789430aa6adc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50466600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c3b3065aa7582d9a54ef3a65f7e975d18656e3c132d093d154ec4b03b006f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:41:31 GMT
ADD file:99d6a1f205a46734ffc61c992b3c9029eb83aceaab7b9777a94552ae226a209f in / 
# Wed, 01 Nov 2023 00:41:32 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:41:34 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7778791eeb3e7444e84c2d682795ca0f756d9e1d87e924e2739660a8ed9134ad`  
		Last Modified: Wed, 01 Nov 2023 00:48:34 GMT  
		Size: 50.5 MB (50466373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a86dd0dd31380a808cf26fac4c3645f7e923c35b932daf1ea37e13eccdcec0f`  
		Last Modified: Wed, 01 Nov 2023 00:48:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7f5f497905feeddfb64023d15f8c472761271cb81c3e0ffe02c3b5e0289a86b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49278854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f890467afdb27ca48d80eb0033e0bc5fb9ff7d0b069878a43f176178a299df13`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 01:15:37 GMT
ADD file:fcddbc3f0c0456097a49c255590801b884727d47f9ceac6afe8463117d63a70e in / 
# Wed, 01 Nov 2023 01:15:43 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:15:52 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:434392845279581746e8cecd769b536845c39fb214d29012afa566896853392c`  
		Last Modified: Wed, 01 Nov 2023 01:26:47 GMT  
		Size: 49.3 MB (49278627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e093716c180c9b302fdad9a43cac4c120ec47258d4f724979392894f3ee46a1`  
		Last Modified: Wed, 01 Nov 2023 01:26:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d76ddd2d4a4e45b0a0c4c7f614de6a11a1e7c7e2b828a076d0a47bb8b2413a6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53390924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cdf2e8fc41114283c5a8d0097ebb0d6df142f0bd4ec13e6f9858c6d8f81369`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:24:06 GMT
ADD file:d45c9f62cb1fd4297a5ee2026bc6abb62f25a456f3a44a8ab6d115eb1d59ce39 in / 
# Wed, 01 Nov 2023 00:24:09 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:24:14 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a86485f1d263f9f0955a85f3d3707fcc2bc7bb4d598df11d02b766bd3da90ad3`  
		Last Modified: Wed, 01 Nov 2023 00:29:48 GMT  
		Size: 53.4 MB (53390698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305022e1c359401a1cdad9cfbc1bea3678901553f4f559b88c604c3c7d6c8573`  
		Last Modified: Wed, 01 Nov 2023 00:29:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:22e9d15f57e31355fe358971ffb5dde465ee57b2bbbaad01a1657af6c89ae74d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48900405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612d69bc95bcfa04c4b5bbb830b90c96162596e341158579d3ff59a1a6b9e212`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:45:36 GMT
ADD file:b451624b6214da7e4871235da21071d55a6c21b9ed56fe301e78beebaa9c034d in / 
# Wed, 01 Nov 2023 00:45:40 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:45:46 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:37319c2577b55a62447a947186364b13c616c3448bd2c4aeb444733fc58dfb64`  
		Last Modified: Wed, 01 Nov 2023 00:50:43 GMT  
		Size: 48.9 MB (48900178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0cfe8d392bfaff4d56d4eedc6bbac037154a04e2ef6cad5436b16954216e573`  
		Last Modified: Wed, 01 Nov 2023 00:50:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

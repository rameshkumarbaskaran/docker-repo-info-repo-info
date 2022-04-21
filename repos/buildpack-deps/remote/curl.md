## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:0bde98e1dc9b8b49bc97d3a2af3dc0dc29b1032f0917e1dcd0fe5d5dcbc0c619
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

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bbe7d63d0287a34ebd6eb8b551fd51c957a23f0ed395017ad7c27d7cb4037570
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70972421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1984eca1d4c0efb7b52ba8b27e1c464f161e76c0d260960e5497fa624676480`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:15 GMT
ADD file:3a81c181c66f226bd6abd48d0c7ed8a9c599c9f521ec7229286c83161afec8c2 in / 
# Wed, 20 Apr 2022 04:43:16 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:57:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:57:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6aefca2dc61dcbcd268b8a9861e552f9cdb69e57242faec64ac120d2355a9c1a`  
		Last Modified: Wed, 20 Apr 2022 04:47:57 GMT  
		Size: 54.9 MB (54941777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967757d5652770cfa81b6cc7577d65e06d336173da116d1fb5b2d349d5d44127`  
		Last Modified: Wed, 20 Apr 2022 07:05:43 GMT  
		Size: 5.2 MB (5155716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c357e2c68cb3bf1e98dcb3eb6ceb16837253db71535921d6993c594588bffe04`  
		Last Modified: Wed, 20 Apr 2022 07:05:45 GMT  
		Size: 10.9 MB (10874928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f6135240123669e1f1f43f1050db8b470e9a7ca747f5f94d94b50948dc413d1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68113244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fd475bb9a0f013ec317ca5d7be7c06cce530c80fcf9e32dbcc6bf94b50ad2d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:16:05 GMT
ADD file:d668b425e22c8042fc04ca031d5034b01d7488f8b7adf54485b4025fcb8eea77 in / 
# Wed, 20 Apr 2022 07:16:06 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:39:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:39:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:625ca11644bb62d8db7c0b110e4fd87d4b2b14a21e09653f8ea20ef89a5d2663`  
		Last Modified: Wed, 20 Apr 2022 07:31:39 GMT  
		Size: 52.5 MB (52474869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d4384c7dae46d328099bda88d10ebbafcc471d58bdf0406b841e921662c498`  
		Last Modified: Wed, 20 Apr 2022 13:01:10 GMT  
		Size: 5.1 MB (5065356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5055670fe43460d473fa625bd789cb9b2914d39fbf8340205152c5df047212d`  
		Last Modified: Wed, 20 Apr 2022 13:01:12 GMT  
		Size: 10.6 MB (10573019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:47d78c3c0e5dfda5067991590351daab9a2417edec8e526b41b8439a8d06191e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65276553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6799798cb245df14e6b47c37719d8842a45304b51aa9b294950013d377dd881b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 13:26:39 GMT
ADD file:1c05c50014bbd32a4cf1edd085996a8c62abc3c8969b64d2355475827a07475e in / 
# Wed, 20 Apr 2022 13:26:40 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 20:07:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0a2c02101ee4340d4a9ebb962e9331486e417a3835c9adefb9badd2f0c116ab6`  
		Last Modified: Wed, 20 Apr 2022 13:42:55 GMT  
		Size: 50.1 MB (50133696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301394875428f05a3ac7068600f0d729f8c7df313e7c9574aec8362194fb4e56`  
		Last Modified: Wed, 20 Apr 2022 20:30:57 GMT  
		Size: 4.9 MB (4924850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f80b9e8049b2a4b26cc100bccded1ae7d0bc8ff2e1fa9fc7e255631328f0af`  
		Last Modified: Wed, 20 Apr 2022 20:30:59 GMT  
		Size: 10.2 MB (10218007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fad67c562b8b3bf27ced56a95d62e9bbbec4d5b680dba157c18e80dcc47dd815
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69228730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7425ae4c9fe74ce5f7f9f3a8b5eb018474a6623d9de3808d303a916c99f91361`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:28:55 GMT
ADD file:ece192802cbdaf1a141d04f0c2e90cfd3479e5e3e82c6a00206970684494cf48 in / 
# Wed, 20 Apr 2022 04:28:56 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:44:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:44:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:83d5dcfea08e6927083bc886bf182fc39d87bb04b54b63002ac0c4c0b9aab682`  
		Last Modified: Wed, 20 Apr 2022 04:35:19 GMT  
		Size: 53.6 MB (53633096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cfa86b7b1aca6d694057e4d42ee1440527f41c00b9e577df729244380c9eba`  
		Last Modified: Wed, 20 Apr 2022 06:54:10 GMT  
		Size: 4.9 MB (4938663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c79b19335f27cc78840bf9159e875322f3252ac06113c73756f9d4fba905f9b`  
		Last Modified: Wed, 20 Apr 2022 06:54:10 GMT  
		Size: 10.7 MB (10656971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0d93e8598333ac41bb47bc06d5e00393fd974626502e496153f34b43da4a1a7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72054664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5c45db5f038eadc9bbe5f07f6f7344fbc98eafc9602bb3aeda7009e4ef6720`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 07:37:18 GMT
ADD file:81b79bac6ad02f2b0e2d30c005dac5f38d58fc7e12d7466c6704bc8a8980a0ef in / 
# Wed, 20 Apr 2022 07:37:19 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:16:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:16:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:03830d6b0d2ecb0a7f823997ff6629d0ff36a821ec317f6d5644d08b1870d936`  
		Last Modified: Wed, 20 Apr 2022 07:44:23 GMT  
		Size: 55.9 MB (55940721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5cb7d3850c1f11597dc2fec3a9db47da0cf01b07710d9db78b1bef55ee2868`  
		Last Modified: Wed, 20 Apr 2022 10:27:18 GMT  
		Size: 5.1 MB (5080236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d496dba7030d724d160a2e22c59274cbb50c0ef8459868c1606869acc1e547dc`  
		Last Modified: Wed, 20 Apr 2022 10:27:18 GMT  
		Size: 11.0 MB (11033707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5d3ef16b8edeb00f874ec62648297a4bd9fcba2230d03fce6266bf9e4c520a9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68775565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8169e8268aa95f03b8ba2b66f87daf73c2a8e8eccf9e0c10b28511d6e8e9f867`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 14:27:54 GMT
ADD file:8150012d71535a0807e6b7f0bb9f31dcef864730e1df2362a20fb269ccc902a2 in / 
# Wed, 20 Apr 2022 14:27:59 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 23:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 23:16:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:774a3fd0175393ffcac86ec5a65f3f57dfe09f9c38a55812cb69c85281394d6a`  
		Last Modified: Wed, 20 Apr 2022 14:38:35 GMT  
		Size: 53.2 MB (53203304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844a58a93488914047d6805e3dc9f4ae899bcbf99d6a7471f9317a6d3e1ec7e9`  
		Last Modified: Wed, 20 Apr 2022 23:42:13 GMT  
		Size: 4.9 MB (4912267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8511d2f4e2a16a1f9fbd5a7f93cc0afb4c48d25ca3cb1384417a007f74ac71`  
		Last Modified: Wed, 20 Apr 2022 23:42:15 GMT  
		Size: 10.7 MB (10659994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a3159cada50949b1add91ad02cf36dc8ce5a0b3a89c5e9c114914bcea2aac1c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75868230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a2e40d758d7cbb0286f7ab3e58bced248adfeae72483931e1e4f4cd01dd9d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 09:45:51 GMT
ADD file:2fff7021563ff08bee97c626d3c91410f8f8dc3213b548a7e8b0c351557c7f1d in / 
# Wed, 20 Apr 2022 09:46:01 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 16:46:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 16:47:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:09c77622a2c385ed83fadca4a945b0065fdeaaac427ce2b1a9e795ce2007f8c3`  
		Last Modified: Wed, 20 Apr 2022 09:56:19 GMT  
		Size: 58.8 MB (58835334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ca809b2ea695f0799b00d20783f98ba01ff0027cda46173ed27695cab4b285`  
		Last Modified: Wed, 20 Apr 2022 17:25:52 GMT  
		Size: 5.4 MB (5405282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6df07c738b32af886b9ac59e4c9e9fdf67b4fec93e92eacbcae05a6c9d2c758`  
		Last Modified: Wed, 20 Apr 2022 17:25:53 GMT  
		Size: 11.6 MB (11627614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d6a0f9bd7c4787da40c17d4e498281144c5d5cf25791fe184511c9fc5f16f47f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69113444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b0156979548201802d1561ff427f8dc5e2bef7c1b7dfd94aca6b7afe7bf7fe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 08:39:00 GMT
ADD file:82d4840cdb4b0211b2191ba71ea2698d8dc1b05554d7ed1499aca9cbafaa3fc8 in / 
# Wed, 20 Apr 2022 08:39:07 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 11:14:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 11:14:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:bec7f58dd40ec15934a767db84e5e9b88704cefe60ebe4d7f5abc1583f6c060c`  
		Last Modified: Wed, 20 Apr 2022 08:49:18 GMT  
		Size: 53.2 MB (53207374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3218063f6607544274f51ec8c2c55ce1aded6957be3971daff89994bdda6a2cf`  
		Last Modified: Wed, 20 Apr 2022 11:28:09 GMT  
		Size: 5.1 MB (5140662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be0a6f99a2efe32d3a43fb003ae9ecc029a6ee042cf8dd86a02575641ae1f2f`  
		Last Modified: Wed, 20 Apr 2022 11:28:10 GMT  
		Size: 10.8 MB (10765408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:kinetic-curl`

```console
$ docker pull buildpack-deps@sha256:ba4289bbed606561273f27c806fd846affbd796eacbd8c4cecfb6f2d96318de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:kinetic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:628343781ded2c94ad5718697c35e308a5f311e55d0cdfa5683a3212ef1228b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37871048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5734d54baebbd154ff8e126a96d0562dc73c32d57f5533596ca492663f206b57`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:48 GMT
ADD file:610b4bc612cfad108d07bf023abb796fe6c02a4b6305d824d5d556b7dc85aa89 in / 
# Tue, 25 Oct 2022 01:53:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:42:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:42:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:bcd446fbf8a137bbf135b63332ebcd0c3e9880060bc5b41962fbbb07e94062b7`  
		Last Modified: Tue, 25 Oct 2022 01:55:07 GMT  
		Size: 27.5 MB (27457582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00919c8a5cf1930144d6fd110c137244137a98d7a72e6a12685a879091389d23`  
		Last Modified: Tue, 25 Oct 2022 09:53:54 GMT  
		Size: 6.8 MB (6779535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895cb5b3ae5f27255eda4cb39e4ed45bad1d38cab7a215c9e80ea9d4fcb23d67`  
		Last Modified: Tue, 25 Oct 2022 09:53:53 GMT  
		Size: 3.6 MB (3633931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:861fff831e50b31c9e7118bb3354ac332b2fc19972080eda8d6d0a86f494110f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35624115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13089193757a003a95792f7975893b9695c5030e57b5d80a1b88b89ac848b1e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:07:24 GMT
ADD file:31236ee30d76250acc4fc4bb20966889b0bed2937a5b93700b736696f1e25e04 in / 
# Tue, 25 Oct 2022 03:07:25 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:57:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:58:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6766f7306fe7e1bd5ce2cb35ca97441b04c6499433584c7c2d9948d20267d74c`  
		Last Modified: Tue, 25 Oct 2022 03:10:10 GMT  
		Size: 25.9 MB (25870336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5753e040959444a5794dd2932f0e55c5e23893d1acadd26879e3fd624a332c39`  
		Last Modified: Wed, 26 Oct 2022 05:18:03 GMT  
		Size: 6.0 MB (5953474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10881ecd046e566797823dce068bf8a678690078c366c2bf3bf03251283e2bb7`  
		Last Modified: Wed, 26 Oct 2022 05:18:02 GMT  
		Size: 3.8 MB (3800305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:373a282293140d34f364cb32917ccbfbb1b5657135e1d5b77becf7ec26d57437
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36886502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0532ca7c686b7c5989d673e4c097b51d9fa7759a3b351e18ab993f11252e5d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:06 GMT
ADD file:30361063c284df6e20a85ff95b9c7b93648fe9e04ac935c9ff888e5c5f3af7ea in / 
# Tue, 25 Oct 2022 05:55:06 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:19:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:19:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7a2e58a4bc1e52e3ab8904706a68a79146364ec32d8caf1bd106c3c9966a38fc`  
		Last Modified: Tue, 25 Oct 2022 05:56:30 GMT  
		Size: 26.7 MB (26676995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208c8913a9c66f64a1f5ca1349c8a8b9923f9eb9c8aed25bf3ec160a33e5a796`  
		Last Modified: Tue, 25 Oct 2022 08:36:03 GMT  
		Size: 6.6 MB (6607031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8491d7cc7a42af61771e26652e91532db813e380fa19339f7279420206df0290`  
		Last Modified: Tue, 25 Oct 2022 08:36:03 GMT  
		Size: 3.6 MB (3602476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9144ea52e36fbf4e170dfe335aab6d5de9469737d3055aa70abfbed5e80d33fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44213298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c8b0212d45ff3894e9e1dbc78bade496aa82a9c927fd6b5fd083714d2fa734`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:26:14 GMT
ADD file:60dd11bbfa9f1e2bc613c7f05cbbb83bca9e4b81550b6a0540a5d1d39f870cdd in / 
# Tue, 25 Oct 2022 03:26:16 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:40:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:40:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6d37bc653a986baef621c195bf8def80ca65133b8a3917bbd3a148b31bc1704f`  
		Last Modified: Tue, 25 Oct 2022 03:28:34 GMT  
		Size: 32.1 MB (32099941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc18decfda3085820c97e73c59dba18c534c4455c2eafc5812d29975ad7a9292`  
		Last Modified: Tue, 25 Oct 2022 06:57:12 GMT  
		Size: 7.8 MB (7752006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a931134d9aa21913f6400e3083b4c6955008f9fab7eae04019249a1d912c279`  
		Last Modified: Tue, 25 Oct 2022 06:57:10 GMT  
		Size: 4.4 MB (4361351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8a15a4dc4e2bed4e6c918c30e78a154640305642174809cd2068ea57b92475fc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35438670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cbd0430fb0003ea049701c4e4f48c263db2fd0b465b629c023af10128ceac8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 04:25:56 GMT
ADD file:8b523a4459cfcef333ade98289072a047a1f716565672fbba2b99fa0b7595bff in / 
# Tue, 25 Oct 2022 04:25:58 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:59:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f4447a9c12287b9486384fdda13ff5d2394a84fa81f944b1df82a6c65cacc889`  
		Last Modified: Tue, 25 Oct 2022 04:42:49 GMT  
		Size: 25.6 MB (25621218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc55b17f01e8499ec0532021df7869d72331bb1a3894bd93e3d212b1498e245`  
		Last Modified: Tue, 25 Oct 2022 10:37:50 GMT  
		Size: 5.9 MB (5936166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edee1f55b908e16aef18d4f96c19a0fa263eb259b672dc0e87b32f06e8d90562`  
		Last Modified: Tue, 25 Oct 2022 10:37:46 GMT  
		Size: 3.9 MB (3881286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:75ab25d6d67c72f804bc2ecca53130abb5963b93b91371b24be4f8ab90b4b54a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36121104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644ada4f863420e616b970ac64e228a95ba0993dfbee2c4fb59ad86e50b0566e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:31 GMT
ADD file:9c0c4172b14f0d37b0b074729a4738aeb165efe5c83e2d9bfefc5b39e4a4fe0b in / 
# Tue, 25 Oct 2022 01:23:32 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:44:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:44:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cf61a33f110308ce64c1dd7a5dddf2a5587ee1c8ab2351219b925428957cbc10`  
		Last Modified: Tue, 25 Oct 2022 01:25:01 GMT  
		Size: 26.0 MB (26022178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df11273ce2e4ff8fbfe44b4708e1c3b2323d38c23cc29bfb9935c1788807165`  
		Last Modified: Tue, 25 Oct 2022 02:53:37 GMT  
		Size: 6.5 MB (6473357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36f51f919c9bd6bce882afd5ce69c1de2f32276ae54369c26ae41702ff241ce`  
		Last Modified: Tue, 25 Oct 2022 02:53:35 GMT  
		Size: 3.6 MB (3625569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

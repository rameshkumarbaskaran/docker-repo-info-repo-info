## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:39f8b5331adf3c014e8c332aee6846ff4b25e1ffa54bf14b52fa5f153edca176
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a0fda67f80cb1e5d8d1cf5d332333bedd93fcf88aca088206fc6093dcb0aa987
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69461094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c4dc28e989164cd78109a93eaa7b29e91e386c73864a809029f17e629e2942`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:3f67740cbc1b7fefda4dc75bd2c0f0e76df9ae6b845f37b33cf8eea958403b6c in / 
# Sat, 28 Dec 2019 04:20:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:45:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:45:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3f64e5c246a10532414f3b69dcf620cbf27337d8900089f4139ab3215186e02f`  
		Last Modified: Sat, 28 Dec 2019 04:25:14 GMT  
		Size: 51.4 MB (51358861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a40087c7676442e3d13e8a213aa17fb44a1cbab4d952197f09edac463f58edf`  
		Last Modified: Sat, 28 Dec 2019 05:00:44 GMT  
		Size: 7.9 MB (7919349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce8ee259aabe18e11221885897dc3fc3f8081c56a276bef858633277e6384ce`  
		Last Modified: Sat, 28 Dec 2019 05:00:44 GMT  
		Size: 10.2 MB (10182884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:48e5fc4412ef2c628c395565ad637b817a620e7fee236aeffcc3bc09828a4eaf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66695367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d2457e4cd67547029f6d23fb107bbb539e582f2f8b7a0437772f9a09e4ab5a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:48:50 GMT
ADD file:730d57bac91e32701978679d8ccfd9d70521397f6008ad321414c8d7ccefd937 in / 
# Sat, 28 Dec 2019 04:48:52 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:17:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:18:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a3c7b9678a433c6c2e10ed1e6dc96f81cfce99fe5f71bc8091965c137d50306d`  
		Last Modified: Sat, 28 Dec 2019 04:55:31 GMT  
		Size: 49.3 MB (49328079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775f3daa9663989f7914a385f5db11a26a307dab5f2cd76d08edc09eda570a44`  
		Last Modified: Sat, 28 Dec 2019 05:48:51 GMT  
		Size: 7.5 MB (7490102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebeaaf463e9882767863e9735347274863750c30cf65c8b1a8c8032c9e7b221`  
		Last Modified: Sat, 28 Dec 2019 05:48:52 GMT  
		Size: 9.9 MB (9877186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4485800135235e32142f6b1fb2bfd91352a467c966bb154d33cc7e3649530867
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63836842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d168bad59f4ca35bc1195c3c83feb3ea86e1b875b605cc1f2fd3b3efae5bccac`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:57:57 GMT
ADD file:ff4aac151f354dcf2159847b433d9631b254a18c30cb55390fe848c64ae989df in / 
# Sat, 28 Dec 2019 04:58:00 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:37:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:38:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:aa5ecd1f9158499f6ccdafbcc35abc9cff760ff71453cf163442fd894809336a`  
		Last Modified: Sat, 28 Dec 2019 05:06:38 GMT  
		Size: 47.1 MB (47075322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29564c870b9ddbfdb14447cd65ce79e4a7d90599b8451e5102fbf34b5bbe13e`  
		Last Modified: Sat, 28 Dec 2019 07:05:38 GMT  
		Size: 7.2 MB (7232551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de02b8a9c8996450e899ce5c5cf642268569a23eacfaf79480c1237a0967c76`  
		Last Modified: Sat, 28 Dec 2019 07:05:39 GMT  
		Size: 9.5 MB (9528969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a977adedc92dd45ce7c2a2d1ed858777a6ecf8f9d6d45922d01dc4a7a57ef15a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68303643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9024dfac89929252d3fe29f9bed9f2ad9101a99d5da332f7cc5a7e7a05d2706b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:59 GMT
ADD file:d8dee71c9b462c830ef0fea7e4ea281b8c8ee4f3a1e9e3252fae2401bc715637 in / 
# Sat, 28 Dec 2019 04:40:01 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:58:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:58:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9ddc6b7ca7922f46e5d77becb1dd9bdbfabf5d66b99008799facc91235201022`  
		Last Modified: Sat, 28 Dec 2019 04:46:03 GMT  
		Size: 50.3 MB (50319316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f147f3a8b319f949fb21cc8ef219b5e607881821f497aad9dea6fe7a9a88977e`  
		Last Modified: Sat, 28 Dec 2019 06:19:47 GMT  
		Size: 7.8 MB (7793115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15fd445a2b52a4806ef65aaa42f0fe599f857e4b40277d4740433c4c0e2380f`  
		Last Modified: Sat, 28 Dec 2019 06:19:47 GMT  
		Size: 10.2 MB (10191212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:653b729b75d10ae904611a93e8057ff9c402f40b7d08928d22d10f0fd8b6863a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71105852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f30a330b5abc783d01a5807ebffb0548463186f5abde7f68e8531b9033c007`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:38:52 GMT
ADD file:de81f6da93dbb580dd4c6a23ebd6cef637ab58e6f566e5ff7a217d4def3ed529 in / 
# Sat, 28 Dec 2019 04:38:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:18:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:18:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e3ee43b8971d572beb3640b791c4bba0d66137db2252115ebd9b2bb3ab7704d1`  
		Last Modified: Sat, 28 Dec 2019 04:43:38 GMT  
		Size: 52.5 MB (52480376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372a64d1cd36c22d0befce3fc6f8cba8fa5023d7bd33fc658de98186e128919f`  
		Last Modified: Sat, 28 Dec 2019 05:41:00 GMT  
		Size: 8.1 MB (8091626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ac8412cc2ead4ec139c961dbfca9f633b422edecc1798b4b7057866f1cac71`  
		Last Modified: Sat, 28 Dec 2019 05:41:00 GMT  
		Size: 10.5 MB (10533850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c47272c714df22e6b719e97d6244431fed1df5cb06c2ddb0fa86870ef1130dbc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74480327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a90149e561f31a9b5eb2c709fa684b9c178be59003a035fd5949942aedb23b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:19:20 GMT
ADD file:b4f9e68f81c696fdc52ed16b3080552fa23e19fe66b8de9cb3ade042aac7115d in / 
# Sat, 28 Dec 2019 04:19:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:34:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:35:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b0127e22d45eca52f3501e5b68ef14e0d3a7c0c031138b56d8f69924604af15b`  
		Last Modified: Sat, 28 Dec 2019 04:26:06 GMT  
		Size: 55.2 MB (55181582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8e72dbc0de56d75beeba9cd6882f85d47bb6b3077837bbff7414b67963edac`  
		Last Modified: Sat, 28 Dec 2019 07:19:58 GMT  
		Size: 8.4 MB (8353078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a10090632680817f5ee840a8157c3a412aa82b9db7e41f83c953b68f06651da`  
		Last Modified: Sat, 28 Dec 2019 07:19:58 GMT  
		Size: 10.9 MB (10945667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:45a45496fa6d81af13632b99d5ef7efee76d80d5411f254a287acb81a6123900
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67676607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061469bc6e557997712e2465a0d0322a27e46b8a8b3cae1af6adfa01856dac84`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:30 GMT
ADD file:ef81707ff6f9411444d40f7819b6103572f1c71599afd4c687f5262af6d30f7d in / 
# Sat, 28 Dec 2019 04:41:30 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:42:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:42:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6967537f6d685c8e7bce246638525934908340998b95e5baed55bd5e9805611f`  
		Last Modified: Sat, 28 Dec 2019 04:44:31 GMT  
		Size: 50.0 MB (50017657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5626baeec9661579acdaed4ea6587cae4c16df097bc274ac329b6422d405ed9d`  
		Last Modified: Sat, 28 Dec 2019 05:52:41 GMT  
		Size: 7.6 MB (7590139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc69b710fc3f7e4f96daf59aa3255a7f810b677a869eedde6dc313330d76855e`  
		Last Modified: Sat, 28 Dec 2019 05:52:41 GMT  
		Size: 10.1 MB (10068811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:ee80f9d7a84f519316695f6b35e67e4fc44337df14405c72c1583ae7bdd24669
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1f22e35df4777aeeaea73df67b6fdd64790734cf5d098c9b682319dc2c949e81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71954697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c179e40c225200c4653a3f543e040983aa133979403538dad0ac8de8d77b5771`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:12:48 GMT
ADD file:ba00d13bcd1098159b17d28658733d14360751081a0ff0ae5e599ea2b24d8bfb in / 
# Tue, 01 Mar 2022 02:12:49 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:24:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4e0d8da139e3fe03100d4937bc5abe5a82000a26ba213987f21c101384e663b3`  
		Last Modified: Tue, 01 Mar 2022 02:18:16 GMT  
		Size: 55.8 MB (55764122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d860ac80d90a3973e603f905ad5187aa30b4c4bc1166661080e7b5d70eb9b7`  
		Last Modified: Tue, 01 Mar 2022 06:34:57 GMT  
		Size: 5.3 MB (5275155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439be32a1f7086d86d5df8e4bc94c4e6afe93efcf848747f2a0414cf45ba26e2`  
		Last Modified: Tue, 01 Mar 2022 06:34:58 GMT  
		Size: 10.9 MB (10915420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:08a016c719afb59eb6ae166ae084ac1cc3b06c47b720d10db72c8feb3e95acd7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68917192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020f2f32400ef4c86ba15428ce9760f482c2f139850435fc06d4cf8a7c455817`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:15 GMT
ADD file:1c7800709331eb899ffb3adab213dd035f158fbb5682366917ca9b29bca0df53 in / 
# Tue, 01 Mar 2022 02:01:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:56:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:57:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:73894112358cdc16a19d6f8dc64e5d28dbe24c82ac6079e97e3750913f71a9bd`  
		Last Modified: Tue, 01 Mar 2022 02:16:26 GMT  
		Size: 53.2 MB (53159389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85671ba5fc3ddadb093aa6d64a5f20d876e7de8441908798eb76d8ae77670100`  
		Last Modified: Tue, 01 Mar 2022 03:21:22 GMT  
		Size: 5.2 MB (5174924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1d9a4597c4c1fcff57e018f1450613480d9459062fbda983eb61aacf9903cc`  
		Last Modified: Tue, 01 Mar 2022 03:21:24 GMT  
		Size: 10.6 MB (10582879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:83d0e2b46c70a52e95a07c807f96a53d8dea413470b8b193cbced35050dd9f55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66064217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e3425ae1ece84a216e81a7922d8246d14921d90909616b7d4032a46730d888`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:09 GMT
ADD file:b4dba23a3881b51ce93a5fac275db003c57e88fc4534625e4c57917ee7d15dad in / 
# Tue, 01 Mar 2022 02:01:10 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:23:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:bac975da179fd2ec964b1f0a2374ae27456aefbe28014e1301872aaa7a545619`  
		Last Modified: Tue, 01 Mar 2022 02:17:11 GMT  
		Size: 50.8 MB (50787576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1c6337247740872b2c547fe2c235240cb511f34f377358193108cc09d66ea1`  
		Last Modified: Tue, 01 Mar 2022 09:48:05 GMT  
		Size: 5.0 MB (5035170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1747c607a3fe8511a51023b984fd817a06b714e0a09c5028257ed90eebc47b0f`  
		Last Modified: Tue, 01 Mar 2022 09:48:06 GMT  
		Size: 10.2 MB (10241471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a6d1c1ef9641135a5658e654fc61b78624952caecf01fa5ef05490e66de9f834
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70644316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5873104487d1c52593562f637995429b2790d437e22710d6d733d32471d137a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:10:47 GMT
ADD file:6cc6cb40b70acca2462997590c41a6b84b7434e382c9b14ee43a22dcd7981979 in / 
# Tue, 01 Mar 2022 02:10:47 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:31:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:31:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4ef7b4e27074d58d976b796a4f016999e5977498dbef83e6266727f3bedc89af`  
		Last Modified: Tue, 01 Mar 2022 02:17:12 GMT  
		Size: 54.7 MB (54704495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc4f4f700543c2cb8f09a5e25cea55c5087ffce8b003613f3eab3bcacac0eec`  
		Last Modified: Tue, 01 Mar 2022 10:43:20 GMT  
		Size: 5.3 MB (5263173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41eb0c886efc88379b75421a9b2e06041df5838818e786ffa383c74457975d62`  
		Last Modified: Tue, 01 Mar 2022 10:43:20 GMT  
		Size: 10.7 MB (10676648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5017ad435aafdcf2ea872f2515fa180db4832f9e77dd4f8e5e5adbe1e2a99598
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73515014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845963f985308db7a4d7847da6d5da11fdecc643b2a303d445c0d258afc60a2d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:44 GMT
ADD file:2e2ec9677737b8bd29e3af438e4f72a00e4024d7771df47c835bc532f3955901 in / 
# Tue, 01 Mar 2022 02:06:44 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:39:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:86f9569b4496bcb71f9a06eca983db008f228f89df9115b51deb7ba67bce86ba`  
		Last Modified: Tue, 01 Mar 2022 02:14:26 GMT  
		Size: 56.8 MB (56800248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc642b9c58ccfd6d24ba39de754790979cb5f4259049a1024063ce9ecd8048b3`  
		Last Modified: Tue, 01 Mar 2022 05:50:18 GMT  
		Size: 5.4 MB (5407350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03eabfe59d42c8a3ee934b6d80db7f1185e56951d5ec5a9561133731b6ff2d`  
		Last Modified: Tue, 01 Mar 2022 05:50:19 GMT  
		Size: 11.3 MB (11307416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ff278af3a4f36b82191fe9bca09bd271dcf85b28e4136c1dbf85c1baeaf6c6d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70519128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3c195d2d997cd3777fe09450b75aa8a2489e6f0ba2f1035a3664cdfc732a1b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:16 GMT
ADD file:205e6fa10b349b94cd09f9ab81d41ac5b9cc551f15798915ab0db37a758e13ed in / 
# Tue, 01 Mar 2022 02:01:16 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:57:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:58:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f016bfd811ef5b25e78858421fa083872f3db557018c6de8e9e19a3db5d69e73`  
		Last Modified: Tue, 01 Mar 2022 02:10:17 GMT  
		Size: 54.4 MB (54412288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1db773d06493b0e4fe3289f2a2bab8a332145545a6d356ae31f7c1daeda745`  
		Last Modified: Tue, 01 Mar 2022 03:18:13 GMT  
		Size: 5.2 MB (5232019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55060d22611a46bff620b26ad27b1ccccea40ec3d18f5f2fb5712efa15c5b9d`  
		Last Modified: Tue, 01 Mar 2022 03:18:15 GMT  
		Size: 10.9 MB (10874821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:da70962bf15d882b191030ec80881350c1da32d06e1d77f2cbf4a370ab1762eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77403099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ede6fa2ede1b0333e211d7142ad3fb81a01a889860679f4bf08bd27b189e43`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:03:22 GMT
ADD file:08a06b615cc3142b45e95ffc03be0940c1aed49581fdb5c3a45d69c9ba65fcdf in / 
# Tue, 01 Mar 2022 02:03:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:54:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:55:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e0578def7e304114d931a4e4be85f40364b30cf0228e8360d7ec9d82b30f2519`  
		Last Modified: Tue, 01 Mar 2022 02:13:53 GMT  
		Size: 60.2 MB (60166365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb379d336c1a24b02d5693d3a19fe1017d67c67f734a56c109c876bcf8547f99`  
		Last Modified: Tue, 01 Mar 2022 07:40:40 GMT  
		Size: 5.5 MB (5543531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a933c5a043de953ab3d5444edf590034fecf2a41084159c2ff91dcb57e349a89`  
		Last Modified: Tue, 01 Mar 2022 07:40:41 GMT  
		Size: 11.7 MB (11693203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dba2ccb306a1c947844118fbea5f36cd7f51a83b292b3fc3a5df628ead9ac219
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70071283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba9db32ca4ec339aeeb414b5d2be7f010f0d0c62e922593224da1a4604a7d53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:03 GMT
ADD file:97ccc226b81c90fe178edd1d68832f3a504aa1ef983753f12fed36e4fa09c796 in / 
# Tue, 01 Mar 2022 02:01:10 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 03:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:49:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d7c29f1e9903c84021327567eb513269c7f0b92b6f050037783556a33deac133`  
		Last Modified: Tue, 01 Mar 2022 02:06:47 GMT  
		Size: 54.0 MB (54007195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed9e936b2203a39badf459e13626bb8073e325e33067ce97b014c0f2564b7be`  
		Last Modified: Tue, 01 Mar 2022 03:59:12 GMT  
		Size: 5.3 MB (5256848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11b370eba2faadba4103ab569fe90fa51ac4c8f6634d504e481540d47ad92f7`  
		Last Modified: Tue, 01 Mar 2022 03:59:12 GMT  
		Size: 10.8 MB (10807240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

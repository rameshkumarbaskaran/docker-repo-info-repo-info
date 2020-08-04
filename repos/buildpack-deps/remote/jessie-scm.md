## `buildpack-deps:jessie-scm`

```console
$ docker pull buildpack-deps@sha256:3408c5a37b7fae6f613610f44047a5676a94de9d117401913c0f059c614f8dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:jessie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c06e5f9d977b72c6bc64cf3ea369aa7420f585910b2142099d8c17851145c953
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115269132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de69cc278717cf80139e3384075b58b98e952d0634d333b955a244984cafb034`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:57 GMT
ADD file:c7289562291bdeb61e0423cc6f7c93e71f1db0631093278de35bccc99ac0137d in / 
# Wed, 22 Jul 2020 02:03:58 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:04:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:04:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:06:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e58952790bdd9e11086d30293a8de4ff1b9960b3ef414cfb7cfe6283010d156c`  
		Last Modified: Wed, 22 Jul 2020 02:10:14 GMT  
		Size: 54.4 MB (54388443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2ff14f8a79fc9f0751ebbf0b42f16b01a3167518a5c32a36f03e616a037af0`  
		Last Modified: Wed, 22 Jul 2020 03:17:30 GMT  
		Size: 17.5 MB (17545946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c48eb095f4e23bc343acb9f93e42c07047a4cd3b842658d4d0ca5bd0c1c4d9`  
		Last Modified: Wed, 22 Jul 2020 03:17:50 GMT  
		Size: 43.3 MB (43334743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fbb77087517328191efc62969936f96711c366e67a5591bdaebdbac28381ebe0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110777102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca0abd07c745cc1eaaca0e2d33a61f24d79c042db14b751c90963bc56f0ea09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:14:10 GMT
ADD file:c7cc2243f2c8784e78a2e6bfa6e0d96e590093564a380d437d171d192f6ee21c in / 
# Tue, 04 Aug 2020 03:14:20 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:18:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 06:18:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 06:19:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35595d63dba33c63a7b9cb31f318a3ac9a96e3da166a6db28d65c2128b9fc3fa`  
		Last Modified: Tue, 04 Aug 2020 03:34:38 GMT  
		Size: 52.6 MB (52583710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a98c2c543d779c2f88f1c25143bad4c0432ac10d0bb6a5f2c62f722949ef57`  
		Last Modified: Tue, 04 Aug 2020 06:38:43 GMT  
		Size: 17.0 MB (17037316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499da6ad6050a2f850169782cb006bad2e835107f058a4840f8eee37d855215b`  
		Last Modified: Tue, 04 Aug 2020 06:39:06 GMT  
		Size: 41.2 MB (41156076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:642c036543bb60bdbdf7759098f805a88228d40dead33e5b5058d2c851d894a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106808130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda8154f51a5cc1a08f7b81a96c8636ef5a14391b204e2cf4ed797ebf876c5c4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:20:52 GMT
ADD file:fc97a5157392072f2e584533bc20a7c8565d3ab25811c37aa8b0be0d2772d001 in / 
# Wed, 22 Jul 2020 01:21:05 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:34:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 05:36:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23856a2fcb20620043f7afa719e5733743f2f68b019438dea4617813e12db79c`  
		Last Modified: Wed, 22 Jul 2020 01:40:57 GMT  
		Size: 50.3 MB (50305246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71e2d521b630caaa42f6e89b0fcbe65a9c6841a05078ba147410ee43faf4e9a`  
		Last Modified: Wed, 22 Jul 2020 06:03:43 GMT  
		Size: 16.7 MB (16723465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431287079b9de87676113f46b63c388b0863d730e7c35fb4947ce0fe35e26392`  
		Last Modified: Wed, 22 Jul 2020 06:04:06 GMT  
		Size: 39.8 MB (39779419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5e7f0dcdc5e8a73615b254c55651361a951583c866d471acad200e303b2a80f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118455147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ed518933aebb33485cbfdefd4f0f03c3f06574e9ab7c04a8e8ce7792c0a248`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:09:33 GMT
ADD file:7daf3f651c76cffc9df8609ab9c201a868bb0b25716eb7d7cf929b036d05b8a6 in / 
# Wed, 22 Jul 2020 02:09:34 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:24:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:24:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:00b5abd6cd880905c210361dac76afbea3e74aef0d203bba4e663196cdbb89e0`  
		Last Modified: Wed, 22 Jul 2020 02:16:06 GMT  
		Size: 54.6 MB (54608798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336722d46e9c737ab1215cf606a080c9c4c07c1c16635127f97d8d3b2f534dfa`  
		Last Modified: Wed, 22 Jul 2020 03:41:55 GMT  
		Size: 19.9 MB (19855800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf8f09aad23c87f45388cc1b2f254074664c3aff8780c5bd8d558ef63a8ff54`  
		Last Modified: Wed, 22 Jul 2020 03:42:22 GMT  
		Size: 44.0 MB (43990549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

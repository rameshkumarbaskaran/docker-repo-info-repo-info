## `buildpack-deps:jessie-curl`

```console
$ docker pull buildpack-deps@sha256:1cb7ae21c7236c0fb0e80db35c4400b6f40491d436e0b7668e62a2c9a8286adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:jessie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:17dfcabb2a4a4464e35359bcd848e4a1001b547cd9f0c02f56ef41656f1a2c82
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71934389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2cc608a66ff08e51ac8d7c80b4565dc380e69d9e4b088ab84aa6787d3db03d`
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

### `buildpack-deps:jessie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fdda44af34e870a36b347a8429b2f33062b331c3d4fb66d16d245b601e5d3e73
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69621026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fb9d2201d7764deba7176852d9e3997e0627324300550791a9cc9a1137735e`
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

### `buildpack-deps:jessie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0b5e8a6ca97c3aff1fed945511e0691f929fe6b24f4894a744f5cf24e14f2a51
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67029209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69b8ac770fa5d75154c9c19fd5220e1adb0f808963d1ebd2efa4ebcc1b6a032`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:57:16 GMT
ADD file:1b4bf8acda0b906341b6a17ca6eccc23744ba196c78c5bc59c3e26d0b2ebe596 in / 
# Tue, 04 Aug 2020 04:57:18 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:00:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:00:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7c58b357cec76336de1011b56cc2999a53017c6a4b3cf93f2b8362b7a055c544`  
		Last Modified: Tue, 04 Aug 2020 05:05:41 GMT  
		Size: 50.3 MB (50305564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64410aa4323d878bbe3be9802befcd90ffd5681624e0e325a80f25a038fa6cc`  
		Last Modified: Tue, 04 Aug 2020 08:27:38 GMT  
		Size: 16.7 MB (16723645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:16105a16604350bb9c9e6af8794a31002bccb2361948c826312f9ec020f05f9d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74465547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3583ac4ed99b91acbedfa812161fd5a17896579ce565ffc63aa49ccb0cf2a36c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:37:49 GMT
ADD file:85c105a2f2f0c7bff57c73bff9ecdb5ae2cb04074a0129fc1a82d4da85b95ec0 in / 
# Tue, 04 Aug 2020 03:37:49 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:11:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:11:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:49a2d30c774cb18fa05d4cb6f730f97f4965b1162debd13f35bf1733bb737735`  
		Last Modified: Tue, 04 Aug 2020 03:42:50 GMT  
		Size: 54.6 MB (54609569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb76cc7bc12f41ea0e34f0355c0a2d2c5689a14b42947760e1caf7b92ff80dc`  
		Last Modified: Tue, 04 Aug 2020 08:27:50 GMT  
		Size: 19.9 MB (19855978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

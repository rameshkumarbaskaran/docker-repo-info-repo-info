## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:dcd7e260640ab11dd2235bc8ca9242dd42c9d10994ccea2ab5d78b9af137a855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2d1fad71b9a2a63643749a5be6c277f5d1c2627f8c9692758fd89cd01df96009
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68077148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d3fd9d03cbd0a02fb4b1a5950fcadb0e3fa6bf63c6f258be5ac01a6a473667`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:23 GMT
ADD file:d9c3e291731c1f06d615709ebc665a41f6d6355607d87ae00768e3be4b330bed in / 
# Thu, 07 Sep 2023 00:21:24 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:59:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:311da6c465ea1576925360eba391bcd32dece9be95960a0bc9ffcb25fe712017`  
		Last Modified: Thu, 07 Sep 2023 00:26:22 GMT  
		Size: 50.5 MB (50497598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9bf114588c05b2df612b083b96582f3b8dbf51647aa6138a50d09d42df2454`  
		Last Modified: Thu, 07 Sep 2023 03:06:52 GMT  
		Size: 17.6 MB (17579550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9d3666a56a52d9bfc5bec032f72926721990f842082d784c9b76e3567b403e4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62177989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0eefe026c34ec614b777f3133eb2299e885a329265d9f0d2562312fd64f4216`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:58:19 GMT
ADD file:7ec242a3962c31a67f54c602b7f422709b35916aa381a646dc41202360549761 in / 
# Thu, 07 Sep 2023 00:58:21 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:37:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:719d9383401f642312dab568888c86aa5069040b61dbe32fb40d5a7bc5fd5c02`  
		Last Modified: Thu, 07 Sep 2023 01:03:31 GMT  
		Size: 46.0 MB (45966117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2da04a998e4694d1b45ec9b56798040834751f733528e18fb5bffc24059f83`  
		Last Modified: Thu, 07 Sep 2023 01:47:14 GMT  
		Size: 16.2 MB (16211872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:693fba8369c38b01ea7646361a202296d268f8452d59f1622d04534bf8363085
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66741963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da913c23eb14e30f7e30aaada367ad899839db75c2d632e31b6c1d7ce8752659`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:18 GMT
ADD file:366546a703fa234d38591d2a54f10fbced83cc0e407775ad31751f0111c348c8 in / 
# Tue, 15 Aug 2023 23:40:18 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:24:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:745797452665e0b4d6f5d0f9b05ae67a86bccfea4ec3a2cf7c6dd89cbfafdd37`  
		Last Modified: Tue, 15 Aug 2023 23:44:16 GMT  
		Size: 49.3 MB (49290964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d4e21e88dbd3e72136906f1d37cb7c9b29c4a4c107fbe1c8b0385f5e663d2e`  
		Last Modified: Wed, 16 Aug 2023 01:40:15 GMT  
		Size: 17.5 MB (17450999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a2f6bc9bc0541882d918d0b6b577d0fc0176c4f25f15e3c1991d4650171fb292
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69351416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e1f222da00d74c27c7fc35eef2dacdd3f2a6c346602e90d5b74493308eb88e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:33 GMT
ADD file:f985eed393788dbeb3e4d9ab7f77d632d72f60bc5da30c59bb7de8fa3de0681c in / 
# Tue, 15 Aug 2023 23:39:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:29:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ce293edb9c35c6521b0a7d87a0d8e0252e4b0cab665a3103cb6d06e3e37cf414`  
		Last Modified: Tue, 15 Aug 2023 23:44:33 GMT  
		Size: 51.3 MB (51255460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d7c3776eae51e29722c4381d59391e00b49339c7298dcbef6adffe94829182`  
		Last Modified: Wed, 16 Aug 2023 00:37:17 GMT  
		Size: 18.1 MB (18095956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

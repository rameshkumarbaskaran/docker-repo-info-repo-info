## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:ce131e54ff360dbf8207d47064a01dea7c9e07f644b48f5500ae0c8f97e25a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:694e67b054793477b5cb90e7e9f504d18616719471c7fa9acbd0e464ef762680
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115269105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6e780ddb8590e6e297a5f26adf79418d021b32ae6c3da0d6922f4b1fb0077d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:24:00 GMT
ADD file:ca64ef47722e4bf4beeab729a34cd854fe7293a0a2a0a2a92e6f1347c071dfe9 in / 
# Thu, 10 Sep 2020 00:24:01 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:03:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:03:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 01:05:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:290431e500161a90ac38ac8631791acb27e14a913613b60b3df58f839168df40`  
		Last Modified: Thu, 10 Sep 2020 00:34:21 GMT  
		Size: 54.4 MB (54389019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcaf1dd00a337044e2c0421947b13d7390883ef55a08ff9ea58d13ce59784328`  
		Last Modified: Thu, 10 Sep 2020 01:16:59 GMT  
		Size: 17.5 MB (17545982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478d2f36706aba42a38a1d269f4e5f9e733730c04955e96a04d508b1cd9d589f`  
		Last Modified: Thu, 10 Sep 2020 01:17:17 GMT  
		Size: 43.3 MB (43334104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5661f9fcc212db92ccd44eeb7f5238fd0bb4e860bffb5f8e3bcd5a2a85335df7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110776885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407674c93506eaf522e0df62a2e3bab72fc66d7927f3acc8b5f53b0d977d15aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:15 GMT
ADD file:b5770ada526014c416df31779f0c640c62a5e53e8e018a6201d507999ac34e18 in / 
# Wed, 09 Sep 2020 23:54:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:37:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:37:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 00:38:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:82ebff95f0e21d655344637482b367c7ea0db41b80cbc667bd980d2141287029`  
		Last Modified: Thu, 10 Sep 2020 00:03:15 GMT  
		Size: 52.6 MB (52583713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f40e46cda9c751ff385c796d48a3c39740220c3885866739fe62640f9437afa`  
		Last Modified: Thu, 10 Sep 2020 00:55:04 GMT  
		Size: 17.0 MB (17037321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bd6814b5011e45af4aaee011465ebcf614eef4d29dab5a87d8a3fed3655f0`  
		Last Modified: Thu, 10 Sep 2020 00:55:28 GMT  
		Size: 41.2 MB (41155851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e17c2020dbf8828a078684a316196da9063d77bece5fc4f768671e18c68a1651
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106808650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719e6f894fff207d8dca57c13b33088cda6bf7001b30a59fdd1b17ba986e88d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:08:32 GMT
ADD file:6c1ccdfbdb357c0b130cfe85bd05903e56f365e3d93c21c70339151862d2897a in / 
# Thu, 10 Sep 2020 00:08:34 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:44:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:44:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 01:46:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3bf2610be79f89db91594c41fa743370fc433e9e9898fa5d42098ba30efd7f9d`  
		Last Modified: Thu, 10 Sep 2020 00:18:15 GMT  
		Size: 50.3 MB (50305547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a9c931dec194117f2ee5eecc8d09f5847406d2a176f0a7256b132a77174e42`  
		Last Modified: Thu, 10 Sep 2020 02:03:12 GMT  
		Size: 16.7 MB (16723607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b2690d60f65f38c5edeeb9ff525bf34649d4aeceedc09723b56dda737b2f6`  
		Last Modified: Thu, 10 Sep 2020 02:03:33 GMT  
		Size: 39.8 MB (39779496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:33a5651955648be20db0ee703ffa62815478d81902af2576a0d9a5b2c90cafda
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118454923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209c1e740e9164d532eedef46adb578679ee18f2e0d1158e35ea5fc5517d7b99`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:37 GMT
ADD file:b8a03a5f95e2490a27b297173fd17ea8037e2db6c1619ac9e84d781ff97ecba9 in / 
# Wed, 09 Sep 2020 23:40:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:54:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:54:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 01:58:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a11948377c3d4859427c8f59e5f3716e2aba1cb63cc4e9dc8807d8e647dc118`  
		Last Modified: Wed, 09 Sep 2020 23:46:47 GMT  
		Size: 54.6 MB (54609479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bc82823dc8235bc61ea05f4d8421c65972757bede832556e79ce352c099f4`  
		Last Modified: Thu, 10 Sep 2020 02:14:34 GMT  
		Size: 19.9 MB (19855914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f993ff77deba249612d2a2fe059efb48af19e36b5559a641be9a95dfd9acb67`  
		Last Modified: Thu, 10 Sep 2020 02:15:01 GMT  
		Size: 44.0 MB (43989530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

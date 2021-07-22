## `buildpack-deps:hirsute-curl`

```console
$ docker pull buildpack-deps@sha256:9be15df0caf6ac0b8f8ae58f95917619bebcb9d63380168ea47fa15502cb7dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:hirsute-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6fd19e6c640b735553a801a651a84d7f96f2e9116b4254cc05b12414cd843044
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40931132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1a7dad1899e0bc50c801997cfa4e432dac17d2060b3e2895d5c813d4def8fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:57 GMT
ADD file:af305d3eb867f312743f97d1cbed14ee2a155fdfed4621c72a8e8cf25355660c in / 
# Tue, 13 Jul 2021 22:29:57 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:35:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:36:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:966b3c5c8637e41360eed39a59e6c16ee1e986f7f2b92244e4d39f7ca6669618`  
		Last Modified: Tue, 13 Jul 2021 22:31:57 GMT  
		Size: 31.8 MB (31836858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a04a01c24f99b40c331ead5fe266437c7e8f9792a150da4220010982073489`  
		Last Modified: Tue, 13 Jul 2021 23:47:46 GMT  
		Size: 5.4 MB (5431774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daefe3fcd90dbd594dc34d343456aba2e06f2154410b341785c870c71e553a7b`  
		Last Modified: Tue, 13 Jul 2021 23:47:46 GMT  
		Size: 3.7 MB (3662500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a73e9688b934342a0bbddf43487cb141a29662bb29c3c0b05cc75bb6136c988d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34850679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dcdd4a442f3d0448a5592ab1bd5c4f202413a320c26c0140143afc4e032ef4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:58 GMT
ADD file:5175798ab209bbc3941a05787751ecf9e7ba0b4e9cda31b044bd6d75e25976c8 in / 
# Tue, 13 Jul 2021 23:21:59 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 01:58:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 01:59:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:fb746c2c12b45d26860f880a6e953018e4e9b83f9de17d11528fa484e1eb0f9f`  
		Last Modified: Tue, 13 Jul 2021 23:27:31 GMT  
		Size: 26.9 MB (26853751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eece18331508c76042ad235a876e23b49181f5ec1a12bc249810a5c1054ecc4`  
		Last Modified: Wed, 14 Jul 2021 02:21:44 GMT  
		Size: 4.9 MB (4858455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ceee6719a049da986bf7137392215103a2329991689f89b7c21e4d6c154ea0`  
		Last Modified: Wed, 14 Jul 2021 02:21:42 GMT  
		Size: 3.1 MB (3138473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:464f711f14fb218568e3a6235b4308f85528c10bd0ac25244489f9d33311c9b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39339182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742d55ea1750bc33fba1db963e1b6317e4461e3a61557d53f2886d6511189706`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:46 GMT
ADD file:9e964afafcec670390a354fe9412da078ea83c247037612ce2b4c00c025cb4f1 in / 
# Tue, 13 Jul 2021 23:01:46 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:54:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:54:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cfe8b2632f122e3d77487867f2d08211ff277e78f8cb07a44832e91dd7c09ad7`  
		Last Modified: Tue, 13 Jul 2021 23:04:18 GMT  
		Size: 30.3 MB (30297903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e729df8790411dd4b5d51402271f41ae54c66f21fab7d27a85128c28afbc1c86`  
		Last Modified: Wed, 14 Jul 2021 00:04:10 GMT  
		Size: 5.4 MB (5403289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4509723cca5717dcc263c340e8d2352f8f9c3473762a6f85c71a50891715ea65`  
		Last Modified: Wed, 14 Jul 2021 00:04:09 GMT  
		Size: 3.6 MB (3637990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a776beac2f717fb88809919c67115f318ac57c8ad35f12cf3d65a0d5a1850c9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48008967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbfa37d941b779588d50f51ca324858e0cb922e1ad66acc3d2cf44ca055c3d7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:07 GMT
ADD file:20ba7c85b0d967e38fdb53a91f37ff0266687978ecc0791861d4d1afb8c79899 in / 
# Tue, 13 Jul 2021 23:23:15 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:38:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:39:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2aeaf089064656dca36cf8480e9c7933a8c61fcc2a4c009ac61cbe442299cb68`  
		Last Modified: Tue, 13 Jul 2021 23:28:23 GMT  
		Size: 37.4 MB (37353027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e56fc28c2da5e76c5798bfbc3de1f85434a42d191df7391b5ab1329ea4f8953`  
		Last Modified: Thu, 22 Jul 2021 05:22:49 GMT  
		Size: 6.1 MB (6132655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9375a3d4e03a069ebacb822be250889976e19ca796cf3cb46a35c232e7b684bb`  
		Last Modified: Thu, 22 Jul 2021 05:22:43 GMT  
		Size: 4.5 MB (4523285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a38dbf3f42d698f0ca17e73028a3dfd80e741ccc13bb933abf8d13c1c555bb6d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42685813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23110081a69b5d65ea81f1816558ddd575b9664d30730b257125d62e34dc2c6d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Jan 2021 04:02:00 GMT
ADD file:8ec30abb851d24263f13b8ab93a9889626368053d325848b2f951e43ccac9a0c in / 
# Thu, 21 Jan 2021 04:02:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 04:02:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 04:02:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 04:02:12 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:25:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:35d604bd00566c6cbc331e49db9228af41b973581b365975622efcddfda24580`  
		Last Modified: Thu, 21 Jan 2021 04:04:14 GMT  
		Size: 32.5 MB (32534356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8645fe124321a0a9ceca773d8bd654c8edfb63087f69654dc33b005cd936031`  
		Last Modified: Thu, 21 Jan 2021 04:04:09 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811acaaa59ef2c29c645ec90173a876498cec8129d2051e6826881ba068508fb`  
		Last Modified: Thu, 21 Jan 2021 04:04:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c0a035e1b4479247e30498cb38c95743838097221a8aafc70ede4da8e1b6bf`  
		Last Modified: Thu, 21 Jan 2021 05:34:30 GMT  
		Size: 5.7 MB (5691508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476bdd8305678676c465817a601000b79a702ef2feb7d9fc199dd171304f9712`  
		Last Modified: Thu, 21 Jan 2021 05:34:29 GMT  
		Size: 4.5 MB (4458912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

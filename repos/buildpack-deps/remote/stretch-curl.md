## `buildpack-deps:stretch-curl`

```console
$ docker pull buildpack-deps@sha256:a3529686d9532b2eb258f48b0ff0c9ccd481b440ca2c542b22cea3536672c493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:stretch-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9ce1b7b85caf88648072d6dcb6b754a3acceacd9da70ef4fd3ed86cc3793a140
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60459778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5e9e50742948630fc6ff4afc3ceabbe452af06111427a6107b7420734346a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1bc6846b475c0c950671b6ed83fa67e9c232b27a29b0f847ab7fbd8b21b408a0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58064680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ba39d4b74ef7fdb7f04fa95986c8951984ed6f7a06d70e72993d0a96e89182`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:23:56 GMT
ADD file:c82979276574ae052b356c92955110dfb283d33659ea097871176d1a62ed98ff in / 
# Tue, 04 Aug 2020 03:24:04 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:29:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 06:30:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8653f8cd9e4c7c5ecd1cd925507522d43ec49dea7127050e56d71d3447f39292`  
		Last Modified: Tue, 04 Aug 2020 03:38:23 GMT  
		Size: 44.1 MB (44081220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04472d0cf19492fee43c5b2d567c58a8db05101bc378a4f87aeb6dbbf7d953b8`  
		Last Modified: Tue, 04 Aug 2020 06:41:42 GMT  
		Size: 9.8 MB (9824577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b057d6a311b4078c040c92aa3f3f070583b89400a46547d07c690bedd9bf535f`  
		Last Modified: Tue, 04 Aug 2020 06:41:40 GMT  
		Size: 4.2 MB (4158883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8780e8945b73f7e9bff64741cbf7d671192e9a73baf2eef43d0fec25669ee7e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55470069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cc3c25b30ad696d46dff7a0adc2614bc491c9f5a861aca25d11f79ccdbf620`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:32:02 GMT
ADD file:762e52a5e1d8ff2daa22c3bec2cfdfe4cbcf224deb1e73d7db3af0cbf5658785 in / 
# Wed, 22 Jul 2020 01:32:11 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:50:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:50:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:05dc12a0df610a09562914533797508b791bbd115ae17b6a1b75666ec90263da`  
		Last Modified: Wed, 22 Jul 2020 01:44:04 GMT  
		Size: 42.1 MB (42107480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b998b2d4ee2005b0f51e94b6fc7467091e54a910491e7873b9e0d6f59aabd98`  
		Last Modified: Wed, 22 Jul 2020 06:06:37 GMT  
		Size: 9.4 MB (9444083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15230f55c10a543d54564a792784b1d2e133d4edeadd58978682d9bf02d1425a`  
		Last Modified: Wed, 22 Jul 2020 06:06:34 GMT  
		Size: 3.9 MB (3918506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1a768b0d9170ec14cb11fa310a8e744bebc613c54d74dab5e91d610588cebb69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56964060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769476cf4c13fbebd1378084305041ddccefc402bfdeb51d7014c444a252f518`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:43:42 GMT
ADD file:9c5c9df9952cb51291333837bdb462bbdf9f157e91e616f1e3fb8d2fcb1a1983 in / 
# Wed, 22 Jul 2020 00:43:45 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:26:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:27:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ad4de4f68e9c2c0f5e5e62d379d936bb88ce467505ed002fb1e10c434fefe90c`  
		Last Modified: Wed, 22 Jul 2020 00:49:52 GMT  
		Size: 43.2 MB (43169407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05aedd313900c1f55a004cb5b8a8b93ee320b25c73286390f0669f387fd96c47`  
		Last Modified: Wed, 22 Jul 2020 01:38:43 GMT  
		Size: 9.7 MB (9700532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2bc27f6e0cc82b950064aa77aa261962e402cb805c2c36bef0ece1371fa405`  
		Last Modified: Wed, 22 Jul 2020 01:38:43 GMT  
		Size: 4.1 MB (4094121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:13cbad1357810dbe36386d823cd3fe09f8902f812f7b9e146ca27d3550b9944f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61428273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7451b3bcaa027e0b584a62ce6b96ba228fcf090297573039f162707c970fcb5f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:12:18 GMT
ADD file:d3f4f838251f30bbb4c033600c18e4c1065e310959dc105d22c6df709decb369 in / 
# Wed, 22 Jul 2020 02:12:19 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:34:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:34:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:48006630f132977bf4db68efe0ddd39191244134bb38b95a1c28b7cc6ce01157`  
		Last Modified: Wed, 22 Jul 2020 02:19:12 GMT  
		Size: 46.1 MB (46092998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55841d4427f3f7db211f0ce8bd00aec32e728961c97fd5c1bfd5c3f9ed73630`  
		Last Modified: Wed, 22 Jul 2020 03:45:32 GMT  
		Size: 10.8 MB (10774080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3f8c22b21a978b42daa813da3020469db274995a267599d278e2c6a196eb6d`  
		Last Modified: Wed, 22 Jul 2020 03:45:29 GMT  
		Size: 4.6 MB (4561195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

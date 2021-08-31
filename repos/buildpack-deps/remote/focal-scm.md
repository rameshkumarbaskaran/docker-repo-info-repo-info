## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:367cefc669c892258f4ac6385b21eab1806001040a125a3b2413ac7c22ed8a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8b8b97d300d1bc88549237ed88c7cdf64686a1328ee3a4ab78fbdd1ef5f8da2e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100684450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c974b9e6e210580e3ae60d84424224f343c342c509e2c10ad8648f3bd6123cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:52:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:53:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 02:53:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1af8c8529138158c1ab9fc21b416a8348bcd120814c9105e5671a61366f1a4`  
		Last Modified: Tue, 31 Aug 2021 03:12:49 GMT  
		Size: 7.8 MB (7771403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0df72f91f5e22bfe2c01836dcbb5cded6ba8b11975958672f924786ad44d121`  
		Last Modified: Tue, 31 Aug 2021 03:12:49 GMT  
		Size: 3.6 MB (3624569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de940d7df01050bdb7ed77215e5c4ab341f72f7375f15a4463755ab286bc27f3`  
		Last Modified: Tue, 31 Aug 2021 03:13:09 GMT  
		Size: 60.7 MB (60718404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fc96eae5b17a1509ebd86aec2fc4f5ab815303f932dee306ef7d372ef9d27f73
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89395289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2592dcde1e1046cc64d12828ff8273c7be8298f1cd34cdb716f3b31771c3187a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:52 GMT
ADD file:f9dcf17ef0f45719dff5ed961907d78a1ea6671fecdb434536f3fc8cf15fbb3b in / 
# Tue, 31 Aug 2021 01:40:53 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:14:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:15:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 03:16:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cccc98128e2b3db00394b4e59c3f674a52e4b861786d9fab388357a88fc428a2`  
		Last Modified: Tue, 31 Aug 2021 01:44:57 GMT  
		Size: 24.1 MB (24068823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c22e0906b4cd7dbb582181e7accbb483c55c760bfd4b2b06e28360279752f8`  
		Last Modified: Tue, 31 Aug 2021 03:35:41 GMT  
		Size: 6.8 MB (6768939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32fb178417438073a96fd01d75df3f32b76e8f1fb7b8dda7e693977a8025b43`  
		Last Modified: Tue, 31 Aug 2021 03:35:38 GMT  
		Size: 3.1 MB (3103787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0210be10f1605c0377e7fff7c8b6f3da7e7c69e756087b20718b4627035213`  
		Last Modified: Tue, 31 Aug 2021 03:36:34 GMT  
		Size: 55.5 MB (55453740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:19b36271f8dc3c3e32d2efe26aee8d1196a466b9e9daa03445d90e2db344a923
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99176541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88006fc39d950f9ac4bcaac8419a7dcf84b7b72b94bfecdf46a55135c344309f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:10:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:10:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 02:10:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1b8ef0ef6610d6e720afe76a3df03bf2afed7f16cc8b12dab2279c75b1c408`  
		Last Modified: Tue, 31 Aug 2021 02:19:41 GMT  
		Size: 7.6 MB (7636852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a226690073506846a68b797c6c96615eec776aefa661831f4abff3715172704`  
		Last Modified: Tue, 31 Aug 2021 02:19:40 GMT  
		Size: 3.6 MB (3600358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d5c6943027b3d6294ec2bbad85003c7584f70a77a2b64b363ee36bbf30920b`  
		Last Modified: Tue, 31 Aug 2021 02:20:04 GMT  
		Size: 60.8 MB (60766232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3c557088facf8e21f8cb162d5da3b29b0b4d22b7978c6e5330f1abcf4069d200
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115856069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81f3ab03184adf9e5ddbbaaf4424797d4ab33a9a2a2acc21b05608758876dbd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 03:08:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 03:09:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 27 Jul 2021 03:11:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53f198532bfc08536f5ad0c1f1242b55d34d7aac9ce9dc059a6109c2d7e20b7`  
		Last Modified: Tue, 27 Jul 2021 04:23:58 GMT  
		Size: 8.7 MB (8722787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8f157ddc9f96bd79c6823da12b4c54366d23b79691f3d8f39665ef321ff86e`  
		Last Modified: Tue, 27 Jul 2021 04:23:57 GMT  
		Size: 4.5 MB (4456512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a51a75aca451f998a1dcf27f7a8ece4fb2c2aaf4f7a09896e4664873136d52d`  
		Last Modified: Tue, 27 Jul 2021 04:24:25 GMT  
		Size: 69.4 MB (69386343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:87aef79db204a762d5f40f658ce076db36ab3efc621aa006c6405230ae43653a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98117720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b46e24901559406cd7200c4359b8f96650d7eb96bb6cd9a829fc4b415f1ad1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:42:23 GMT
ADD file:979855f79ebaca36cc7878f71b2326f1cd189970fdb223b37cd64ee12d1c9a2b in / 
# Tue, 31 Aug 2021 01:42:27 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Aug 2021 02:36:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fbf86d355c92d30b8de4c0360b0d79e1100e392d0885b6b5b302a1c3781dbf1`  
		Last Modified: Tue, 31 Aug 2021 01:44:13 GMT  
		Size: 27.1 MB (27127470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748dba3041b2bd31a240176639b763492a369d59b429da56c854b823820b27b3`  
		Last Modified: Tue, 31 Aug 2021 02:45:59 GMT  
		Size: 7.4 MB (7428812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e0c13c39c1426302723ee65c5c58538ee64cf9d25b9629ac690cedd2a7169b`  
		Last Modified: Tue, 31 Aug 2021 02:45:59 GMT  
		Size: 3.5 MB (3542143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80abe2f24b0566481303d246a8e9996957224b079b7ff282fae87f647409e82c`  
		Last Modified: Tue, 31 Aug 2021 02:46:16 GMT  
		Size: 60.0 MB (60019295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

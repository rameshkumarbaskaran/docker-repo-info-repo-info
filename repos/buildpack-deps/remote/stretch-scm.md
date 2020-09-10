## `buildpack-deps:stretch-scm`

```console
$ docker pull buildpack-deps@sha256:3034917682e138821fe2ed7768edf341e9a64772e536a5865d2f6405cd618ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:stretch-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:39115a22852d8ed38f548270a91c72de6fa04e33c31982f1e63c4c89744a4cd1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110567898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a40598a74c69356227d0be06c257e6e98e8f731930e6fd31a457c92471a11f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:11:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:11:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 01:11:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b49aa113642e1d83773ca83de882e12c4981ed565d47b4c7da998855ad182e1`  
		Last Modified: Thu, 10 Sep 2020 01:19:16 GMT  
		Size: 10.8 MB (10750802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159512f4cc2a5f8c64890a32b7766e2662b61241ef585cc28daf194bccaf1c1`  
		Last Modified: Thu, 10 Sep 2020 01:19:14 GMT  
		Size: 4.3 MB (4340512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8439168fd8dcb35b71c06211b4c23c02bd846e1d37f72cfe5638ada30c196556`  
		Last Modified: Thu, 10 Sep 2020 01:19:35 GMT  
		Size: 50.1 MB (50109858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:61054b992af2822bbf629fb6eb5a6a5001a140517b028189bfe0051f79b1637f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106369471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefab29bda40eff68555beb5089ce0b04e7d4a443d94e10e9973376a5a8bf621`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:58:16 GMT
ADD file:39312a9e824bd7c6ad3eca3ada9e922d8f7219c51e10047672e9ccab3dadb248 in / 
# Wed, 09 Sep 2020 23:58:18 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:47:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 00:48:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301ffd407a7ebea8722c85a0474f1c621b0785275eef7a32a1ab7b5106a8e762`  
		Last Modified: Thu, 10 Sep 2020 00:06:45 GMT  
		Size: 44.1 MB (44081297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3c7b013af3cd7da74fdf184d75df567c3ba56ee21fa571230b433477d588a2`  
		Last Modified: Thu, 10 Sep 2020 00:58:19 GMT  
		Size: 9.8 MB (9824691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f78c2d8a2a251c2677baf2550b75f26e68595aaeefd369b10dbeb6c4a8a76e8`  
		Last Modified: Thu, 10 Sep 2020 00:58:17 GMT  
		Size: 4.2 MB (4160081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaf49af0025cf63295d41c39b9a75e9e4adb695cfe41f26eb93f8801ee772b2`  
		Last Modified: Thu, 10 Sep 2020 00:58:44 GMT  
		Size: 48.3 MB (48303402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1c50398f579ed7f583ff29e45584569a9800ba497d03dda03863ead873198848
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101889271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4686416266ee77cd4adc6e94b3141f3759b33e3911f467af94b93fe34ef2e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:13:17 GMT
ADD file:3da15ca153ab01cc777bb2a828e1097edc064f49012d96e9b0789cc4cbe9c205 in / 
# Thu, 10 Sep 2020 00:13:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:54:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:55:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 01:56:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2dc31d01bd52bc4550017dd5cb9e295a7998fbfa6b3ea3f612efb5da666b3600`  
		Last Modified: Thu, 10 Sep 2020 00:21:14 GMT  
		Size: 42.1 MB (42111430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f054c3bb715838c3b5b7a1b87d44bb27e66b730c6f46043718676fd2b5f82a9`  
		Last Modified: Thu, 10 Sep 2020 02:05:53 GMT  
		Size: 9.4 MB (9443974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7852e0ac40ce276d38d43909de6fc6e0283548a22510dba9ed39e9c093895f`  
		Last Modified: Thu, 10 Sep 2020 02:05:52 GMT  
		Size: 3.9 MB (3919884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee36d6b27968e04921e9febd754fab4304b42cd2a81762078e12818d8103e04`  
		Last Modified: Thu, 10 Sep 2020 02:06:17 GMT  
		Size: 46.4 MB (46413983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0bb90df142c46d00907c5a1fb377f9f185ac3bdb8887eb48352f92963efb7099
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105011714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2e1b8cc3fc3a70ec6ac0d962b3e5f31820f71416e8062a4123477c88faabfb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:23 GMT
ADD file:f74bb8d38ef70a022988428f254630d1f424ed9a3b957687b0cd0f85b9d49e29 in / 
# Wed, 09 Sep 2020 23:54:25 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:35:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 00:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b396f138ad78ffceac749b105c676dce568fa15a7b9f2273c2ee13ba023cea1`  
		Last Modified: Thu, 10 Sep 2020 00:01:33 GMT  
		Size: 43.2 MB (43171697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db606bd1ccd8d11ca18492ee5d5122fdae2e7172ceb0df9cd15dc4d9f3c259`  
		Last Modified: Thu, 10 Sep 2020 00:45:55 GMT  
		Size: 9.7 MB (9700841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd3b5402f1859618a8e455e6bf04a916c8460da1c5f115568ba530c96f6ba3`  
		Last Modified: Thu, 10 Sep 2020 00:45:52 GMT  
		Size: 4.1 MB (4095176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb81e51c7d923c71bc53fedd00e3247cbe38545e27848eb452110320aedf641`  
		Last Modified: Thu, 10 Sep 2020 00:46:19 GMT  
		Size: 48.0 MB (48044000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:61c16bd6711a16440da21b7f9bbd02e34df485da29c13bc9b6c5bbe76d68aa85
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113049931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a045e6a5f2aae34085bf92f74a90fed27482632948f94a62ca5771d587db0e1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:43:30 GMT
ADD file:615d959fea19ddc0e0fd27a59a77c1da8526b37da0b65bae0bfc4aac68c83ad4 in / 
# Wed, 09 Sep 2020 23:43:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:06:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 02:06:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 02:07:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5147f8567709ad49d5f034aa307bd29bdbbe40bcf438c67f4bc82655742c25c1`  
		Last Modified: Wed, 09 Sep 2020 23:48:59 GMT  
		Size: 46.1 MB (46086780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e04927bb8c87279f902150b7ad02632a0e41d18229b6d829e6c31e632936df9`  
		Last Modified: Thu, 10 Sep 2020 02:17:37 GMT  
		Size: 10.8 MB (10774112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ac4e21d5e22018e549d10694e362444abccd9e2bd098cc054587004c06e121`  
		Last Modified: Thu, 10 Sep 2020 02:17:35 GMT  
		Size: 4.6 MB (4563120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b554aa7ce070cfbb92dc0ba57007ca8eb8116627742ec4900e7b8ca629145f4`  
		Last Modified: Thu, 10 Sep 2020 02:18:00 GMT  
		Size: 51.6 MB (51625919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

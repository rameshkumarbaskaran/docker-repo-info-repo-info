## `buildpack-deps:bionic-scm`

```console
$ docker pull buildpack-deps@sha256:eb5c10a52fed7930ae1222436f4562d475c067d45900e33942789bacb2a47bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c7f3ec603f229956563670c8cf1bfca3911d20ef161a9203f4191cfddc4d07a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81855838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa23fc1a469e5b95ae71d84bfc5ad806da6f63676aa998fad3e500129dfbb76`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:43:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:43:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:44:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274f5248d99647b05dde09b6d5637c6ea924dae8e7ed3b5a328a6a3f28b86b82`  
		Last Modified: Thu, 03 Mar 2022 21:04:21 GMT  
		Size: 6.6 MB (6641663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c1aff063b29fefbcc720e348e1e2a9f6d10b63af15c57efde9bea08a52c759`  
		Last Modified: Thu, 03 Mar 2022 21:04:20 GMT  
		Size: 3.0 MB (3022228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b50c58fc472ca4d346b2f5a53aa790df6766881a4bd6ccd05c8bea90ec382b`  
		Last Modified: Thu, 03 Mar 2022 21:04:38 GMT  
		Size: 45.5 MB (45483621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7d5940e1432cdf7ddd439031fc7d67cbae945f1099297c3722329479e33700c5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71281384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8137e5710dcd959656d9dba1da1a22d654dee5f3bc7dfe3568956400f1ac75b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:24:47 GMT
ADD file:f5678be7a8216c2848b16665194b944ad8bdf7696d2925a432437feb730cf587 in / 
# Wed, 02 Feb 2022 02:24:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:52:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 03:54:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ddd1f986797e6622f6e3810028291b19248347b52709a52a74e6dea7ccee961`  
		Last Modified: Wed, 02 Feb 2022 02:29:12 GMT  
		Size: 22.3 MB (22306998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da1b8bb83e9f084a4b63a32178c403213a14c0e1087853ca2b524d7f4f948eb`  
		Last Modified: Wed, 02 Feb 2022 04:41:23 GMT  
		Size: 5.7 MB (5712132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9d2b667f1e938366a3c39c8de13e8ffe1c11351051d4e27affa22d801f593b`  
		Last Modified: Wed, 02 Feb 2022 04:41:20 GMT  
		Size: 2.6 MB (2584548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1c97954aecd75d04deee982c28e4519c8c8e3bfcd2b2852707224d19068530`  
		Last Modified: Wed, 02 Feb 2022 04:42:03 GMT  
		Size: 40.7 MB (40677706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2a852c6c745a43cd4e1d65663e92edf8d6550d3014766dbde5a1d842259a176a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75661920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695cd948e9e0e904561837612c552d4ff0d957f3fc2970af2567117b5eafb396`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:06:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:06:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:07:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b00c8ed3e482790555b6ba75dc2fe88a431898579874f982bd42af6e94adaca`  
		Last Modified: Thu, 03 Mar 2022 20:16:15 GMT  
		Size: 6.1 MB (6082527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355a1859624fa4241536a77dd88b7f379d0cfcecb8c9d1647065d1fce7976682`  
		Last Modified: Thu, 03 Mar 2022 20:16:14 GMT  
		Size: 2.6 MB (2570125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3bc0765bf07acd739d63b3109b54f69ce5a1785763501059461889ceea1a45`  
		Last Modified: Thu, 03 Mar 2022 20:16:32 GMT  
		Size: 43.3 MB (43279617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:30783dd795ca37eb07be88dae29a448dd72564418f5844d448a46e7236daf704
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84411983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0a49c902ec3d2523618324a91faecf5afc38f4c0a1e1f735b695ac71855b1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:18:47 GMT
ADD file:2ae34e7bffe3a59f3167a286025a093609188772be7b14601867a334bb3c0166 in / 
# Thu, 03 Mar 2022 20:18:48 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:37:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:37:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:250799bdfa37968bdaf47cc4d86f759e4e574d5e795f888e42c66ec0b7e92034`  
		Last Modified: Thu, 03 Mar 2022 20:19:35 GMT  
		Size: 27.2 MB (27161874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac28247ef04d1b842fabfcf6c1d41142412aa75bc7a718d9ee2f0a5294e7fb5`  
		Last Modified: Thu, 03 Mar 2022 20:43:48 GMT  
		Size: 6.9 MB (6930049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4db160b7628ac1a70c90af6b530d3f743602f72afb95d72926eb8e64f2348b`  
		Last Modified: Thu, 03 Mar 2022 20:43:47 GMT  
		Size: 3.3 MB (3252130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cbf4098c0549d70474da4743f711339b52599ece179881e218aeb9abfa3d01`  
		Last Modified: Thu, 03 Mar 2022 20:44:11 GMT  
		Size: 47.1 MB (47067930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e308d26fb1bc07c976d7943846eb8f057bc461434ae01aad7e2daf90a2013b9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94937629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09051eb25da7ef387f8118100aa16042ab9297432be76d53edca971118940989`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:27:52 GMT
ADD file:1070cef5a9454e0fdf7349b67652cf1ee9f02fb2679b05c10cfd1d7e2c378145 in / 
# Thu, 03 Mar 2022 20:27:59 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:11:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 21:13:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b055ba315c818484fa9979213cb00d276e7ec194a6928dd1270f73cf2aaa73b2`  
		Last Modified: Thu, 03 Mar 2022 20:31:51 GMT  
		Size: 30.4 MB (30437967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0253aa808a4a4801d83aa1d00c4ad4634c1f77aad211d65ef2ae9e34abdf1194`  
		Last Modified: Thu, 03 Mar 2022 21:56:52 GMT  
		Size: 7.1 MB (7056561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d945feb70f5ae95204f28dcb65ae6b9b5784e8fd4ad76bcbddaa6807a2347f9b`  
		Last Modified: Thu, 03 Mar 2022 21:56:45 GMT  
		Size: 3.7 MB (3719275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c0d1b13d6f5f94f46b37dca9eaef53960854bf39f26a3d8eaad6aff832e503`  
		Last Modified: Thu, 03 Mar 2022 21:58:18 GMT  
		Size: 53.7 MB (53723826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bcb9fdcfcec1d000234af71590791d9af44f13f5b3db426914b3a50f25264511
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79687185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13efae0562950939eaac87d2a9b74fe28f3d1118e2dcaa0c8719302b397c0a22`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:41 GMT
ADD file:84b8165a5044433cc2f9fdf9670d391f085aad3799d5e6dae035f8338dbe6081 in / 
# Thu, 03 Mar 2022 19:41:44 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:33:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:33:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:33:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:084e045c78b3a9e38ef6caaf47c3ef1c3d672d3cc2e60543ae9629511a5e1c8b`  
		Last Modified: Thu, 03 Mar 2022 19:43:09 GMT  
		Size: 25.4 MB (25365258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f451b0973e7815327265ae400866c266a9df0155f7711ddc54f80cda51301f0`  
		Last Modified: Thu, 03 Mar 2022 20:42:23 GMT  
		Size: 6.3 MB (6332491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae3cd2e93934ab0fa445573a52ddb393438bacf99a6402e72555da0ec0b4a31`  
		Last Modified: Thu, 03 Mar 2022 20:42:22 GMT  
		Size: 3.0 MB (2974972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60792c2aad4f31dd07cf0869cbe9a56153e7fa49039825aee8074f6d4afebbd7`  
		Last Modified: Thu, 03 Mar 2022 20:42:36 GMT  
		Size: 45.0 MB (45014464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

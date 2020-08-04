## `buildpack-deps:jessie-scm`

```console
$ docker pull buildpack-deps@sha256:df3dd6fee326c065186edca50b08629837226bb3c05537d0e81806c251d94e89
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
$ docker pull buildpack-deps@sha256:dc6e4ea0322331efa6c1378d8b2183b3c978e5a0237fb117e8f2ed3f6c1616b3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106808152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1749970c4c9b178ba7834e3ae81bb396b99426465aff78bff44293737f83759`
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
# Tue, 04 Aug 2020 08:02:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:89ff21f785d375d1e97b8335d239d9cfbfffe0b0706afae0679ffd7f6c202157`  
		Last Modified: Tue, 04 Aug 2020 08:28:04 GMT  
		Size: 39.8 MB (39778943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2d057f5e909c9c72f6e4738b18cb6b3190229045d2a9a8e140656f5499f1a820
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118456014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff8680d043d4076e1d5e86f3506aedabac33f30e9d8cfa4727f5e9c9e84c32a`
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
# Tue, 04 Aug 2020 08:14:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:b2d975d21db51982cf56382647589c692e4b2d94ca28355895c5bd8514ad38b0`  
		Last Modified: Tue, 04 Aug 2020 08:28:07 GMT  
		Size: 44.0 MB (43990467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

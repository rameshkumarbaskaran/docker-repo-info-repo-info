## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:6f46a689dd68655e0b707f1ec16a07d59be2327a40a9024674e6d8951ea00f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e05ba1ac80973daf6aff9e5262bcf8dea5634f4652ec02b1ed5dbb59b15925af
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126658866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f8a1c645ee05e3d3c6dbe9f293482c5ad5909dfab79a13093f8ec16ddedb4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:34:16 GMT
ADD file:f1c9279b9eb3b88b40c4958324519afa81185c0383ed51d5138ebf2a0eff6d7e in / 
# Tue, 12 Jan 2021 00:34:17 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:59:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 03:59:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:abc50f4e181143f18afce1a5282914e00abd896a798d96f7514e728b30f0988d`  
		Last Modified: Tue, 12 Jan 2021 00:41:42 GMT  
		Size: 56.8 MB (56800959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e331862b1a60a0f0273b0162c4d7c2b7bbe7a7b631e4a7847799daa4d3d614ac`  
		Last Modified: Tue, 12 Jan 2021 04:07:28 GMT  
		Size: 5.2 MB (5151057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d621cee81c84693094bc652651e3d6789dd350ca0bd2dab361e7677761ef3a02`  
		Last Modified: Tue, 12 Jan 2021 04:07:29 GMT  
		Size: 10.7 MB (10650196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8528b6c5869ceae094dbd96627195e8a672bf6f4e72992200cfc64bf6de1584`  
		Last Modified: Tue, 12 Jan 2021 04:07:48 GMT  
		Size: 54.1 MB (54056654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:61bdc21b732e0e309470c94104a80346985f4a74f8599a54ee2dab386dbbd8af
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120509885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba09e064a0d59103ba8ac7fd7fad438ca175b501cb646ef1bc7aa7c968c03ef1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:53:02 GMT
ADD file:8a666bde5248b085708640c42b93c850be2265e6a4db5b59c48543ddc8ad0148 in / 
# Tue, 09 Feb 2021 02:53:03 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:29:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 03:30:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 03:30:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b915a09886212577bb3e4444d6bdc576b17746fa48c0239c56c968d81127e7e`  
		Last Modified: Tue, 09 Feb 2021 03:01:34 GMT  
		Size: 52.3 MB (52324134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c594f7d69077392315310232b92354eaa9652361ef5e54825e4aade3a67e2851`  
		Last Modified: Tue, 09 Feb 2021 03:41:51 GMT  
		Size: 5.1 MB (5053985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195684c55108e3d23d6b03082fa8140c8859a738918fed4410211cbac9dd2ee6`  
		Last Modified: Tue, 09 Feb 2021 03:41:52 GMT  
		Size: 11.2 MB (11214925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4c9349b2c21a4df7a32b0def6cda8f6f44a4972a38016b41392e9a816ae16f`  
		Last Modified: Tue, 09 Feb 2021 03:42:16 GMT  
		Size: 51.9 MB (51916841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:269e462e07e2550a6d485e28c3c569fa5da043174aec85e41f870e5fa7425b2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116573873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb24e45497c42ad3b506c7a19b92a44782654e74d073cdb09dca362b42fb1c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:03:45 GMT
ADD file:a459be4601ccf608a415f6ce53ea885edd1a9a10ba1205f3e8493e277e6a7faf in / 
# Tue, 12 Jan 2021 00:03:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:18:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:18:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2fdfe7e087b5c823888d02320fcca90d4debb7a7d0ead6a978abb2de6acbbc00`  
		Last Modified: Tue, 12 Jan 2021 00:13:47 GMT  
		Size: 51.9 MB (51902171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0592e7529a748d8d0e52ef640addc32dcea717609f5c656e4399e87bdd4d9db`  
		Last Modified: Tue, 12 Jan 2021 01:31:29 GMT  
		Size: 4.9 MB (4921500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeb968aa1e6a404fcd0a89cbc65878f592c4c4067725853712ca4d00c1669ce`  
		Last Modified: Tue, 12 Jan 2021 01:31:31 GMT  
		Size: 10.0 MB (9976214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdb7dfd157d86a4ab3edd03ec9cf4d063137a8f583451d79dea1963f4ac7213`  
		Last Modified: Tue, 12 Jan 2021 01:31:56 GMT  
		Size: 49.8 MB (49773988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:47f792147745c3a04e3075b90b8e336e8ed66aeb3ab30058cd22e9c917f3ea69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125496053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3f1ec20341d60a664a366e1dcfb03a7c2de631dcea6de70e2124f7fc531ced`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:42:27 GMT
ADD file:ba9ce45e2c6743713798982615c806de6db6d8fd9a0d8734c8a69d80f3959eb6 in / 
# Tue, 12 Jan 2021 00:42:35 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:27:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:27:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:28:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:01dba80e9024f3ac734ae74a14f2997ea67918b4de57aef778ed839a508baab1`  
		Last Modified: Tue, 12 Jan 2021 00:53:15 GMT  
		Size: 55.5 MB (55537816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8417d785c975de855b94a5c17e92b69107a02149bbd61ac1b6d1355d80b32549`  
		Last Modified: Tue, 12 Jan 2021 01:40:11 GMT  
		Size: 5.1 MB (5140360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34511ce04354db34bda0eb613bcb4990a4e262fe16307861b007423a0033c44`  
		Last Modified: Tue, 12 Jan 2021 01:40:13 GMT  
		Size: 10.7 MB (10655802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23256b8138d02e2f8552e7878b3d34195476c50b86ef0dcf9d758fb0bade2fc`  
		Last Modified: Tue, 12 Jan 2021 01:40:39 GMT  
		Size: 54.2 MB (54162075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e665658d1e9d85acf9e5e3a355195f93425a17d389e6401d59c0930cc1b3a439
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128506616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c4d284a18a12e27fec48bb3d12c68e5325e0019dd47cc38acab8f2a1018145`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:17 GMT
ADD file:d3470c47b61c2df201e9fe51e9dd198c152bae2eba84df9bbfcb591bfb29502a in / 
# Tue, 09 Feb 2021 02:41:18 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 03:12:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 03:13:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:14213d5e86eb4e1e7c43e3524429378786d8674960445945ce050c587b83884f`  
		Last Modified: Tue, 09 Feb 2021 02:48:13 GMT  
		Size: 55.8 MB (55792012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2cbabcd8ca39fd619ad8a109f0fe5eea442c6afefd108f3d2a80a49be04524`  
		Last Modified: Tue, 09 Feb 2021 03:22:39 GMT  
		Size: 5.3 MB (5271392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cacdc0d9d1ac9a69c2a336a43253fbfd3737321bf5e32c6f9ee54465cb2087`  
		Last Modified: Tue, 09 Feb 2021 03:22:40 GMT  
		Size: 11.9 MB (11932342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f68738ae071787fe3613a10b142f8364d3bb9250f4e045082d605a217ca3a1`  
		Last Modified: Tue, 09 Feb 2021 03:23:12 GMT  
		Size: 55.5 MB (55510870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:58f7c36a6f3774dd3233336975741f3f58b69b7ef5dac5a10af488711ef95027
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123578418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5080581b208811c075eea5ce0f7991f7fb4b576f6463ef9a1ba8394961848244`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 01:16:48 GMT
ADD file:7bfb9d47fcd2b6a553e5be3b702d34f192cd8798dd3982fc6e6e77479f0affdc in / 
# Tue, 12 Jan 2021 01:16:49 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:54:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:54:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:55:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24a4375dbae3deddd016bd6d4372d219ba5fe4102ce643c06dd57677bc882654`  
		Last Modified: Tue, 12 Jan 2021 01:24:08 GMT  
		Size: 55.0 MB (55046139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1447ce8a926cf7692ae55e3f2edb9925e5b11be684c7fd68fe2a385a5b812880`  
		Last Modified: Tue, 12 Jan 2021 02:05:46 GMT  
		Size: 5.1 MB (5114938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfd08658a76a7d3cedb6b4760f760c0ce830104bb77dbffd92228d4d0448730`  
		Last Modified: Tue, 12 Jan 2021 02:05:49 GMT  
		Size: 10.7 MB (10658281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e7a05de00a7a60c4b7f630af924f98065319eb7883ece0b8839a36675802f`  
		Last Modified: Tue, 12 Jan 2021 02:06:42 GMT  
		Size: 52.8 MB (52759060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:da7d02d54f25245b44530156a1c8dde78590aa4570d25cf76250229401eb11be
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136205465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3bf782687e1b88166a4992fdbdc58a14a653553a4459da68ab97f1a17e4e02`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:40 GMT
ADD file:f289d6dea557bc0563fd9221c4857a56c56bb52d981a3ec90ade2f1b76980794 in / 
# Tue, 12 Jan 2021 00:25:56 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:21:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:22:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 02:25:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:594e638823d3ce0bbedac4d1aebea00f91d28a98d7b98ca680fd90e4c0fc8850`  
		Last Modified: Tue, 12 Jan 2021 00:34:46 GMT  
		Size: 61.0 MB (61048727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a59148553af7496dfbc29a5704e94338ac15ab898a646dcbab32076a5f00f3`  
		Last Modified: Tue, 12 Jan 2021 02:40:41 GMT  
		Size: 5.4 MB (5400394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45a065f7b5587bec16714bce093a4075fb92b291238fee1bae7d383a16a4052`  
		Last Modified: Tue, 12 Jan 2021 02:40:42 GMT  
		Size: 11.4 MB (11422811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d08d3752bb8f3109a9dc34906d86a1d6f92b178e9b8153717c78ad56a98e568`  
		Last Modified: Tue, 12 Jan 2021 02:41:08 GMT  
		Size: 58.3 MB (58333533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bae397ffc65009cbdd5888b97aae389d32213a3317b64ff976a0c04f405dcde7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123247810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1e67a02e0a6800c8df7adf9c338b62bfa9e84c2f7c6e0d0afe4a759fd5050f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:21 GMT
ADD file:6b632451421e7f0411db1927a48466a6b3bc2f7e10a53b00a06799fbec279bdd in / 
# Tue, 09 Feb 2021 02:42:24 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 03:07:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Feb 2021 03:07:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3dd2606d37926391a1e8153ffefee2aaccae04bd432c37c97187880ba3ed01ea`  
		Last Modified: Tue, 09 Feb 2021 02:45:45 GMT  
		Size: 53.1 MB (53060083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd34d7430306d4b5f56a7983d33fdce7c2f86209989ddeacc68e07134aef96e`  
		Last Modified: Tue, 09 Feb 2021 03:12:40 GMT  
		Size: 5.1 MB (5127742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b9a7cd753b983b2730894814680d1c0b77e08d7affc85900856bd036f96806`  
		Last Modified: Tue, 09 Feb 2021 03:12:41 GMT  
		Size: 11.4 MB (11412927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dceafff3a3e377a78f87f033989c6a1e6a8359c5afc3075ebb1d31d46a46a2cb`  
		Last Modified: Tue, 09 Feb 2021 03:12:56 GMT  
		Size: 53.6 MB (53647058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

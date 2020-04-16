## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:81497b4be433ec59e0a11e493cdee52f133aa97f6a905a6cbd41fb8f9860b3e3
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

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5a48918bde4021b392272c123fb0e4bc39f090c20d84e358d76228f8d09abc65
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125526141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae43e074170794f11b549e1a8267958bf458e159b9b1f8cba156e852724b910`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:21:21 GMT
ADD file:d8f8a66e04b091b1ee6d1d330b5cd80472768f8cef96db861ba4dfaa2472fe20 in / 
# Thu, 16 Apr 2020 03:21:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:57:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:58:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 03:58:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d9ec154a243cb2fcf510aa97241fa4d7c075add5b018b19db3f1dca9f93c83a`  
		Last Modified: Thu, 16 Apr 2020 03:30:54 GMT  
		Size: 52.0 MB (51968339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f52bafd3e8510b30e30d2ccb5e044a4647586a4b5dcdee4e79b63b54296a77`  
		Last Modified: Thu, 16 Apr 2020 04:14:57 GMT  
		Size: 7.9 MB (7932617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61caa2b6b1a3f079feb31d0b6ce33740955163e262ec2f624070129b13ebc779`  
		Last Modified: Thu, 16 Apr 2020 04:14:58 GMT  
		Size: 10.3 MB (10298054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c043d752dd56512f49ba5efa050e0701eadb2605cd22b197ccffd7aef9ba742`  
		Last Modified: Thu, 16 Apr 2020 04:15:13 GMT  
		Size: 55.3 MB (55327131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d7c7aa1396c2fbd2dff89fd465a37156a8352261b179520c687e2c5a9ba9cea6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120336738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250eae667e8ea1e30eb07b7c431e2be943ca786117053c2abbf9af414110af1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:48:51 GMT
ADD file:34972a3f69849271a3928351165da58547b7e747a95139712188aa70c0b57364 in / 
# Thu, 16 Apr 2020 00:48:53 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 07:35:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 07:35:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 07:36:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:562c28f550656170c3977f83af3b203cf461b48e55905e20714735c0da33f6af`  
		Last Modified: Thu, 16 Apr 2020 00:57:24 GMT  
		Size: 49.9 MB (49911580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6e10c95bf2fb0d9afd80c213468dbbf9c1ad4730788858911322bf24add94a`  
		Last Modified: Thu, 16 Apr 2020 08:03:59 GMT  
		Size: 7.5 MB (7514410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e617dda0a7a661e7f311626e566d0268d79bc1e83eb5b8e533776c9cd3991592`  
		Last Modified: Thu, 16 Apr 2020 08:04:05 GMT  
		Size: 10.0 MB (10008531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85850fe957d69f2c749872a598fb5b37adbebb598130616ccab029087a446243`  
		Last Modified: Thu, 16 Apr 2020 08:04:30 GMT  
		Size: 52.9 MB (52902217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f65d24344ce190aa133cb193ddf3fdb9d8066164a2730f0cf39d6d1aaed45b30
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115241301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d730fa5f7672233b69aacd01556accaa1e2a9aa1b4c082cb913e5a32f2af9e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:58:05 GMT
ADD file:353f89e64e5475f2d99be1c5e0eaa80d5aeb89e02c274ba507df4def8f7ccc8a in / 
# Thu, 16 Apr 2020 00:58:14 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:33:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:33:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 01:34:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a287a7fa81e293e147ba52c36ae34e643e975ef88ebe9a6f226a048dbb7ee9fa`  
		Last Modified: Thu, 16 Apr 2020 01:08:03 GMT  
		Size: 47.6 MB (47646389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47358f6975165f42a9cd9b867f0d03e95a00b52627d5e833781a9eb45eca84cc`  
		Last Modified: Thu, 16 Apr 2020 01:54:57 GMT  
		Size: 7.3 MB (7255347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376a0294fac4492ac4a3da9b92cdf02ee87e6bfd519ee19fb996c5db96da33ae`  
		Last Modified: Thu, 16 Apr 2020 01:54:57 GMT  
		Size: 9.7 MB (9672922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010ce0dbcbdea4c6cbef9d1bda1fb769c382107cb837edfcdc6258b8421fc200`  
		Last Modified: Thu, 16 Apr 2020 01:55:21 GMT  
		Size: 50.7 MB (50666643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f0a2855c50addd8e9077c8c020a64f736c1d7d7a946f333abb626666fc91e55d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124388724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5e5a4139d93d5d8851e533acbc5b183d1c638415ace769dce08bddd67075c6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:40:12 GMT
ADD file:27c25cdd69090f4b15f9f2f4a147879d1d7510b7b2f8c231a92fc74832325413 in / 
# Thu, 16 Apr 2020 02:40:14 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:09:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:09:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 03:10:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6c6bfde49c5261423574a9f9bc077a0cd0057775509f9d9e061556a16b84e1d7`  
		Last Modified: Thu, 16 Apr 2020 02:48:01 GMT  
		Size: 50.9 MB (50901465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c744c6854f291e264392cb87f79c4675b05d5383ca93df9f5b4be8f447aba3a7`  
		Last Modified: Thu, 16 Apr 2020 03:26:27 GMT  
		Size: 7.8 MB (7807688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0a53c53b80bd91c029938e07ae8fb49e75ae1d45620212fa6fc041e97f5750`  
		Last Modified: Thu, 16 Apr 2020 03:26:27 GMT  
		Size: 10.3 MB (10294224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee1bd7b8a02f00bba05f898a3f2c91d213d6fff20796effafce1437c9b6cab9`  
		Last Modified: Thu, 16 Apr 2020 03:26:51 GMT  
		Size: 55.4 MB (55385347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:35bbf824f62bf3c22b4487fed0981e21f80b413f87a2b58bd6f23305b26283ce
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129038284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98814398813cedf5dfb13faec18e7f8b874c3b31c18fbb19715aa7e8464565a8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:38:50 GMT
ADD file:1d78edb74644d640409b64831c000f00654603e8888b50c46ac37ca0c186c3e9 in / 
# Thu, 16 Apr 2020 01:38:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:16:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:17:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 02:17:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d162d6311c3b7618a8b9a80392bb71455272c7ef63938e132282070923f16ead`  
		Last Modified: Thu, 16 Apr 2020 01:45:26 GMT  
		Size: 53.1 MB (53116500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d42814ec88fe50214d62dfdaf2c1a27abf7c61f1718b16dc664b952cc85492`  
		Last Modified: Thu, 16 Apr 2020 02:35:50 GMT  
		Size: 8.1 MB (8110131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97139d647978bbac84cf0fbb6575ccf2950e262ccf617d10aa0e60e479481bb`  
		Last Modified: Thu, 16 Apr 2020 02:35:51 GMT  
		Size: 10.7 MB (10657214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29d09c18686eb52024c1b28dd62d1ffe2ca03f040d1f82bf9fcfa657d41bb5d`  
		Last Modified: Thu, 16 Apr 2020 02:36:12 GMT  
		Size: 57.2 MB (57154439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:69a2ddfe22bdf5eef565d5ec8640c4849b7ffe8ecf38d08eb7dc89523033d4f2
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122727464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1953c7f9f043d95086fe2ab1c50f6a597e611cf8f153983b5c556ae297eb32e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:29:03 GMT
ADD file:571d620a73f63f0bce6937ced0e2a2f7dbd127e0fecf9e97790d0941cc6bce5b in / 
# Thu, 16 Apr 2020 03:29:05 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:06:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 04:06:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 04:08:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:02267d0e0eb88e51f19069b5cba14fd409e92034ffa2d476e3692b85e83addca`  
		Last Modified: Thu, 16 Apr 2020 03:54:44 GMT  
		Size: 50.7 MB (50678841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb4f080ce8cb9f9c9b928bdf65ce27246d82edfff61aa1f7897eacde7012a6b`  
		Last Modified: Thu, 16 Apr 2020 04:31:14 GMT  
		Size: 7.5 MB (7459912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82100df7296466c11c6b4ac15634db8168d4618b3226c40897edace4a237a2a0`  
		Last Modified: Thu, 16 Apr 2020 04:31:16 GMT  
		Size: 10.3 MB (10324443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a595cb267827df6d653c7f6bb665d87184787ea82d990902cf4edb2b88804d`  
		Last Modified: Thu, 16 Apr 2020 04:32:43 GMT  
		Size: 54.3 MB (54264268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9d710af780f3b50fc92968ff0d9a998d9070b92172c5d8a723ac996abb9d4ffb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135801949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4662fd62fe897e2d09dea699fe709ee8ad6e113e3d519fb5268b3128992f18`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:32:12 GMT
ADD file:2efc2c0f69b08c32feb2685a63906c73b19fb52d2b93f97e10252433820bc5da in / 
# Thu, 16 Apr 2020 01:32:20 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 05:28:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 05:29:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 05:31:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5bebe00a0631d47861daeee3fc26571ca333821c566ce1b711e981ca7685ea53`  
		Last Modified: Thu, 16 Apr 2020 01:50:59 GMT  
		Size: 55.8 MB (55848114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82799cc8d738aec7df8ddf9bb9deae49b2ebb048ae3ff658fab69e938e9eed79`  
		Last Modified: Thu, 16 Apr 2020 06:16:14 GMT  
		Size: 8.4 MB (8355958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b8d71962ead5ce3976d8ea0a1c6a27893344557398f8d2b314c28d2b065fd7`  
		Last Modified: Thu, 16 Apr 2020 06:16:16 GMT  
		Size: 11.0 MB (10975758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51294330fdb8f00471b393961669925b313ea4466f89528adcdb5a6fe85b497`  
		Last Modified: Thu, 16 Apr 2020 06:17:41 GMT  
		Size: 60.6 MB (60622119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:67462a97f31b95591f64b4e54a3ddb9ed3c559ca74af1fced7123183896ded9c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122918838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e0789c7cb01e0395c24ec28746371549f142f2b653fb112ebf1cb1a731d4e1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:41:36 GMT
ADD file:91904e1cbd0660c7c48420aa34dd58c0e8619c69afe6c1412a495c364773b5bb in / 
# Thu, 16 Apr 2020 00:41:39 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:56:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:56:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 01:56:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:929a8c37dff5f4096f453d7847637ff8b3e3fa702bd1043408eb37af338237d4`  
		Last Modified: Thu, 16 Apr 2020 00:45:37 GMT  
		Size: 50.6 MB (50569040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625f45e55816a01b4e47db24dfb9857e953051816a723f6999906fa8fe1cb40e`  
		Last Modified: Thu, 16 Apr 2020 02:05:36 GMT  
		Size: 7.6 MB (7600032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af726635ebace664ecb1c229bba4cbd77183a3411aacacaae74f1cbb0882eadb`  
		Last Modified: Thu, 16 Apr 2020 02:05:36 GMT  
		Size: 10.2 MB (10183890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216e30525b6ed08c23f0a9ee26e1498e8ad2fa322601120a5936a44f2ddbfa87`  
		Last Modified: Thu, 16 Apr 2020 02:05:50 GMT  
		Size: 54.6 MB (54565876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

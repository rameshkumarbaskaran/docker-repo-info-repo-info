## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:27786d22033911c7da59c2e14aecb8716f13019b1c3714314ece08b4d7e714eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:52a7124440aeb68cd12e2cf204d86fbfecb0da0f4c7e3cea170ba3e02918fa82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77151035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d42f20418a32e6749f9981f745dacdc558edd5fe6925bc07a06a6dd7a6989a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:25 GMT
ADD file:11157b07dde10107f3f6f2b892c869ea83868475d5825167b5f466a7e410eb05 in / 
# Mon, 06 Jun 2022 22:21:26 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 02:16:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:16:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 07 Jun 2022 02:17:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:405f018f9d1d0f351c196b841a7c7f226fb8ea448acd6339a9ed8741600275a2`  
		Last Modified: Wed, 01 Jun 2022 03:03:39 GMT  
		Size: 30.4 MB (30423715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bca3245ce06c5f92cf1528db00b152cdde37af4bf05c5d3976141dc4a704c5`  
		Last Modified: Tue, 07 Jun 2022 02:27:12 GMT  
		Size: 3.8 MB (3819557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7cdee01903ed192b91b97760507cc18ed88be4ff61e33e87bfe6f1944605c9`  
		Last Modified: Tue, 07 Jun 2022 02:27:11 GMT  
		Size: 3.6 MB (3559751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e140559ac12daaa563a0869b223a27cca33ef57ed3eac04f09c6c1f88d1da866`  
		Last Modified: Tue, 07 Jun 2022 02:27:28 GMT  
		Size: 39.3 MB (39348012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c073bc7d6d5dc90d0f5efb152d103147c1b524d76fb4e5183af60d9dd0e7526e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76398354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fbd82b9f0ac09aaf49e47847d8d6817739cf69be8fd92832e2de3bb2e3d485`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:51:35 GMT
ADD file:26c86cfcbc153addbca421974e648a7af07234cb3f741bfb030aa0db90b6a7c6 in / 
# Tue, 07 Jun 2022 05:51:36 GMT
CMD ["bash"]
# Thu, 28 Jul 2022 13:40:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 13:40:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 28 Jul 2022 13:40:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5aeb313108e16ff98084efb2ae2830cbe915ea38b3e2fd1e32688dd9d8c11320`  
		Last Modified: Tue, 07 Jun 2022 05:56:03 GMT  
		Size: 27.0 MB (27017432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ae1200b85869148ec2ccc96108e9afadd9b35842db2ffc6c68e698f7b28939`  
		Last Modified: Thu, 28 Jul 2022 14:02:21 GMT  
		Size: 3.6 MB (3571388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0830edfa34eddc4f218d51b9dbcb0a3a05e93b8e2cfc40d4e6595fa4e51b2ae8`  
		Last Modified: Thu, 28 Jul 2022 14:02:20 GMT  
		Size: 3.9 MB (3903482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5ddf9431301c2e11f60aa38393f9a80ad5905a96ec49a163f1202bdaf6798c`  
		Last Modified: Thu, 28 Jul 2022 14:02:48 GMT  
		Size: 41.9 MB (41906052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2ae5301f83a59b52f0b0d2683973fe4e31f3426bb606d7a355884db489fe215f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74737992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d3e646f7716849231d58af81d9056582a811d0ced77fb75a59ccf288b4ea7d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:35:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:35:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:36:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6de042cb869a25eebdf68de514b4450f82c38b9cec853a790e0bc12272588d`  
		Last Modified: Tue, 02 Aug 2022 01:50:49 GMT  
		Size: 3.8 MB (3793545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efd2a11a62cb05975c115b200176aa1783cf879e07bb4ee462cf161275ec087`  
		Last Modified: Tue, 02 Aug 2022 01:50:49 GMT  
		Size: 3.3 MB (3320844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803994e685daf2d39be7fccc240aafb13aec0f79465eb21e6a2ce4e349763d8b`  
		Last Modified: Tue, 02 Aug 2022 01:51:07 GMT  
		Size: 39.2 MB (39242448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d1d4db991dcbf8892dfc4c29db3dafc62fa36e2de54407e47c3b6ad0a83ac058
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88192936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6a9e574eaa55f964034d5f75b19c8b950012f2811cf5596ac824dbacf79245`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:46:49 GMT
ADD file:62ec907c651e833838867bd541cf824f5f609ea4e2b19c4b26cec74a57b60470 in / 
# Tue, 07 Jun 2022 05:46:54 GMT
CMD ["bash"]
# Tue, 26 Jul 2022 23:14:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Jul 2022 23:15:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 26 Jul 2022 23:16:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b851cfa9fcbcb74629241502e21ebbae255fe40a2f26949573f278672b65c308`  
		Last Modified: Tue, 07 Jun 2022 05:49:53 GMT  
		Size: 35.7 MB (35717509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46343fc34cefc64643ad2978b456c5594781763e18fa40d5e422cf0e46e272a5`  
		Last Modified: Tue, 26 Jul 2022 23:57:02 GMT  
		Size: 4.3 MB (4289632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a263dc068c2c9cb95560c1132cef9e8f9817a9a18a04618da486f2aae098c9cf`  
		Last Modified: Tue, 26 Jul 2022 23:57:01 GMT  
		Size: 4.4 MB (4426126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2c89ab993e71903f35368596bba94dd9f5fc311f934a5a66c7931b074bdf1f`  
		Last Modified: Tue, 26 Jul 2022 23:57:25 GMT  
		Size: 43.8 MB (43759669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:eb73e93ae933bba13bc3d493271626cf5c510a2d2a2a25a02460581c0629fa47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77229577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db9acb80252960587fbab9540365e07b254af741cab169a74ecccce7d3602e9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 18:18:50 GMT
ADD file:d19287898059e2e99fffa362a449097aaffb132af21a1d1e72c5b898ff785df6 in / 
# Mon, 06 Jun 2022 18:18:51 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 19:31:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 06 Jun 2022 19:32:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 06 Jun 2022 19:36:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1edfbf9ed16b67ab57bd93f6b8aa57ec157383c958bd3e39e94cdac02ca1db32`  
		Last Modified: Mon, 06 Jun 2022 18:41:31 GMT  
		Size: 27.7 MB (27745919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0b2b247adbcda207142d115c60814f361a65d9e79b584f05cf2c7ae16de140`  
		Last Modified: Mon, 06 Jun 2022 20:28:14 GMT  
		Size: 3.6 MB (3614448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e32164a9b5dee9bb43c693f8c7c833ebe435e4b86660f7a14ce30decd26898`  
		Last Modified: Mon, 06 Jun 2022 20:28:12 GMT  
		Size: 3.8 MB (3776968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26beb173e0f45f69bbe4fe18a33e9aac6ddee5f7c6e5cf78b1a639f7dcc4b1f8`  
		Last Modified: Mon, 06 Jun 2022 20:30:26 GMT  
		Size: 42.1 MB (42092242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:38c941a0a7341b92e0cd0128473178a0d41ef7eb43f6b3205efcd3700ebfc5e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75233345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4073d5e81c9dc09facbd3c18e71d902ea51d6a5c75d4dfa569007fb1920ebdf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:24:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:24:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3f1b5666f8b3207bb75caab1dd328b04374a37a1d6568a5a870f2e893cd488`  
		Last Modified: Tue, 02 Aug 2022 01:39:39 GMT  
		Size: 3.8 MB (3823523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d904f2efab931c8317caa6af484cf95df9e6cc7e721574cc2a67fa999822e39a`  
		Last Modified: Tue, 02 Aug 2022 01:39:39 GMT  
		Size: 3.5 MB (3471689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce845895b5d4851821cc732df48f574c90565b82ede329134d3999f61cf073`  
		Last Modified: Tue, 02 Aug 2022 01:39:52 GMT  
		Size: 39.3 MB (39295348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

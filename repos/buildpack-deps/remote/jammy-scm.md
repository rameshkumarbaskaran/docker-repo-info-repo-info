## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:7bf5d5f2337bd5d57e375e221f744d8a9148d63e9c1671850092210b4f9a030b
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
$ docker pull buildpack-deps@sha256:dd6a1375f1f144120e73c33263d15fad407cdf3af5700bf06b98c42e712a0d2a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77143770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5fb79923d815372876a15ca9afa7294969ee8f6142ae8377dd987dd91de455`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:20 GMT
ADD file:6cd2e13356aa5339c1f2abd3c210a52f6ed74fae05cd61aa09f37b6a4764f65c in / 
# Tue, 04 Oct 2022 23:35:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:09:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:09:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 01:10:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf92e523b49ea3d1fae59f5f082437a5f96c244fda6697995920142ff31d59cf`  
		Last Modified: Tue, 04 Oct 2022 03:04:01 GMT  
		Size: 30.4 MB (30428928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19b9364a5e7fea40b9e9eb4614f0e4533857b602c7fba30362889933ef14298`  
		Last Modified: Wed, 05 Oct 2022 01:24:38 GMT  
		Size: 3.8 MB (3804673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856d49148d8882ac6866bcbcbaa08bacfe1f0d0d382b73675630ae29d44ae3f2`  
		Last Modified: Wed, 05 Oct 2022 01:24:38 GMT  
		Size: 3.6 MB (3561097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f83374f27f6992ee240fe68ce2e0c2d9db958dc2c9acf1864ef83040cc5387`  
		Last Modified: Wed, 05 Oct 2022 01:24:54 GMT  
		Size: 39.3 MB (39349072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8ee2ceb7f89309d35af0ffd83a4e9f99593da3ebc818ef9db16edea6807e5999
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76186876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac586f0d0ef3e15932beb867ebeae6c400aec079dbb4e9675345a7b3a0cfb07`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:57 GMT
ADD file:11e25fc4812528219464289700bb0495bf9298918899103c33d7ef9022690eb0 in / 
# Wed, 05 Oct 2022 00:13:57 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:44:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:45:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 00:45:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99b9c73338a7c0dbe41f9fc543fae706650a616453e1e330f870e20916c18a11`  
		Last Modified: Wed, 05 Oct 2022 00:16:02 GMT  
		Size: 27.0 MB (27018632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c337b77409c2e34b5e69df73a11e0ef62cd00b8b23e7d6776235d6491726ac80`  
		Last Modified: Wed, 05 Oct 2022 01:00:37 GMT  
		Size: 3.6 MB (3555370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a1dc485f1a7e2433bb9a4501dac3fb4727fb7708715e743277a50ba4933ca1`  
		Last Modified: Wed, 05 Oct 2022 01:00:37 GMT  
		Size: 3.7 MB (3712768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5595ebdf3f8239b659bdbfc55b5e0a70965f29a4e546cc5efdda43f8e3a4ef76`  
		Last Modified: Wed, 05 Oct 2022 01:01:00 GMT  
		Size: 41.9 MB (41900106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:754125ea4299c3778e6d095b40dc8e689a5cab6d965930f39c19d10cdf176fbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74719893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0530b319b8790bb31a1191861e5bc7d4a28a5b5125d18d134d79a64edee993d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:31:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:31:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 00:31:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e4680d7b30c1a6751735f5f2e99eea49e96adad47b7382c4944ced1c92764`  
		Last Modified: Wed, 05 Oct 2022 00:42:55 GMT  
		Size: 3.8 MB (3776737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd6f597bdec02a1a3fe9903e9fef999621ae074f289e4bf2e8fb5a209f38722`  
		Last Modified: Wed, 05 Oct 2022 00:42:55 GMT  
		Size: 3.3 MB (3320776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf571b6e690a8dc0a34f2d65d0d5239528c8cbc76e1325ac3b60e92182e0cc6`  
		Last Modified: Wed, 05 Oct 2022 00:43:12 GMT  
		Size: 39.2 MB (39240125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3994372206c22556838300c19312f37cdd84e93c99e55960bf20393d1d085d52
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (87985443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d893fac575fc17de4548f3b459f5fac5d9619b30626da9439dc3316cb4ad0c03`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 10:52:24 GMT
ADD file:5f3953a21754ce756642c9ddcf521f2cfe220a5fe988ccec51085bd074fbe46e in / 
# Wed, 05 Oct 2022 10:52:26 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 19:01:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 19:02:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 19:03:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5053ecffedc109608feacf4836ad15e0f7b2f6a411250a41574342de479c4760`  
		Last Modified: Wed, 05 Oct 2022 10:54:49 GMT  
		Size: 35.7 MB (35709341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc308bad1b10b03cd541c6dea0b11182a79aff23d70d5e2b6a548287677cee4d`  
		Last Modified: Wed, 05 Oct 2022 19:19:35 GMT  
		Size: 4.3 MB (4276449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7dd0a909d4ecaaa680719f71a1dc6ee1b8c9ad3005450b0014d644047946993`  
		Last Modified: Wed, 05 Oct 2022 19:19:36 GMT  
		Size: 4.2 MB (4234195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12882d6f215684cf2695c5956be754005a9f994b2414fabd51f026d46da7ebc7`  
		Last Modified: Wed, 05 Oct 2022 19:20:00 GMT  
		Size: 43.8 MB (43765458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0b59c501076932d75abe6baf6b45272617ca658c00bea23c4c642ecf0cef54ad
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77238223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c179e15b046f9a7a277678332c1ba0ff71c2985288dede5b120f176dbd7b378`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:14:15 GMT
ADD file:e1fa146cf8e97dd6a2f3ebb2dacba539556ef4a1e87dc53bd745a3cf0ba10aef in / 
# Wed, 05 Oct 2022 00:14:16 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:46:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:47:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 02:51:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbeff255552ba792be63b343113968df42de6f599d1372edd4c7346d08dfeace`  
		Last Modified: Wed, 05 Oct 2022 00:31:39 GMT  
		Size: 27.7 MB (27747416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6129e2d138d3d5141f87ef04090f82aeeb874b1d1e3c6f6e94d843cd2447826`  
		Last Modified: Wed, 05 Oct 2022 03:43:29 GMT  
		Size: 3.6 MB (3598134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a1ba2d60715be154c4f520ac4f1ef149f66b921651ab2726a809c14316e55a`  
		Last Modified: Wed, 05 Oct 2022 03:43:27 GMT  
		Size: 3.8 MB (3778196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91414a4a50607595a5e83cc27ee8f8e885ea1d1c43848a3df1487911ae62cc19`  
		Last Modified: Wed, 05 Oct 2022 03:45:48 GMT  
		Size: 42.1 MB (42114477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1261bcd972c83821318a0ffbee775f7c50792bde771fc73c806e78a7af67b584
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75206497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44680731da527ce74344c9ff0197ff653c79174a875a4711b0b82402a398c303`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:21 GMT
ADD file:d9af7670f58e9478e400dac85a0fcb07a4209846dbd1ea560fdc6de6e2cb5e4e in / 
# Tue, 25 Oct 2022 01:23:22 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:40:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 02:41:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9aed974aece14dd3aed00810d58a89e87eb5be9ad1c6fbb1ed077dc3f145dccc`  
		Last Modified: Tue, 25 Oct 2022 01:24:48 GMT  
		Size: 28.6 MB (28641668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0474dffae2d1e16bb420718a81adc05c65e7cf46cfec815544e0ed630334ee45`  
		Last Modified: Tue, 25 Oct 2022 02:52:51 GMT  
		Size: 3.8 MB (3809925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdff4ace6c098f616aa6e4ddee394e5472cdf30f97f3b22e0dc26d42d42e234`  
		Last Modified: Tue, 25 Oct 2022 02:52:50 GMT  
		Size: 3.5 MB (3472443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92140a87366357bdb10310a5cb8497d894c21c28e686a09af051436e071d5075`  
		Last Modified: Tue, 25 Oct 2022 02:53:04 GMT  
		Size: 39.3 MB (39282461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:83e988e7c0dec7baf911e2f60b443ecaa0e7a537bd5a4b017a33180eec974731
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8b663c336c6f27ee8028294339f22471745a996fcf20061316c06f47935f0a8d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130142597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a98bf89580a9a6c1ed6ecfc55a3c351a4469fabeee99d44571edc9a31f73c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:22 GMT
ADD file:9463b73933c9a0f2df3bbfaa2805027794a0e3a0cca69453b066ebc4644b6f06 in / 
# Tue, 13 Oct 2020 01:42:22 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:22:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:23:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:23:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ead5025e4e59e53184c941889a91b90e4e7af750b6f2e005952c8484512851fe`  
		Last Modified: Tue, 13 Oct 2020 01:49:57 GMT  
		Size: 52.6 MB (52587404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50bcb11b150787afba1f3af7ebbb7af8259b2b8b14121b74a6d0b01551ad97c`  
		Last Modified: Tue, 13 Oct 2020 02:30:25 GMT  
		Size: 7.9 MB (7879844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455355c490cedd80caaa467646ef3389e55170d8520f80248b97232c03d34b5f`  
		Last Modified: Tue, 13 Oct 2020 02:30:25 GMT  
		Size: 10.6 MB (10628194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0e82f26a95e6e817a52816fabb1c5164fea5eb51bdf5a55955277dc5d11381`  
		Last Modified: Tue, 13 Oct 2020 02:30:42 GMT  
		Size: 59.0 MB (59047155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9913f9f06699f843925abb2bd5b444ba1c2abb5cc3554ab9239112019170b5f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124541107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69c3214c0ef55135510b9821dad0dc51f04558c60f1cc0b17307b163aa64e9a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:56:41 GMT
ADD file:9c8616d4fabe6861a7f03ec7c1849957393374004adaf865fad27fc7e91057dc in / 
# Wed, 09 Sep 2020 23:56:44 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:42:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:43:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 00:43:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dd8dd816178223393e19e5b2cd1f62df2d94bc6d5c9c393d8da9f901c96e3f93`  
		Last Modified: Thu, 10 Sep 2020 00:05:28 GMT  
		Size: 50.4 MB (50413542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2d13ac158f55a44a68ac2d72292b51ad657a5202b688ec68c8cf3d7b42c7d1`  
		Last Modified: Thu, 10 Sep 2020 00:56:35 GMT  
		Size: 7.4 MB (7444216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c022e48ce06ce9a71076c5494577357f81ef67fdb3da661d48226f9f774c37d`  
		Last Modified: Thu, 10 Sep 2020 00:56:36 GMT  
		Size: 10.3 MB (10314983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37810e689b38ee68a82a6e11e092cb03c3b43af079aaac26e44b1719e537bc8a`  
		Last Modified: Thu, 10 Sep 2020 00:57:05 GMT  
		Size: 56.4 MB (56368366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9b0c03d8a1fe3da202380f6c7de94297ee3ce83dbcb25adb3e1f6ed10bcf26d7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119344235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a40382015a21e049b58f533a6746ba22730b58382f8948694fb21e2fcda7958`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:02:25 GMT
ADD file:6b1218c9574b91ad91309c12b66b8a83d37f3a3ead47d7fc3a16e3c498e6e102 in / 
# Tue, 13 Oct 2020 01:02:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:43:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 01:44:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 01:45:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:107486c9309dafb8e1d046960e1dca3c02d5aae566c72f8113cbb0f1ed15f9ab`  
		Last Modified: Tue, 13 Oct 2020 01:11:07 GMT  
		Size: 48.3 MB (48255653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb01673e64e8a48d10056720613123aae28172bfeb11020a3aba43cbbac68876`  
		Last Modified: Tue, 13 Oct 2020 01:59:15 GMT  
		Size: 7.2 MB (7183442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3439ff31f32aefcdeeaf2b053e0f8857776f05392e92baaa254c5446d40fc`  
		Last Modified: Tue, 13 Oct 2020 01:59:15 GMT  
		Size: 10.0 MB (9959277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ce14a99f926f046b0d2295b27dd91ff454c774130961e9dfc7dfe01ee57ad6`  
		Last Modified: Tue, 13 Oct 2020 01:59:39 GMT  
		Size: 53.9 MB (53945863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:522b03728e61a055176b183c87f2dda5c2d70feb88794e37220cc7e97a703d60
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129159085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d6b888ba92ba75072de6cc9126aa8a2d6ed9be7a15c8829bd12aa238322060`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:15 GMT
ADD file:af62f3e6ea7fec61b2823188f91b0f3419596dad24e9f9303c3305a3747d4350 in / 
# Tue, 13 Oct 2020 01:42:19 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:36:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:37:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:77774dc39e62096b335ade088d1f9f15b9cfba84ef4b0106507ec53b4bd6290e`  
		Last Modified: Tue, 13 Oct 2020 01:49:29 GMT  
		Size: 51.5 MB (51483868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7d9ffc760782b4e9e54ad713a8d51c982bb91d4571cbcdaddfd15199b58c4f`  
		Last Modified: Tue, 13 Oct 2020 02:49:10 GMT  
		Size: 7.7 MB (7745936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3602bebd6bd88919236d9b8aaed761e14585cf0d0129ae39141683ca7678c032`  
		Last Modified: Tue, 13 Oct 2020 02:49:10 GMT  
		Size: 10.6 MB (10636757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac51bff55f8abd95fb04d6b1b6c83ce20aa95d629d93a8dfe0528a765db3cda`  
		Last Modified: Tue, 13 Oct 2020 02:49:37 GMT  
		Size: 59.3 MB (59292524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ea9366aeb8d79c594427b39d2accfb06b13e56dc032b4c094090a0c5cfdd29ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133671932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29356c2e5c6b47284485f7bd29638261e71b78ac1285f421cfc1397f4105200c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:43:42 GMT
ADD file:71e92b8b05766d1d5d02c013ee4e6bfd49cfe21c2bd5ab2182af02e5e2493796 in / 
# Tue, 13 Oct 2020 01:43:42 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:31:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:31:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:32:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:04671281ee1c9a57e6e56404219f6ae19ebe375e509c240cbdce889f052d441b`  
		Last Modified: Tue, 13 Oct 2020 01:50:52 GMT  
		Size: 53.6 MB (53624141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47de0273945f6e2c47e2f3f03a477c27bd73945f6ad62e80267ca45b1bd029e0`  
		Last Modified: Tue, 13 Oct 2020 02:41:40 GMT  
		Size: 8.1 MB (8053959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b0b6fad1e883cd355dcce25d38d601d02eefec153ce528a98d0b38d4a84f4a`  
		Last Modified: Tue, 13 Oct 2020 02:41:40 GMT  
		Size: 11.0 MB (11015595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd96c2e2dd5b064c3f2b4644f9c8fdf61eb3eb5e96cf1c4f144aa8bde2b402e1`  
		Last Modified: Tue, 13 Oct 2020 02:42:09 GMT  
		Size: 61.0 MB (60978237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:623072dae44800710e2423a6d5b2eec38d479104171f16d15c52ac1eb7193775
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127235141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d129fb712a3c30dd9e967c82b6ee4ad285956103101cc252c08f974ac9adb3f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:10:19 GMT
ADD file:ec8eebd9c015be5ae41233496690d158f5f7d31b3dbece81b6474018168d339d in / 
# Tue, 13 Oct 2020 01:10:20 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:15:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:16:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:17:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:acfd16a511fbf47ee6caac9e14f0361f1b2a477e4e410835a21a56951f404ee0`  
		Last Modified: Tue, 13 Oct 2020 01:17:27 GMT  
		Size: 51.3 MB (51292191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c8c36fecc594af5a0fcd22383157160ab20328027a9a7aafcc7876e036c074`  
		Last Modified: Tue, 13 Oct 2020 02:26:36 GMT  
		Size: 7.4 MB (7400523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07514ca8c30d4614bc9d748c8ca9dec4b2481d32639fe54cfc45cc2d68aee7a`  
		Last Modified: Tue, 13 Oct 2020 02:26:37 GMT  
		Size: 10.6 MB (10639538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ed89d809ac68ebf4610853e2f5f0dc9ef101c69abe8a4dc2fdb558e07ad9c2`  
		Last Modified: Tue, 13 Oct 2020 02:27:30 GMT  
		Size: 57.9 MB (57902889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0d65706ea3cb3f0b117f3dbe135a21b86684ccda9d80b9d17b07c1d34224f463
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140724067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9fb4dfd6eb1a84b6269ae95b83313a8f3b3ba6d3ed141caefb660ff903b55b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:06:51 GMT
ADD file:6525cb187fc85a4741e9d9de398149d93f43e196e99a20d48f165a25a1a8f36e in / 
# Thu, 10 Sep 2020 01:07:08 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 03:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 03:31:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 03:34:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:184155505be08ee96b6e64926098f03c472ad33bae3d34b8f683480960d7b5d6`  
		Last Modified: Thu, 10 Sep 2020 01:30:22 GMT  
		Size: 56.3 MB (56336687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f84de13452ce499d161f512ceea2535494fd124e4903980cc88297c393465b`  
		Last Modified: Thu, 10 Sep 2020 04:18:28 GMT  
		Size: 8.3 MB (8307371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62889fb00d8e6d8533f5a3ae0d38209c3a2e220aefda427a5f00b595e3862e8f`  
		Last Modified: Thu, 10 Sep 2020 04:18:24 GMT  
		Size: 11.4 MB (11389809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d0d792fd0c71e7d5a634580e82d16f64ab3485e3ec0591357c0572795f9bfe`  
		Last Modified: Thu, 10 Sep 2020 04:20:32 GMT  
		Size: 64.7 MB (64690200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b0a3bc284401613824f404d81de9fc3aea597c8b5bac0ca5e1bfbce97ae20526
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127395555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d530295fa6020b82a7867bc0402d0a1f1797441d9d053c1096829d11513f671e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:39 GMT
ADD file:8ae741412fc2632b17f3119be3f00db5ac9da9165ec6ba803cecb706cca2e10a in / 
# Tue, 13 Oct 2020 01:42:41 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:07:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:07:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:08:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f8a9ab7d8c65b5068769e112907fa3def6a9a81b79ba5632dcc28f6bc45c59d`  
		Last Modified: Tue, 13 Oct 2020 01:46:00 GMT  
		Size: 51.1 MB (51120285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c6c2e1d37a743e5cb89bea0fbf288f3c97c58bd5e1e111a310a1968a8fa789`  
		Last Modified: Tue, 13 Oct 2020 02:12:16 GMT  
		Size: 7.6 MB (7552593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9d2e85355b3a65546bae45dcf206bd44a3e26e29009a1fcaaccec7cbdc9062`  
		Last Modified: Tue, 13 Oct 2020 02:12:16 GMT  
		Size: 10.5 MB (10505631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450cd2a37bc042631c0485843fea47b52793d6012a3c58241d6cbdca704d0c23`  
		Last Modified: Tue, 13 Oct 2020 02:12:31 GMT  
		Size: 58.2 MB (58217046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

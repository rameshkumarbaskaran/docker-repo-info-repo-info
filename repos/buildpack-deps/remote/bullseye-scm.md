## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:896b30798502abfc9abe813e91c3488c1ec0b930a7bb492d5a900c52c2f571df
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

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8d3c3ea73341c1f2756de872789ea3eb7a59154557dd5e816baa7385a266d9b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129424495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf12525ea9c00706afddb0f947a97706768508835bb3c63659f3b05dab5eb2e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:20:54 GMT
ADD file:375c01cd4aba0ddf77202decfeed5df5e3119ce460fcbf1f3b47f540a70b3864 in / 
# Thu, 10 Sep 2020 00:20:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:57:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 00:57:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:08d7334100fee80149028a0d0df44589b68e0c31592157808d18b68e6a572fd3`  
		Last Modified: Thu, 10 Sep 2020 00:33:04 GMT  
		Size: 51.9 MB (51906528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e2cbaa6fb6571d6e6f88e645061abb7c64ad18e76e900e6cfd8b80c5b36e84`  
		Last Modified: Thu, 10 Sep 2020 01:14:04 GMT  
		Size: 7.9 MB (7866624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70f330112cba767d415d7e4179b0dd52578b7685d2984ac61d9c3ba0884843a`  
		Last Modified: Thu, 10 Sep 2020 01:14:05 GMT  
		Size: 10.6 MB (10628764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a512e8a3ad92fa17f1debc71fe57ac4b49e1ffd4b1b80b5b847f6d5e48df83`  
		Last Modified: Thu, 10 Sep 2020 01:14:22 GMT  
		Size: 59.0 MB (59022579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0d65357164870dc7c817a3682d8e4d879021ede94c27dfc084813b09077e3717
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123995342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96348aea6bcec4b0444ae2a27071691978b495f077a9cb174f82546633f9797`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:52:26 GMT
ADD file:f71e0d87d6d096130aa8dce14ce4db75b3a50725e9ba2aaab46f722a444291c9 in / 
# Wed, 09 Sep 2020 23:52:28 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:26:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:27:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 00:28:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23e3aed2d466532e16ed7a54a2dc8d1ab497d8cd849573a7aa149e39f499eb77`  
		Last Modified: Thu, 10 Sep 2020 00:01:42 GMT  
		Size: 49.9 MB (49868299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57296d1a05acc9b2b6a146828bc5cd73f18a33087981038e29d2911236360b77`  
		Last Modified: Thu, 10 Sep 2020 00:51:46 GMT  
		Size: 7.4 MB (7444028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf329ff0c0ac4aa69298e3dae2a5539c0c7f11957ec83f3ae34b781fe1af258`  
		Last Modified: Thu, 10 Sep 2020 00:51:47 GMT  
		Size: 10.3 MB (10315041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3cadd83d92f88a8a5feb6e4917c4c36841c9e067f1bb16dd55109f787f57cc`  
		Last Modified: Thu, 10 Sep 2020 00:52:12 GMT  
		Size: 56.4 MB (56367974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:85a189fe7cea19e4f341abcd3c68a1097bf9f2f1d99ac52c507dc1b0c53c54fe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118705794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6825298bb19111f6c08c928f52084d7788192031ea6b2a90679965fcbd672813`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:06:19 GMT
ADD file:1cf6aad11149d2248c2d64e694eea8993365bc92e69acb766de8eed5ff5ea516 in / 
# Thu, 10 Sep 2020 00:06:24 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:34:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:34:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 01:35:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d74d0dbf37b1422ef3ad4850d0d2337a00c1b3b940052b8328d43b006d7cac98`  
		Last Modified: Thu, 10 Sep 2020 00:16:52 GMT  
		Size: 47.6 MB (47622633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39be7872e432bb84dd6799e4f7aea36b8e63f90690ab9a44e04241ca2c86b8cd`  
		Last Modified: Thu, 10 Sep 2020 02:00:02 GMT  
		Size: 7.2 MB (7184503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba87750aacaf06d58ec51afa56e4906f26eb6e094675669d666733b31b9313be`  
		Last Modified: Thu, 10 Sep 2020 02:00:03 GMT  
		Size: 10.0 MB (9959100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b151654e46e69be96bffc92ab40bf87d534d6125cea216288fc9486abd79d2`  
		Last Modified: Thu, 10 Sep 2020 02:00:29 GMT  
		Size: 53.9 MB (53939558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:456764d92d150277ff944a80bd582e02e0e3e671ffc22d375b8bfc3548d0aa9f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128464883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e53f4959ed29952caab2a521652504697dcfda9ec054ec138a41c89161f26ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:49:11 GMT
ADD file:82c33a26fb9be3ddaf17956539af2b205bdb6e28fe5ff1c7304ae8f294fe9581 in / 
# Wed, 09 Sep 2020 23:49:14 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:24:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 00:25:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a65667356fa05b061c6733c879afab36ec44c6877341c2527e321b7206a26b2`  
		Last Modified: Wed, 09 Sep 2020 23:58:05 GMT  
		Size: 50.8 MB (50825395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730279b4ebb859065c90bbf90b3ac77059bd7d1e6cdc143106e0994dca9f4c59`  
		Last Modified: Thu, 10 Sep 2020 00:40:35 GMT  
		Size: 7.7 MB (7743447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a2c8b657c8d1b22dc8f6d15821f7035a315a0900f84b26ef36c86803feb02c`  
		Last Modified: Thu, 10 Sep 2020 00:40:35 GMT  
		Size: 10.6 MB (10635675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c8357b95e1bce3c0d061d88bd56a0cbc03afe5af4f86cdd0057650adee23ef`  
		Last Modified: Thu, 10 Sep 2020 00:41:30 GMT  
		Size: 59.3 MB (59260366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:35c73902bcf2c5dd491fde53ccf6184669199d319b3e95be11a7996336fdae52
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133020755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3275b31243b9395293c4761ec832a49a387617196328bf3fe3a36afc9e15de91`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:39:17 GMT
ADD file:f37f3bb35b6cca1cef993e4f39f48aab88ed76e0c47d97d61b4329fd8c5c5d03 in / 
# Wed, 09 Sep 2020 23:39:17 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:47:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:47:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 01:48:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e5adf65093f5c6d699308a44f2173fac564be9f4e4daf24d82204c617b438d5`  
		Last Modified: Wed, 09 Sep 2020 23:45:45 GMT  
		Size: 53.0 MB (52969189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6830211bac3c1325ba53a3a4581992aa1d1916adf979c416833a3e9c0e9f24`  
		Last Modified: Thu, 10 Sep 2020 02:10:09 GMT  
		Size: 8.0 MB (8040370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7dd281614cde829dde09a35d83f8a4fa325cab69fafac8dba60a7b8950cae3`  
		Last Modified: Thu, 10 Sep 2020 02:10:09 GMT  
		Size: 11.0 MB (11013589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08863d0a092f025c74c2a9e8e76db66b3097078722465f8c26eebaa59a4772bb`  
		Last Modified: Thu, 10 Sep 2020 02:10:43 GMT  
		Size: 61.0 MB (60997607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:eaec1810300022db30b078ed90719de165201897ff16a9bdc25fabe2c5c17683
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126578362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5728913f772fdb0465c4c17426fc5e0ff19dc3aeb5debd71c7dbf46e54d721`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:08:32 GMT
ADD file:f875dea5461bc3a98c6c3dab6e2eafcf83ee8edb22905981e0dc44debaa18b43 in / 
# Thu, 10 Sep 2020 00:08:33 GMT
CMD ["bash"]
# Tue, 15 Sep 2020 05:41:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Sep 2020 05:42:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Sep 2020 05:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:51d9c21615eb513b443cf8d3194bcf27d511c5166a9688eb785755ea42a8612d`  
		Last Modified: Tue, 15 Sep 2020 01:11:13 GMT  
		Size: 50.6 MB (50615514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551731966e3741293759ffbd53b01ada1a4b84b2fb5cb7f190698fe3e27e64a9`  
		Last Modified: Tue, 15 Sep 2020 05:55:35 GMT  
		Size: 7.4 MB (7396754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb9f8e47af91313fec84689680bbd6c20a5a005b81e85eaf1f04ce83da60eff`  
		Last Modified: Tue, 15 Sep 2020 05:55:36 GMT  
		Size: 10.6 MB (10641150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130a2cf998f7fb148cf2098337d010a7854ba5420ee9674091fe3746461c3e75`  
		Last Modified: Tue, 15 Sep 2020 05:56:29 GMT  
		Size: 57.9 MB (57924944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c77446e09ee3ab2817db66aa68c9d91ca599351347593a3e8f2fb6d055b04213
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140150593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff940f87cbb947bb88a11f9a53da3b7c7b49fb5346395856524a11349025c5ed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:54:23 GMT
ADD file:4529de4df0d9d1d1c2fc4ea683021e7ff678a24ca45c21d9dfaeb7c4dc1da51f in / 
# Thu, 10 Sep 2020 00:54:39 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:03:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 02:05:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 02:12:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6146fe38f8409e50a43aec229f36623c0f8c195d2cdf9bad02573a9d952a31a1`  
		Last Modified: Thu, 10 Sep 2020 01:23:23 GMT  
		Size: 55.8 MB (55774504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be50b08123b1849db4a42098bf6c8ac1fa2b4b66f3529542c22e6ebd32daaf8`  
		Last Modified: Thu, 10 Sep 2020 04:03:25 GMT  
		Size: 8.3 MB (8295948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc42e2c525916d192694c8773ed6f0bf7a72f3fa13d751e4087189acf6827c6`  
		Last Modified: Thu, 10 Sep 2020 04:03:24 GMT  
		Size: 11.4 MB (11389924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ab50161d442dcd0b65170374cda4a3a14daffa715865256250897962df11df`  
		Last Modified: Thu, 10 Sep 2020 04:05:25 GMT  
		Size: 64.7 MB (64690217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3e0ba2a654b46559d6df1bdc7c65a171b7321ede89a2e55016e846916c89c75c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126741432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d8646c50c6005345fcb6b1be73815e012477fe41713783251905305dbef4c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:41:38 GMT
ADD file:d30705fcc57734260b517d32c4d610f1fe18e7d5faa78a22754774f5bf15eb9a in / 
# Wed, 09 Sep 2020 23:41:41 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:03:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:04:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 00:04:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b7fac0c9089d6ff39f6a7de3af657a8d580a7b074b45118b115539fd90213654`  
		Last Modified: Wed, 09 Sep 2020 23:45:45 GMT  
		Size: 50.5 MB (50468550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e4abf36c400373c14e1dc03dc7d41c9bb01249ef118a39b67294471b0cea9d`  
		Last Modified: Thu, 10 Sep 2020 00:11:24 GMT  
		Size: 7.5 MB (7537717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c291ff634945f7dc165f540d95c5d3958483aba31d45fbae0ee30d37ef13ca7`  
		Last Modified: Thu, 10 Sep 2020 00:11:25 GMT  
		Size: 10.5 MB (10504927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6369fe3859abc7090769cdf547264b790f6a68071ae32f9e9cc6ae6002948f10`  
		Last Modified: Thu, 10 Sep 2020 00:11:39 GMT  
		Size: 58.2 MB (58230238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

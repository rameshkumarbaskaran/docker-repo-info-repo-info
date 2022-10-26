## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:04e31fda8ac92a3aa996068ef9ed3659e9a55a466913ef9001ee96059775a485
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
$ docker pull buildpack-deps@sha256:2b7c78c9838082bca359f71999fa38a52f492caa004964cf492cf4d4f2d5c320
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100701852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a323f2f281532cab37e5f3f4b34f608af569da3cdf3b810caac0a438f8a313c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:33:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:33:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:34:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bb4286bac8e516f99402e13c31ac9edeef347075ab5c01322b42836bcf8d63`  
		Last Modified: Tue, 25 Oct 2022 09:51:54 GMT  
		Size: 7.7 MB (7747876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fbc8ca21a2e17468d6387cf181f407c621199a5e31b984af59f8a55f782844`  
		Last Modified: Tue, 25 Oct 2022 09:51:54 GMT  
		Size: 3.6 MB (3627190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e78ed8b1a1b3baff33d9b1b83961fbf908aaa1cb8db42215009adade171924`  
		Last Modified: Tue, 25 Oct 2022 09:52:14 GMT  
		Size: 60.7 MB (60748952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bbf9061337a03d7fd2837da7c393316f8fdafad306960931caa1de02c427c8d8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89879217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c2a25062bfb772be78271f4aaf6012114ce958ffd17e24cbd4204e809288e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:07:00 GMT
ADD file:0e30b9fd980776c745b113ac234367069202f461c4d888acb3225ccc0aa75385 in / 
# Tue, 25 Oct 2022 03:07:02 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:47:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:47:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Oct 2022 04:48:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88411d40226eb74e038e5d2cbedefbd7555c34298ed687d1073cf87740fab694`  
		Last Modified: Tue, 25 Oct 2022 03:09:28 GMT  
		Size: 24.6 MB (24588786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970743f747a5252a11cdfcabb172568d2939c95510a7edb7f8890b83b44c203b`  
		Last Modified: Wed, 26 Oct 2022 05:15:44 GMT  
		Size: 6.7 MB (6741828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df987fbe326e845bff146ef821c4e2727aa7f0f31131998b7aa47f06ac9f915f`  
		Last Modified: Wed, 26 Oct 2022 05:15:43 GMT  
		Size: 3.1 MB (3105786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f13e7d6c374ac32958c8e7f681db3cdcb91d95e0078225810968766392b3812`  
		Last Modified: Wed, 26 Oct 2022 05:16:08 GMT  
		Size: 55.4 MB (55442817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:328e8c05b0f0341747f5871823ad81ae7ac6e958a44be976bcca059cc132912e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99237200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238b304b5e34bc73bb2557c4303d7a9380f67900d30cac408cfa2c46b7c6b625`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:09:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:09:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 08:10:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f7d42f1359bed862a992a062b3c7cf025e6bf6625dc1ca56ae2c66d7250fba`  
		Last Modified: Tue, 25 Oct 2022 08:34:12 GMT  
		Size: 7.6 MB (7616212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc75acb9c1e02b10ddc3966608ccbac66c6fd9eeb3bff80797f9983f268a9b1a`  
		Last Modified: Tue, 25 Oct 2022 08:34:12 GMT  
		Size: 3.6 MB (3617606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d21db26b13141f20e7cce995a63f8234838277895d2d6d0e2ec4f35e659c78`  
		Last Modified: Tue, 25 Oct 2022 08:34:33 GMT  
		Size: 60.8 MB (60807384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b5156fdea407f78ae8f5dd5a40c70d5686fd01e7a1316d3896a123aa5f2d1e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116020776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d728b216db5852c775762c0dbeb7021e76038e61147d6565e4df9ebaf321e554`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:47 GMT
ADD file:013ddcea49540903962069a03762fe471452e8cf00bafeb530724940405797e1 in / 
# Tue, 25 Oct 2022 03:25:49 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:27:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:27:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 06:29:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:42e5f4d60d38e5070be91d6965be1cff1294e6dc275038002dc2ef1812233b0e`  
		Last Modified: Tue, 25 Oct 2022 03:27:44 GMT  
		Size: 33.3 MB (33300542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa48197ece6cedfce46328b98e2bd3ffa7f116e92dc0cd9aba21390a5edf11f`  
		Last Modified: Tue, 25 Oct 2022 06:54:02 GMT  
		Size: 8.7 MB (8705088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91159ec91712ffe519d3e9624103d9ec7b58e6b1959cad0b77145851e14fc55`  
		Last Modified: Tue, 25 Oct 2022 06:54:01 GMT  
		Size: 4.5 MB (4486836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c68813dea6733b577ebd8f432367b30fab9f0639692bc2e99d633f9347aff6`  
		Last Modified: Tue, 25 Oct 2022 06:54:33 GMT  
		Size: 69.5 MB (69528310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6e1c097aaa5b10d603b3ca7af97305eb87efa8eb846c6b08fea8968c3a45fe4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (97967486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cb9f67e31afed0eb376d14ac80a2758ecbb81e5ccb14b069d1b33c9da0399f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:11 GMT
ADD file:c657b467ecb15f1f4a49a5f04a525f38924750c8187c9ef9f0b886d0264e21f1 in / 
# Tue, 25 Oct 2022 01:23:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:37:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:37:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 02:38:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a63328f08dbd14148b5ffe154c18846ead48e759779d007b78ec3fb19f5f43a5`  
		Last Modified: Tue, 25 Oct 2022 01:24:36 GMT  
		Size: 27.0 MB (27016028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7f4256f9365e6546f5def4594e750767ee106712ba11997c58b0e9b15ab10a`  
		Last Modified: Tue, 25 Oct 2022 02:52:05 GMT  
		Size: 7.4 MB (7390068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c49cddcfee6d6315b4a734cc802ff8d05a8ecb16654aeca9cbd0076b7dec22f`  
		Last Modified: Tue, 25 Oct 2022 02:52:04 GMT  
		Size: 3.5 MB (3542342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8b09e3088369fc4b7c4afe1c6fa3627b4a08b7f6388e1e455d9bbb75dbe837`  
		Last Modified: Tue, 25 Oct 2022 02:52:20 GMT  
		Size: 60.0 MB (60019048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

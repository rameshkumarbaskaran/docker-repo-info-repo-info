## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:440a394f984d473ba8f8a8e2ba1ca3d6c1c1b7051c963a78eef134636f561d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ea4a50e747d5b8520bd77bfdce9398fc14417b6c9e8ba12cdfc2f82a10ba9d59
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330720700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c86111c2be12903474bed35d5bb40fded7436d0f486634c91b45f6d15cef4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:09 GMT
ADD file:15e5b0a35c4fc7a5ae0bf08f713bde738d2cfb06a30b8bd5780fabafb91d934c in / 
# Tue, 21 Dec 2021 01:22:10 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 01:50:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 01:50:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 01:51:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9aa4f47c6909274e4d7f0b2429a7ad24598b19c01da78245a16a3176f9acf847`  
		Last Modified: Tue, 21 Dec 2021 01:26:44 GMT  
		Size: 55.6 MB (55598801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f71e2132b1cfc0df72e7252fbbc759f38ec76718cbb194e3f3abae59f6c6f7`  
		Last Modified: Tue, 21 Dec 2021 02:00:06 GMT  
		Size: 5.3 MB (5282859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f2c25fefbc6f35b9aa1d2da6608ac2eca9de0a624ef3624ea94b11c7ed3db4`  
		Last Modified: Tue, 21 Dec 2021 02:00:06 GMT  
		Size: 10.9 MB (10904095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5817e8417410ab0f6ecb2677bde006e866e271aa33c4338c69a38955bc4b585a`  
		Last Modified: Tue, 21 Dec 2021 02:00:27 GMT  
		Size: 56.7 MB (56716774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea4021abe765ed06ddce893640f37d49e85186b69baaae39cc75351df52e4ad`  
		Last Modified: Tue, 21 Dec 2021 02:01:15 GMT  
		Size: 202.2 MB (202218171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e294facff8667c7890bd7d4c98d5579e866298d26619eb039f3485644cea61bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302204864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcefa6ade96b1ed76578d00e81a0c154a5b502aa9f56fdedf27bd821455d3e7a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:48:58 GMT
ADD file:06611eba7b36a7e9c8c68f1d8c97d596b024eefb00a7b0638c9ccbeb8a6f9142 in / 
# Tue, 21 Dec 2021 01:48:59 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:49:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:50:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:53:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:13e93eb93ae4e3d37ac97bb105a341f9c56baf0c8b9fe4707b27ad57f5633247`  
		Last Modified: Tue, 21 Dec 2021 02:03:43 GMT  
		Size: 53.1 MB (53058545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73be606123ef3d587583379ade2e43196a09d32211ca610ae8055f2a48d91e0a`  
		Last Modified: Tue, 21 Dec 2021 03:15:16 GMT  
		Size: 5.2 MB (5181568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4426a7d153510d4bd96e6bac61d8ea9195987680a4574d6a787782c29278cce1`  
		Last Modified: Tue, 21 Dec 2021 03:15:18 GMT  
		Size: 10.6 MB (10610681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883d1ad25106a20efdf246353ad7f7629ba6e0d3a9c79bf855de453cc463cf96`  
		Last Modified: Tue, 21 Dec 2021 03:16:08 GMT  
		Size: 54.4 MB (54386399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757dea867851bf74226bfa172bf108c3954b2201011524dfe73dda61031d3d77`  
		Last Modified: Tue, 21 Dec 2021 03:18:07 GMT  
		Size: 179.0 MB (178967671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:afcfa9a260620c068f01a9b333ef0bf0d5a443a112c00ba83639a0064977cb27
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289193887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90797aac0cdc8a6a2b7f8f12746c7bc0263dbe81af93b0c2a4d5b491381db539`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:58:11 GMT
ADD file:7ed54a4a4704538f37ad0755a81034bc1bd04ec05d6e2a10f3dc44aab517bd3d in / 
# Tue, 21 Dec 2021 01:58:12 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:41:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:42:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:43:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:45:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:661d8e50ead70cdfa65f1e6cee609c2fd7cee22ad5c09bb02a88c7d51c60da27`  
		Last Modified: Tue, 21 Dec 2021 02:13:26 GMT  
		Size: 50.7 MB (50698897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5d0b7054a91e67d50977b455394390d0f917a72170645e36baa0f3bf4cd227`  
		Last Modified: Tue, 21 Dec 2021 03:08:55 GMT  
		Size: 5.0 MB (5041369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a74408f958843b1528904123a2083d2d356be52a7c7b3159df85d62edcdb0e`  
		Last Modified: Tue, 21 Dec 2021 03:08:57 GMT  
		Size: 10.3 MB (10253302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dc7ba3304f4177c28f529682d8fde457f38c05eba7ebdff813e0818a2807f0`  
		Last Modified: Tue, 21 Dec 2021 03:09:44 GMT  
		Size: 52.3 MB (52255497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1006d707084329ac0148f4f026aad39c79fddbf56052c16a1acd379e49110b4`  
		Last Modified: Tue, 21 Dec 2021 03:11:31 GMT  
		Size: 170.9 MB (170944822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3e319813b7f2d7f72e9b10aa3593c22fa3fd7578c3557c2c432af5af6368680a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323408764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3bcb1de437525f965c07907fdbbfefdda6672537e5501542984e253ee2adc0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:41:45 GMT
ADD file:c64482c2e0b0935b000b024e468499d2586b78ca5c64b035ded7ce33f1dabe14 in / 
# Tue, 21 Dec 2021 01:41:45 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:10:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:10:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:10:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:be902f523b4c4ddf53ea157e340cd7ce836ec2a0952d6f18602467352524e312`  
		Last Modified: Tue, 21 Dec 2021 01:47:42 GMT  
		Size: 54.6 MB (54598073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae3b1dd188183d78f548c40b842d6abda988dc1e02042a8d2fbba1292db6225`  
		Last Modified: Tue, 21 Dec 2021 02:21:21 GMT  
		Size: 5.3 MB (5271381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d762390d417c63f26301db70b2fc0b6cbfb2a625b710902a4efa39a4fbe7eeac`  
		Last Modified: Tue, 21 Dec 2021 02:21:21 GMT  
		Size: 10.7 MB (10679800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a737f25eeff639378bcc151ec6663db78937cc6769ac1822011ac7d273f3638`  
		Last Modified: Tue, 21 Dec 2021 02:21:41 GMT  
		Size: 56.8 MB (56754689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13dac7ea5a877f55f482350c53a691d593fa89bdd4697e972157874eef96e484`  
		Last Modified: Tue, 21 Dec 2021 02:22:17 GMT  
		Size: 196.1 MB (196104821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c410a3b387de6e77c2b75b9ceca69720f8727ccd0995a5f97b8c219da83e9e66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.8 MB (333778264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b803e029ea2ff6b16892fe4c15ea422d724347fb57c341ca7f90ea2f9b25f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:39:06 GMT
ADD file:f5394800b665e61b6f319d6dffbccd66c1172d4e9fd1db6ba962ef5aa177c353 in / 
# Tue, 21 Dec 2021 01:39:06 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:11:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:11:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:11:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:13:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:75388d3fd5f848339be12f5cd41cdf79effd086f4656396bfbac934b7f1f715c`  
		Last Modified: Tue, 21 Dec 2021 01:47:16 GMT  
		Size: 56.7 MB (56658883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de7e33a377d91eac773d98f83f6ca3f85f496a95ef1607a2f5af89fb4471391`  
		Last Modified: Tue, 21 Dec 2021 02:24:06 GMT  
		Size: 5.4 MB (5414374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4180045f386d2f79d4770aa88797a1fda448758575d57afc6ea4e781dc548b5c`  
		Last Modified: Tue, 21 Dec 2021 02:24:07 GMT  
		Size: 11.3 MB (11285476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c98f4c5e2e21a446971fb90d2f11dea323e9e79c68d747e0a9e0a487d9a02b`  
		Last Modified: Tue, 21 Dec 2021 02:24:34 GMT  
		Size: 58.1 MB (58132384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1988a2df175d53c80c25c439241f37d674fb84fefcc1c0a549ac9e8bb24a89d2`  
		Last Modified: Tue, 21 Dec 2021 02:25:27 GMT  
		Size: 202.3 MB (202287147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7ac9b3b6a9460e4e6cb4ecec98a60f445f3ac48ffbbba42ee268a17c1f8b3591
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311446371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf08f11ec050015268d4bc7d9ee8dd5cccba86c41762df3d9df45101b8225fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:07:47 GMT
ADD file:41547ce5cf30425be5612cd827fbdd2cf3e3190ecb39bf4c5a634512db860237 in / 
# Tue, 21 Dec 2021 02:07:48 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:42:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:43:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:44:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:47:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:847df5d6ab10ba0e4a41a13ce3d04aa9d5b5c826a90bc36162239e7587e48cee`  
		Last Modified: Tue, 21 Dec 2021 02:15:49 GMT  
		Size: 54.3 MB (54302729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af94995fcd9a58273ccc81803188949261f64b3a771444b5dc0408ffb3ad8349`  
		Last Modified: Tue, 21 Dec 2021 03:02:36 GMT  
		Size: 5.2 MB (5239498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ab30ebbf9013d67a4457a6c6b22d4d7ab04825a9c236c9eab72883ea9b0bd0`  
		Last Modified: Tue, 21 Dec 2021 03:02:38 GMT  
		Size: 10.9 MB (10906973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a34781de14f880f5e9c3c649e97a40aaa2fff70da9701593835e36519b9debf`  
		Last Modified: Tue, 21 Dec 2021 03:03:38 GMT  
		Size: 55.6 MB (55553253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86e197ffb2c6762711fe0c8a770f0ee93bb0354d20218bda16e3e430d4a5ef8`  
		Last Modified: Tue, 21 Dec 2021 03:05:55 GMT  
		Size: 185.4 MB (185443918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:58f6500f11e23968f266cc49c2f5370789ffd18b3bfb690654da01e57b60d875
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.4 MB (340379259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772521788d04b6273f90ac475b05e6466634a95922596c1cfc4958d43c1df2e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:18:58 GMT
ADD file:b2445892db6f22a700090e84ea01cec8156666af13bbd1943ff76648f9b45fa7 in / 
# Tue, 21 Dec 2021 02:19:03 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:51:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:51:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:53:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:58:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:acf94744ccb1210214c86a9a0cddb19c2809171609310c507f8e988f1e399199`  
		Last Modified: Tue, 21 Dec 2021 02:27:45 GMT  
		Size: 60.0 MB (59991767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa307bdd256e07a4f80e7738435e94bffc8cf569eb431ad77f525c6f8a3278f1`  
		Last Modified: Tue, 21 Dec 2021 03:28:32 GMT  
		Size: 5.5 MB (5542942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ed5e5aee08e16352da62214f310fa20dd79bcc6ab93d84223f6bf298802214`  
		Last Modified: Tue, 21 Dec 2021 03:28:35 GMT  
		Size: 11.7 MB (11658731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea61bd6a58f3cf41e443ef5b4a42ce41bf8151dfdeecd58eab448e045fc58b03`  
		Last Modified: Tue, 21 Dec 2021 03:29:19 GMT  
		Size: 61.4 MB (61384264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ee031f4f88e53c5cb1cdfb0d283ebc10e253fe03880ce741c874ba0d7a680b`  
		Last Modified: Tue, 21 Dec 2021 03:30:38 GMT  
		Size: 201.8 MB (201801555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a43df0bd72d2342600f311af656cfccda041c0f1f681188e701f03192cd09e39
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303072312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b353df6f9f8591660d87aeb32a7e0904565b70b8d850b14a409946093c80055e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:41:36 GMT
ADD file:c9626c75e4b53a0e71f37a2a3df45699d003ae102e7e3eedc97afe7897f82180 in / 
# Tue, 21 Dec 2021 01:41:42 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:07:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:07:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:07:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:08:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:341c5a56ba0f7b7f22f0613addb31ee3342e410686dda8753a049d0bd1f319f3`  
		Last Modified: Tue, 21 Dec 2021 01:47:23 GMT  
		Size: 53.9 MB (53888441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8be60271199953262ee02a4148a07af9a66fa017104d2d03d65d92956150fe8`  
		Last Modified: Tue, 21 Dec 2021 02:16:46 GMT  
		Size: 5.3 MB (5263047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100220edd1ab3877c378dcbe4658541db3dcee1ff143d2e1e5b5d75d67380a9b`  
		Last Modified: Tue, 21 Dec 2021 02:16:47 GMT  
		Size: 10.8 MB (10796850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68675f5371673f128e99d0c8a3b555294317faf74cbdf4da6d9b9221c2459f21`  
		Last Modified: Tue, 21 Dec 2021 02:17:01 GMT  
		Size: 56.1 MB (56095562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e326d2fbbc64eec5f2a2fd56eda6f2dbd24a14e5d6eaeda7eee6c4f7d0c76e4b`  
		Last Modified: Tue, 21 Dec 2021 02:17:26 GMT  
		Size: 177.0 MB (177028412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

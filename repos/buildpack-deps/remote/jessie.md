## `buildpack-deps:jessie`

```console
$ docker pull buildpack-deps@sha256:19f3d2ec91e567529b898eadfa3dd0818920bb880310e8290a14faa6bf98eff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:jessie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9451efece67b99398887e5190f1abeab9ad536dbff3a5e960678a56d22d61628
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247164284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e5edd8fdc1e69ea3d3d627ee25820b24c8e506a50edb1f65d0b0cad133d063`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:15 GMT
ADD file:00e3c0ca649cf82da02cd7fec7b3121205c2c54c4569209a2212c4924c73d5a9 in / 
# Tue, 31 Mar 2020 01:21:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:00:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:00:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 02:02:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:04:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f27d6ed8cebc4be4a992767cb74cd433e5e145ae55c57e9e913e47d315b1dbdf`  
		Last Modified: Tue, 31 Mar 2020 01:26:56 GMT  
		Size: 54.4 MB (54389951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2886394fe026f40712d4f22ecfe40e26911d758627d04e684d9d5ff5637296`  
		Last Modified: Tue, 31 Mar 2020 02:10:58 GMT  
		Size: 17.5 MB (17545721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c79486f9007497ffa7c18e154e42d395db78950bb662ad3788d208c2b7b9599`  
		Last Modified: Tue, 31 Mar 2020 02:11:11 GMT  
		Size: 43.3 MB (43333264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2071d428ba7a22c15ddc433fcb14a7bc30e7990695c11886519abb304c6b97b7`  
		Last Modified: Tue, 31 Mar 2020 02:11:35 GMT  
		Size: 131.9 MB (131895348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c702e637ef4204ef2f3da553876c25d24441b5786eb6338154603015bd9b1ddf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227142558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cdc6b4254529083c6c008dee03f98ee365377a69ba7dca6d43f09b9a4465f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:25:13 GMT
ADD file:631f76030613657eb3d82228323e5a3860b5141b58858b628bee342bd47d427d in / 
# Tue, 31 Mar 2020 01:25:17 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:29:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:29:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 03:31:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:35:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ebddd0cca47bf5452de875b55a7b0a10e182a550196df63972f211a03e9f7cd`  
		Last Modified: Tue, 31 Mar 2020 01:33:28 GMT  
		Size: 52.6 MB (52580205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e80167505cea44898f4dce8e6007acae3e6ccf8b0b3b62d514cb4d769474d4`  
		Last Modified: Tue, 31 Mar 2020 03:48:54 GMT  
		Size: 17.0 MB (17037090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7962f7d2575522a8a0df557e93a9845753c76833c794b332df26816e3213f676`  
		Last Modified: Tue, 31 Mar 2020 03:49:15 GMT  
		Size: 41.2 MB (41159943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd4b8d411f9744bb3e6e4c8707228ecd533bdeecea6dad8285163abcbca29f0`  
		Last Modified: Tue, 31 Mar 2020 03:49:58 GMT  
		Size: 116.4 MB (116365320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fa89514567656f5b914ac5ef53425dfb5dd07e9a60707bb19e17944662d6dd9a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221422629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de55fb02a33499d13836e7028a05e6efad1b8466943f3239bd26df4bc9dd548f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:48:35 GMT
ADD file:3345f549ac73be9cbff84c9a9992a29c6a50a098e6ec75781abd7e752f2e4905 in / 
# Tue, 31 Mar 2020 01:48:38 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:43:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:43:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 03:45:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:48:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b42378553088c1b5fa4e7b74e80d9e3bc23e8120256271a16a71718555bb74a9`  
		Last Modified: Tue, 31 Mar 2020 01:56:46 GMT  
		Size: 50.3 MB (50303700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7396438102c898ad52f1a70f57579ff2986e776b6305e87017a39204c1fb0`  
		Last Modified: Tue, 31 Mar 2020 04:02:07 GMT  
		Size: 16.7 MB (16723402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abce9473207298579845f5680e3c4deb2fa262abfd526e63c2e7052a79513b36`  
		Last Modified: Tue, 31 Mar 2020 04:02:30 GMT  
		Size: 39.8 MB (39775371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfb8c8682f67b7ad9263b5faf8e31dbd100b35ec33f8d8491f25e2d70b4166a`  
		Last Modified: Tue, 31 Mar 2020 04:03:09 GMT  
		Size: 114.6 MB (114620156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:aeb7ba7167b7eb3aaaabb3eed9e932109d2e0b19d7d4b122107d2d4418cf31fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254314673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8663b9f2f6bbc4a8053364ccf1a9a63c98ed4357fe1a29e8bad564907dc0bf98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:39:59 GMT
ADD file:ee61b11b0132f3aa493c1fe2d59c8c7225e31b99c52f87f49a49512a80a203ae in / 
# Tue, 31 Mar 2020 00:39:59 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:15:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:15:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:18:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:22:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f263b30518dd64881c8ace989042a8efd1273a1175e0dc751ca62444e9f2ff81`  
		Last Modified: Tue, 31 Mar 2020 00:45:52 GMT  
		Size: 54.6 MB (54607453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f5a9dd559c3a0035cf2826e46fcddd2f78535e67543e52c97156d68f2b89b6`  
		Last Modified: Tue, 31 Mar 2020 01:30:29 GMT  
		Size: 19.9 MB (19855790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e4a737961a715ee92034bb56cf77c442fa2e42a168bbdea4cdf47ae036de6`  
		Last Modified: Tue, 31 Mar 2020 01:30:46 GMT  
		Size: 44.0 MB (43976045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7728564dbb10e1d2b344529700b32e3d00bd06e7ab0eba73435a5c188448417f`  
		Last Modified: Tue, 31 Mar 2020 01:31:28 GMT  
		Size: 135.9 MB (135875385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

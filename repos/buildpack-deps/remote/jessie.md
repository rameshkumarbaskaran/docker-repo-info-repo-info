## `buildpack-deps:jessie`

```console
$ docker pull buildpack-deps@sha256:57ae3a5389532f3ede620da19ba1eb6ffeb4990bb9c9b150fb8969519e300aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:jessie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fbf16e7c228db3727647bc52ce90282796f698686ab562606c70f7e0c5091c1e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247182744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d819310eca30be6edda7ec0950a0c1c6de826521911c986443971f283fc8415`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:24:00 GMT
ADD file:ca64ef47722e4bf4beeab729a34cd854fe7293a0a2a0a2a92e6f1347c071dfe9 in / 
# Thu, 10 Sep 2020 00:24:01 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:03:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:03:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 01:05:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:08:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:290431e500161a90ac38ac8631791acb27e14a913613b60b3df58f839168df40`  
		Last Modified: Thu, 10 Sep 2020 00:34:21 GMT  
		Size: 54.4 MB (54389019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcaf1dd00a337044e2c0421947b13d7390883ef55a08ff9ea58d13ce59784328`  
		Last Modified: Thu, 10 Sep 2020 01:16:59 GMT  
		Size: 17.5 MB (17545982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478d2f36706aba42a38a1d269f4e5f9e733730c04955e96a04d508b1cd9d589f`  
		Last Modified: Thu, 10 Sep 2020 01:17:17 GMT  
		Size: 43.3 MB (43334104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a94a50b39f16528d3bf36d3579aaaa7375c54edffd686c944f42b151b2476d`  
		Last Modified: Thu, 10 Sep 2020 01:17:51 GMT  
		Size: 131.9 MB (131913639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b5d788b26b95577fb583f21d5cc5e1015edff05bb9a2b83852e81ab3db98bada
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227154588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e1237c5e76f0169bb6d2ee5cdd480c2a64976d0db2778b2dc202a4ef18021f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:15 GMT
ADD file:b5770ada526014c416df31779f0c640c62a5e53e8e018a6201d507999ac34e18 in / 
# Wed, 09 Sep 2020 23:54:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:37:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:37:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 00:38:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:42:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:82ebff95f0e21d655344637482b367c7ea0db41b80cbc667bd980d2141287029`  
		Last Modified: Thu, 10 Sep 2020 00:03:15 GMT  
		Size: 52.6 MB (52583713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f40e46cda9c751ff385c796d48a3c39740220c3885866739fe62640f9437afa`  
		Last Modified: Thu, 10 Sep 2020 00:55:04 GMT  
		Size: 17.0 MB (17037321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bd6814b5011e45af4aaee011465ebcf614eef4d29dab5a87d8a3fed3655f0`  
		Last Modified: Thu, 10 Sep 2020 00:55:28 GMT  
		Size: 41.2 MB (41155851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793f4aaab1b4b812ca4076ce91369874ff9de166e35aca03da1a7b38341b8b19`  
		Last Modified: Thu, 10 Sep 2020 00:56:25 GMT  
		Size: 116.4 MB (116377703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b0c337a6b187a6f086c42a6e51bb968042c6a9994d9680031feff16c91ee2eae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221441248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2192bc785ecd306d798d0d8b918e7d069bdb6b34d6aca94cd6aaada01609ab9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:08:32 GMT
ADD file:6c1ccdfbdb357c0b130cfe85bd05903e56f365e3d93c21c70339151862d2897a in / 
# Thu, 10 Sep 2020 00:08:34 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:44:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:44:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 01:46:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:50:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3bf2610be79f89db91594c41fa743370fc433e9e9898fa5d42098ba30efd7f9d`  
		Last Modified: Thu, 10 Sep 2020 00:18:15 GMT  
		Size: 50.3 MB (50305547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a9c931dec194117f2ee5eecc8d09f5847406d2a176f0a7256b132a77174e42`  
		Last Modified: Thu, 10 Sep 2020 02:03:12 GMT  
		Size: 16.7 MB (16723607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b2690d60f65f38c5edeeb9ff525bf34649d4aeceedc09723b56dda737b2f6`  
		Last Modified: Thu, 10 Sep 2020 02:03:33 GMT  
		Size: 39.8 MB (39779496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1031d62373d75e41b77b6584c7bc351e4368955914667fa07b54c1a57aa49455`  
		Last Modified: Thu, 10 Sep 2020 02:04:13 GMT  
		Size: 114.6 MB (114632598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2ac48dac3fcacceac42fcada6e189a84944750e5e12af741c3b1974876c2e19b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254341679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac095a4606afadf69055cdf60b25a7def51acc2e32ce2c7c17fca6739528f22`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:37 GMT
ADD file:b8a03a5f95e2490a27b297173fd17ea8037e2db6c1619ac9e84d781ff97ecba9 in / 
# Wed, 09 Sep 2020 23:40:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:54:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:54:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 10 Sep 2020 01:58:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 02:03:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a11948377c3d4859427c8f59e5f3716e2aba1cb63cc4e9dc8807d8e647dc118`  
		Last Modified: Wed, 09 Sep 2020 23:46:47 GMT  
		Size: 54.6 MB (54609479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bc82823dc8235bc61ea05f4d8421c65972757bede832556e79ce352c099f4`  
		Last Modified: Thu, 10 Sep 2020 02:14:34 GMT  
		Size: 19.9 MB (19855914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f993ff77deba249612d2a2fe059efb48af19e36b5559a641be9a95dfd9acb67`  
		Last Modified: Thu, 10 Sep 2020 02:15:01 GMT  
		Size: 44.0 MB (43989530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1921f4ac03f1876f7ba05481a9d12b8a66f3f413a872aad434a1455b26842e`  
		Last Modified: Thu, 10 Sep 2020 02:15:53 GMT  
		Size: 135.9 MB (135886756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

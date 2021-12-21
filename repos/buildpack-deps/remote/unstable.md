## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:bbc9664ad5c216b776ad3b4d90502a27f0f196dd7e94902ebf97e93abf53313d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:497c82707a39f892cf795391514e83174ad44aee5cdffe367311c7b9c782e4c3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.4 MB (331405495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3624f73116d64f9818fd97c8954b478a55b0322c5b21570674b0e2c72dc5d407`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:53 GMT
ADD file:ce4b0836a3fcb4df3c14bacf996ad27dde10d17f63fbf745c09d6ae62c3e2cc8 in / 
# Tue, 21 Dec 2021 01:23:54 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:54:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 01:55:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 01:55:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 01:56:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4c476fbbe1d7eecc32473e300b1659f1eaf7c11eff20d52cd6f7471c94062564`  
		Last Modified: Tue, 21 Dec 2021 01:30:07 GMT  
		Size: 55.8 MB (55798023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c6bd99048b6b72b33b515cda942b7e40ca1d3de2b2f9cdd7bcb90dbb74274c`  
		Last Modified: Tue, 21 Dec 2021 02:03:54 GMT  
		Size: 5.3 MB (5276774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492abb693e033360d88b0b5fc39af18ee3a635345217fb4fa41328e278d7136b`  
		Last Modified: Tue, 21 Dec 2021 02:03:54 GMT  
		Size: 10.9 MB (10904165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1da4768c8ef0bf34a53ed37a7a7581bb0aa27f68e2047d84c74fbd9e6bd604`  
		Last Modified: Tue, 21 Dec 2021 02:04:12 GMT  
		Size: 56.7 MB (56718041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c27ff0215ae7bbd8239e97dfdc5949dc3c2ddb87163b48af5c7f1ab6b42f13`  
		Last Modified: Tue, 21 Dec 2021 02:04:47 GMT  
		Size: 202.7 MB (202708492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d1d4aa545f783b4c1636aa4788eb588704d079114d506b4b54e950b5b4a10ec9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302620580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef5a9db3bb9e89afecc2e5855834c46af92f754ea71acf42ab52ee393a14320`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:53:50 GMT
ADD file:61604460e02950a274e51fc98393073e2b68e279308b9696e87d53530bf47fc4 in / 
# Tue, 21 Dec 2021 01:53:51 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:03:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:03:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 03:04:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:07:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2252da0fe003db28a23847a348e614635e01bdee48388ba4a2e8f08591bb48dc`  
		Last Modified: Tue, 21 Dec 2021 02:10:36 GMT  
		Size: 53.3 MB (53269288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb0227efa1a180434991f165be712afbd262dce6a1fb96d1e06a75dd6c15510`  
		Last Modified: Tue, 21 Dec 2021 03:24:34 GMT  
		Size: 5.2 MB (5180246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1befa24c2479fa4c965693e683ea2899180a18f0f5e15a301ad8367add88cc`  
		Last Modified: Tue, 21 Dec 2021 03:24:36 GMT  
		Size: 10.6 MB (10610486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccf6e47632f9e757265ab81ed95477d5592cfb414aee5dd1d06090fb7af694b`  
		Last Modified: Tue, 21 Dec 2021 03:25:27 GMT  
		Size: 54.4 MB (54386233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6086d872ef2b31cbb00211c131972241a56cd23f4a8aabdb1c6302d30e1a40`  
		Last Modified: Tue, 21 Dec 2021 03:27:26 GMT  
		Size: 179.2 MB (179174327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1f74c9a2231c45357e0f7b8adcdc6410e3f51eec82968701a08e7b3756a3ae14
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289623872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf36724976732d35f7f33af5aad4baf1ba42a6382252db92f50b5e654693c2b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:03:18 GMT
ADD file:0d5a8f9dfe2d9c5be9a0c7bc6937d1eea64c660ed161e798c852f8e3998ee095 in / 
# Tue, 21 Dec 2021 02:03:19 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:54:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:54:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e7bae00ea7d8195a01bb9d7101851880c4ca29ce9c6a4d32acacd59ce6a3436`  
		Last Modified: Tue, 21 Dec 2021 02:19:52 GMT  
		Size: 50.9 MB (50894650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc192de0e363b378b3d0c50ee0848801b2cc09a505a5242566d80b83658e843`  
		Last Modified: Tue, 21 Dec 2021 03:17:32 GMT  
		Size: 5.0 MB (5037229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3403b6d74fff353f4564db0a15852a0d94b1910fe6e3687121c5fa14ec5046d9`  
		Last Modified: Tue, 21 Dec 2021 03:17:34 GMT  
		Size: 10.3 MB (10252633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb8a7423b98ff03e578c460463d8d500aa39ae23fc1979cb20cf13ddcf662ab`  
		Last Modified: Tue, 21 Dec 2021 03:18:26 GMT  
		Size: 52.3 MB (52256000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c005a180806798e2a046ed9cd02d2d2ac9ca80a5beb2d588db1b509da2a5ef3b`  
		Last Modified: Tue, 21 Dec 2021 03:20:12 GMT  
		Size: 171.2 MB (171183360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6dfab68b9b24040e09b6bfa9fbea8f2f63a5286a0d05602df19c11d4ed15565e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323910369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5375a7d67bbf91c6f0c97bd51cfbd906528a53d4edaed8fe27d64ef78e0e1aed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:43:45 GMT
ADD file:7c4ba9d9936c0139eeef9f235c0d6840aa3c32d40904663e82e285a1b34d3a75 in / 
# Tue, 21 Dec 2021 01:43:46 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:15:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:15:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:15:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:16:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ff79c5138bd3b6ae9212e3b674731e907981317ed2018a35ca98f456034d18dd`  
		Last Modified: Tue, 21 Dec 2021 01:51:23 GMT  
		Size: 54.8 MB (54780864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04ea6899cdef9e4cb3add824a5c066cfe56407ffa977a94114981f8c9e02493`  
		Last Modified: Tue, 21 Dec 2021 02:24:57 GMT  
		Size: 5.3 MB (5263545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d6eba4116602817637a346f0e2c8ed4adf77ba0f6d395eb6b49df6d42761b6`  
		Last Modified: Tue, 21 Dec 2021 02:24:58 GMT  
		Size: 10.7 MB (10674534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffa7de7b15c6883e577b019809e1343d6f6d9c4e790ce8ea84b0c42300324d0`  
		Last Modified: Tue, 21 Dec 2021 02:25:19 GMT  
		Size: 56.8 MB (56755865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941b840fcee9d6e79a57b6bab0dbd40d77af26fe56adf63d9adf135486592808`  
		Last Modified: Tue, 21 Dec 2021 02:26:00 GMT  
		Size: 196.4 MB (196435561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c3aa081ead692a1c600ec78fccf6493780dca8dacf9acc76e45dc220260d7628
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.6 MB (335636781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd935f0c0872d2e4ec9b848156dc8efea55badb71beadd96e326ba718a2671b5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:07 GMT
ADD file:7c506c9d86a63bd33b2bd42ba9e380551bac76c3ef7352900f2acd644f4c8540 in / 
# Tue, 21 Dec 2021 01:42:10 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:17:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:17:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:17:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:19:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4134c3f595c8eb15f3af8157a618c36c51d0cf4948eb0bc00ce1697bab8e3d81`  
		Last Modified: Tue, 21 Dec 2021 01:51:54 GMT  
		Size: 56.9 MB (56851682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39f58d3b3754f23bbc0ceaf7adab7ffcc255c02bf6a043aff6842dd0cd45d`  
		Last Modified: Tue, 21 Dec 2021 02:28:54 GMT  
		Size: 5.4 MB (5408518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769abd0d85d00c570f55ee96473cec596d53c5a8292473578a15779b5e36e82`  
		Last Modified: Tue, 21 Dec 2021 02:28:54 GMT  
		Size: 11.3 MB (11270083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edec29419a6219e77259f3179317cfa40969486314c93fb7616fdede0a463d5c`  
		Last Modified: Tue, 21 Dec 2021 02:29:21 GMT  
		Size: 58.1 MB (58133925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8dccd8068a85a30496088980d288ce2743048e58585a2337c3d1847c4dafea`  
		Last Modified: Tue, 21 Dec 2021 02:30:23 GMT  
		Size: 204.0 MB (203972573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1f565510d4e1d7a6274e45bc4e18c53c74de5b40796f7c866c36f1c2224b47b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312190626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f2c755acca11d252337464d66e1a01f2043cab749055a4e4378ad35e95772f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:11:24 GMT
ADD file:03fe06379d2aa624e1b4f2fa09346703a6e044943801a3b71ad48db009afda1b in / 
# Tue, 21 Dec 2021 02:11:25 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:58:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:58:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:59:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:01:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1b2781e827d3c7d5377a11eaa940ec91a05b3c9be49542abedda2252f7b4fd82`  
		Last Modified: Tue, 21 Dec 2021 02:21:58 GMT  
		Size: 54.5 MB (54503889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831b577e1c4668fee3d0cfe74f3d2215a337eda6285705829c5761ac52d24433`  
		Last Modified: Tue, 21 Dec 2021 03:13:30 GMT  
		Size: 5.2 MB (5235777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648fc2b6c4969cde98966d9fba39c75427177d2b73763f69cd64e55f0b27cacd`  
		Last Modified: Tue, 21 Dec 2021 03:13:32 GMT  
		Size: 10.9 MB (10907743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e45696bac398ffc5f45aa4b095cbb3846957aa140d812fe650783333cdcc021`  
		Last Modified: Tue, 21 Dec 2021 03:14:31 GMT  
		Size: 55.6 MB (55554025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdeef9f351014671aa53d26b0719d958101397b4885e8fe8f2c267196a1702eb`  
		Last Modified: Tue, 21 Dec 2021 03:16:45 GMT  
		Size: 186.0 MB (185989192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b2b02733a114d7adf9b05508ce0ef4dfab94e076334730c35680cf34e69be9eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341422672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d97be89ac1ba6e0f557a57ca3f764663e57ef809c40358c3cc153e9bb8eabc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:22:14 GMT
ADD file:641bd15b93416ef98057364d15a9dc024ad99715a857b95b132e59fa84794dc9 in / 
# Tue, 21 Dec 2021 02:22:20 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:19:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 03:20:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:25:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1afc4e26929331434b14e0ce909f34a23e7896e101e78bc5d9426f4bde69d912`  
		Last Modified: Tue, 21 Dec 2021 02:31:35 GMT  
		Size: 60.2 MB (60199744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9340a0af36f9cb5acf1211719a4c267941994b285c90c83d471fa003822f9809`  
		Last Modified: Tue, 21 Dec 2021 03:33:55 GMT  
		Size: 5.5 MB (5538004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3d148fb84a5de0565268fea6e6c976afdc2985b95421dd2e6b55a8579625c2`  
		Last Modified: Tue, 21 Dec 2021 03:33:56 GMT  
		Size: 11.7 MB (11671846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1096dbf3a5dbecdf522da5839970d63cb8589b951877bd58c31e92246412b7ba`  
		Last Modified: Tue, 21 Dec 2021 03:34:20 GMT  
		Size: 61.4 MB (61384627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297fc8e7299498d81fc01a709f5135d9f427c97c23235754805b519e87f8e105`  
		Last Modified: Tue, 21 Dec 2021 03:35:08 GMT  
		Size: 202.6 MB (202628451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8eba6bd76e364d31f470138d12d10a3c1604ee5a3cef225f1a3f478f5abfc74c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342740508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a6357ff1e99d258d501d195f32663948044cc626d7fe2fa1ec67b1a910baae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:14:08 GMT
ADD file:1dc8a81ea9c954e594eb32623a82cdfb528586b569a915ba8f70a49f68a6f7fd in / 
# Tue, 21 Dec 2021 02:14:10 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:57:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 03:02:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:10:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6b741955e06623f1924320507da1630323c4cf1d6489febc99917464e765860`  
		Last Modified: Tue, 21 Dec 2021 02:30:31 GMT  
		Size: 51.5 MB (51541457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91689f9aadadd96fe4e4ad4ed92ff1cb6a48034aedc9f41e14d54cf85bcdd039`  
		Last Modified: Tue, 21 Dec 2021 03:34:04 GMT  
		Size: 5.1 MB (5089016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a290be0dbc2a1d1f5f12db96d9dc0949f33b55d33712a23f37c71cb89606a3`  
		Last Modified: Tue, 21 Dec 2021 03:34:07 GMT  
		Size: 10.3 MB (10320854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44222df82131b4d925c2f594e50c018b1fb6d67154b22de79d99eb4cd4a356c9`  
		Last Modified: Tue, 21 Dec 2021 03:36:17 GMT  
		Size: 52.8 MB (52817006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71e08edf3534b3a52b84e74759377bd253863a9cf43fa9dde36a31debd1990a`  
		Last Modified: Tue, 21 Dec 2021 03:42:27 GMT  
		Size: 223.0 MB (222972175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f52dbc3aff20cbcc5e371a33aaeebe4f5282272c41696c25fd3a9558e40e8bdf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303824498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283f82ff8f1a5ace3b8332888093b31a9576a9ea617a5606734059ceb49c95fa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:43:37 GMT
ADD file:fef3d16fc616585749eed591688807817c9f37f8c4f5b1f6fa331e8abb0b60b4 in / 
# Tue, 21 Dec 2021 01:43:40 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:12:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:13:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f8ce27066e069d94a5210461101ff67f39042687acc056c6b8f43da616f6b2b6`  
		Last Modified: Tue, 21 Dec 2021 01:49:35 GMT  
		Size: 54.1 MB (54090241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430eb3656cbd2e26f5882863248d1d470bb0f7b5019c000a75107367ebed5950`  
		Last Modified: Tue, 21 Dec 2021 02:19:12 GMT  
		Size: 5.3 MB (5256801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf00a1bce82700c975dc02484e483d113ef14013f902525638bf031c142cae0f`  
		Last Modified: Tue, 21 Dec 2021 02:19:12 GMT  
		Size: 10.8 MB (10797100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8554ce38b98712645df3c9898c381e1ac40835d50f37d436f4f4ad142ee4a654`  
		Last Modified: Tue, 21 Dec 2021 02:19:27 GMT  
		Size: 56.1 MB (56095731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce19a71363fa0f6f8541b41544c92912e5383b918fcb5b75df188ab1301a9fe5`  
		Last Modified: Tue, 21 Dec 2021 02:20:00 GMT  
		Size: 177.6 MB (177584625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

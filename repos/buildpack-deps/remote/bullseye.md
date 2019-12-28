## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:6e59d571cf88895c0b6083ac351b2aa7e5da01bda72945a0f6c7d5975cd25126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:598d278fe934f2a2bc39303ccf11bd2802bd7d8a08ada882789918de61131ee3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.6 MB (320632557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc38c0fcecf18b798106f419536524e372e9d415d599da5f6d9605f5242cfbb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:3f67740cbc1b7fefda4dc75bd2c0f0e76df9ae6b845f37b33cf8eea958403b6c in / 
# Sat, 28 Dec 2019 04:20:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:45:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:45:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:45:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:46:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f64e5c246a10532414f3b69dcf620cbf27337d8900089f4139ab3215186e02f`  
		Last Modified: Sat, 28 Dec 2019 04:25:14 GMT  
		Size: 51.4 MB (51358861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a40087c7676442e3d13e8a213aa17fb44a1cbab4d952197f09edac463f58edf`  
		Last Modified: Sat, 28 Dec 2019 05:00:44 GMT  
		Size: 7.9 MB (7919349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce8ee259aabe18e11221885897dc3fc3f8081c56a276bef858633277e6384ce`  
		Last Modified: Sat, 28 Dec 2019 05:00:44 GMT  
		Size: 10.2 MB (10182884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2980bfd4fdb4de40a047bf0530bc098ffcad6342b5a5b8ff22be79ed73e190a`  
		Last Modified: Sat, 28 Dec 2019 05:01:00 GMT  
		Size: 54.5 MB (54527287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16457550815f011f11ba128c3a2482ac28741a67b9e620d58a39426d478d451`  
		Last Modified: Sat, 28 Dec 2019 05:01:38 GMT  
		Size: 196.6 MB (196644176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:761de65bb9c105ddd71d31363532bd77f63e75c2198f83ef31c15c837cb870e1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291931673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e347f7fc1386a7046b53cac7c1a8983105ac77cdffa92a8f919095d3edd18cd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:48:50 GMT
ADD file:730d57bac91e32701978679d8ccfd9d70521397f6008ad321414c8d7ccefd937 in / 
# Sat, 28 Dec 2019 04:48:52 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:17:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:18:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:19:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:23:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a3c7b9678a433c6c2e10ed1e6dc96f81cfce99fe5f71bc8091965c137d50306d`  
		Last Modified: Sat, 28 Dec 2019 04:55:31 GMT  
		Size: 49.3 MB (49328079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775f3daa9663989f7914a385f5db11a26a307dab5f2cd76d08edc09eda570a44`  
		Last Modified: Sat, 28 Dec 2019 05:48:51 GMT  
		Size: 7.5 MB (7490102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebeaaf463e9882767863e9735347274863750c30cf65c8b1a8c8032c9e7b221`  
		Last Modified: Sat, 28 Dec 2019 05:48:52 GMT  
		Size: 9.9 MB (9877186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c828bf3de027e23d3ec285037b09ce1cd8652c1389dcdd865fb7522c5eeb0d`  
		Last Modified: Sat, 28 Dec 2019 05:49:16 GMT  
		Size: 52.1 MB (52145389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29a4655c0e24a53bb98a182c30ea4ad85feee816b67a3372d23cfd43cf3ac4a`  
		Last Modified: Sat, 28 Dec 2019 05:50:15 GMT  
		Size: 173.1 MB (173090917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b1b4879ec4b40c349833f3af01cb02e25e1c66c9ed0dc3662ffa7fbdf2d5a4a0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286390249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d785b671bf04703edca144eb64a20bd8129716b0ee435927b4967792dca5b4a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:57:57 GMT
ADD file:ff4aac151f354dcf2159847b433d9631b254a18c30cb55390fe848c64ae989df in / 
# Sat, 28 Dec 2019 04:58:00 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:37:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:38:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:39:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:42:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aa5ecd1f9158499f6ccdafbcc35abc9cff760ff71453cf163442fd894809336a`  
		Last Modified: Sat, 28 Dec 2019 05:06:38 GMT  
		Size: 47.1 MB (47075322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29564c870b9ddbfdb14447cd65ce79e4a7d90599b8451e5102fbf34b5bbe13e`  
		Last Modified: Sat, 28 Dec 2019 07:05:38 GMT  
		Size: 7.2 MB (7232551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de02b8a9c8996450e899ce5c5cf642268569a23eacfaf79480c1237a0967c76`  
		Last Modified: Sat, 28 Dec 2019 07:05:39 GMT  
		Size: 9.5 MB (9528969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b277e09389ce7806d68c46268527690026db9abd4fccf9c2fbe89f2fc56f6d7`  
		Last Modified: Sat, 28 Dec 2019 07:06:03 GMT  
		Size: 50.0 MB (50011841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd9796f8e657ffb567c7964bc4abfb35896dbec9eb475f815b44403902a233c`  
		Last Modified: Sat, 28 Dec 2019 07:06:53 GMT  
		Size: 172.5 MB (172541566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:99b3d9edb856b20bc2151aff2382fe694b21a9c4926481ad9ff4d073396aca48
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 MB (312537896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117070203c913740c24bb1ff4205a40abb3ca2d22275fba3fc3ca210d5094d48`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:59 GMT
ADD file:d8dee71c9b462c830ef0fea7e4ea281b8c8ee4f3a1e9e3252fae2401bc715637 in / 
# Sat, 28 Dec 2019 04:40:01 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:58:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:58:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:59:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:04:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9ddc6b7ca7922f46e5d77becb1dd9bdbfabf5d66b99008799facc91235201022`  
		Last Modified: Sat, 28 Dec 2019 04:46:03 GMT  
		Size: 50.3 MB (50319316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f147f3a8b319f949fb21cc8ef219b5e607881821f497aad9dea6fe7a9a88977e`  
		Last Modified: Sat, 28 Dec 2019 06:19:47 GMT  
		Size: 7.8 MB (7793115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15fd445a2b52a4806ef65aaa42f0fe599f857e4b40277d4740433c4c0e2380f`  
		Last Modified: Sat, 28 Dec 2019 06:19:47 GMT  
		Size: 10.2 MB (10191212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aedd3ed7054c5c8146cd072344a2a3541373199331f8fff581744540645125`  
		Last Modified: Sat, 28 Dec 2019 06:20:10 GMT  
		Size: 54.7 MB (54708406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2ea9919254a017935d7a735c12c2e0d3111939a2e6e67769b97b3be175d8bb`  
		Last Modified: Sat, 28 Dec 2019 06:21:08 GMT  
		Size: 189.5 MB (189525847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:102d9c00897ac5dcee552da516be11ad1b37f2839b973a002b1490e8488917ea
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330259795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed53a5d46defb0fd3510a4abfeea8eea1b9782c1d7e682e535698999154cba2c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:38:52 GMT
ADD file:de81f6da93dbb580dd4c6a23ebd6cef637ab58e6f566e5ff7a217d4def3ed529 in / 
# Sat, 28 Dec 2019 04:38:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:18:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:18:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:19:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:20:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e3ee43b8971d572beb3640b791c4bba0d66137db2252115ebd9b2bb3ab7704d1`  
		Last Modified: Sat, 28 Dec 2019 04:43:38 GMT  
		Size: 52.5 MB (52480376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372a64d1cd36c22d0befce3fc6f8cba8fa5023d7bd33fc658de98186e128919f`  
		Last Modified: Sat, 28 Dec 2019 05:41:00 GMT  
		Size: 8.1 MB (8091626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ac8412cc2ead4ec139c961dbfca9f633b422edecc1798b4b7057866f1cac71`  
		Last Modified: Sat, 28 Dec 2019 05:41:00 GMT  
		Size: 10.5 MB (10533850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce9c776c7ea7ab8df81aec52dbda475b2976bb40c49fae2accf334b1755c319`  
		Last Modified: Sat, 28 Dec 2019 05:41:33 GMT  
		Size: 56.3 MB (56310932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b389fc51d762b7ec4681acbb61f299e616afbd5502170f3fd5aa6169f4963e`  
		Last Modified: Sat, 28 Dec 2019 05:42:30 GMT  
		Size: 202.8 MB (202843011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9e539a04441fd0d1ca12f5ed663342f297c747abdb55c188744512180b381e60
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339942320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e90ba90892bc06ca0f2eabefea6b52cf7f005191192e9d3214eebd66f18e72`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:19:20 GMT
ADD file:b4f9e68f81c696fdc52ed16b3080552fa23e19fe66b8de9cb3ade042aac7115d in / 
# Sat, 28 Dec 2019 04:19:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:34:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:35:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:39:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:49:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0127e22d45eca52f3501e5b68ef14e0d3a7c0c031138b56d8f69924604af15b`  
		Last Modified: Sat, 28 Dec 2019 04:26:06 GMT  
		Size: 55.2 MB (55181582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8e72dbc0de56d75beeba9cd6882f85d47bb6b3077837bbff7414b67963edac`  
		Last Modified: Sat, 28 Dec 2019 07:19:58 GMT  
		Size: 8.4 MB (8353078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a10090632680817f5ee840a8157c3a412aa82b9db7e41f83c953b68f06651da`  
		Last Modified: Sat, 28 Dec 2019 07:19:58 GMT  
		Size: 10.9 MB (10945667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de2512f180efbf390aa5c580b30ec1231a51a986bb86bc7b1ce395d59903709`  
		Last Modified: Sat, 28 Dec 2019 07:20:29 GMT  
		Size: 59.8 MB (59784518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08443b658fd0160dff8ef7054a3cf556f3bf315500e7f21269b10533e40f137`  
		Last Modified: Sat, 28 Dec 2019 07:21:33 GMT  
		Size: 205.7 MB (205677475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d5d8294d02b039c80e8ab306879ed854f19336a47492bee2e0cd912ab4b77016
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301158352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b9fe0f712754e1db52c5ae4bf4f6510fc07931c43087d3ca1f4da1da7b8ef`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:30 GMT
ADD file:ef81707ff6f9411444d40f7819b6103572f1c71599afd4c687f5262af6d30f7d in / 
# Sat, 28 Dec 2019 04:41:30 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:42:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:42:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:42:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:44:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6967537f6d685c8e7bce246638525934908340998b95e5baed55bd5e9805611f`  
		Last Modified: Sat, 28 Dec 2019 04:44:31 GMT  
		Size: 50.0 MB (50017657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5626baeec9661579acdaed4ea6587cae4c16df097bc274ac329b6422d405ed9d`  
		Last Modified: Sat, 28 Dec 2019 05:52:41 GMT  
		Size: 7.6 MB (7590139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc69b710fc3f7e4f96daf59aa3255a7f810b677a869eedde6dc313330d76855e`  
		Last Modified: Sat, 28 Dec 2019 05:52:41 GMT  
		Size: 10.1 MB (10068811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb0c2c2d0d3cba15da991cde49579c040bc860db52909b9eb568b8bd8326b59`  
		Last Modified: Sat, 28 Dec 2019 05:52:54 GMT  
		Size: 53.8 MB (53769702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488766b9fee1e6250981b08a9d4986fee06f0c3b3d0ce687e48ea14f5de885ca`  
		Last Modified: Sat, 28 Dec 2019 05:53:19 GMT  
		Size: 179.7 MB (179712043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

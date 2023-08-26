## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:2fa9c6dfccd3fcefefcefdcb564d954bd6f85a5c502f92dfc369e7e40a1f7ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v5

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:45042aff5955087fb42e7926e5083662816560e204c9ff9af10b2ef86b86a776
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338618864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85d63d0113d6c9154f0b72cbd751734f94e9b70d06b00c11d2ae26092f46e40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:49:56 GMT
ADD file:d0da838ea8ff64a44e445dfb0001a4f6a2442085f0c0f942d0129b6f8054c7fa in / 
# Tue, 15 Aug 2023 23:49:56 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 01:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 01:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 02:00:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6d8f24fa9802404161e1d0ef0d1db6d5f4c20cb1f0e5884dd191e1d77f2373c`  
		Last Modified: Tue, 15 Aug 2023 23:54:43 GMT  
		Size: 47.4 MB (47395127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f867d323ed66972b6c492120ce3fa78d7e1d63e0279362a9a55229db8e7127`  
		Last Modified: Sat, 26 Aug 2023 02:00:38 GMT  
		Size: 20.3 MB (20250269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dfbc5e6b18e516ad072378c62dcfa42e9981f0925b16c44303b5c7f6424eca`  
		Last Modified: Sat, 26 Aug 2023 02:00:57 GMT  
		Size: 62.3 MB (62298697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76154f4b1c42c402e154efcbbb3b3594eaa5766589d7938250f678a4ccbc7bac`  
		Last Modified: Sat, 26 Aug 2023 02:01:34 GMT  
		Size: 208.7 MB (208674771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

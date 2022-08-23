## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:2fcc66a2660efc8c5a59614cde0ec59a70dabb1fa139030f7b1c6c68a96aa680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f865df23569ce8d81cc0f8ccd3e8b33d6ccc250ae34a26352f9161e0a074215a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66632140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b60780d8b2d8dd6b19f7afa2f9602864ccf2d9aa4ceb546623604bbbfb470b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:40 GMT
ADD file:6944d322f4c04bd2192061822af5cbec8ac0a6b424c461d66174d32aed604972 in / 
# Tue, 23 Aug 2022 00:20:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 03:55:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:55:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 23 Aug 2022 03:55:35 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 23 Aug 2022 03:55:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:55:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:1671565cc8df8c365c9b661d3fbc164e73d01f1b0430c6179588428f99a9da2e`  
		Last Modified: Tue, 23 Aug 2022 00:24:32 GMT  
		Size: 55.0 MB (55007555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da4c47f93a29385c466f0b8d06c34810d3c2fcf6a9fd424a039d0a9dd5ba91a`  
		Last Modified: Tue, 23 Aug 2022 03:57:33 GMT  
		Size: 11.3 MB (11310656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baadeaeeef9ec92fffddaf3f7991f97f2852ce3310c7e7115279778ce1b60c23`  
		Last Modified: Tue, 23 Aug 2022 03:57:32 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf6357f4e4c8211177f51c1526a9d04ce62e0dd0ed3eeb6745feda9f395463d`  
		Last Modified: Tue, 23 Aug 2022 03:57:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb160502891152d59ef71771495e79282a1d437e3a848021655e73ad1c5e6e48`  
		Last Modified: Tue, 23 Aug 2022 03:57:32 GMT  
		Size: 311.6 KB (311560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d754d80adef35e288ba8c81b0c1d43a68a7a9e9ea44bc4c28954e7006e4c2ec9`  
		Last Modified: Tue, 23 Aug 2022 03:57:44 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:802e6683b403f6aeb2a1bd1ab75212e78c52ebae4e071c9125687ed3e5eb45cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64903163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a3ce288e52475a713fb8a99a0a88e403efb387231eed91025cc1b2a6514760`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:16 GMT
ADD file:ce6014a27d18915dc6d46c5c1f0f894f0027d1e41fbebb1599c16371b7bab2f1 in / 
# Tue, 23 Aug 2022 01:52:18 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:40:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:40:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 23 Aug 2022 04:40:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 23 Aug 2022 04:41:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:41:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:cd84405c8b9e7a8c3d580c2148d25120dd697ea61e1cb55a62f33e67988b7043`  
		Last Modified: Tue, 23 Aug 2022 01:57:29 GMT  
		Size: 53.7 MB (53690830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41389fac6451c5edaa165e707618d0d38aa796dadadf0a53e91375599229d79a`  
		Last Modified: Tue, 23 Aug 2022 04:44:02 GMT  
		Size: 11.1 MB (11104809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa944d0b24a86d3c6783c35a3de9bdb224fd88d85acfc53a6877eba82f4a2233`  
		Last Modified: Tue, 23 Aug 2022 04:44:00 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8e7b2316fff41db365cf154e935a37e0add53d8709a798babc2d773d444306`  
		Last Modified: Tue, 23 Aug 2022 04:44:00 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008ab776fa76597c51b0bcab3ee104b6332e82ee9c3ed228fb27ca22597c479d`  
		Last Modified: Tue, 23 Aug 2022 04:44:01 GMT  
		Size: 105.2 KB (105172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe35c6d6cc8809c65371adcc3555b94ea4f0b56ea9a80a9cd2835bb87e676e4`  
		Last Modified: Tue, 23 Aug 2022 04:44:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ea7f71e76c866a072321510ae8b0772f34bdc263567ffb045e7e796b83b61361
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67619778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce67f44694c91a1a44b742c2dd0eee75b696025d887949e9473f0ed2cd74895`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:02:24 GMT
ADD file:4012c41187a03bdb3d37bec80f6255a1d46582e3ed145b4f313e42196529e524 in / 
# Tue, 23 Aug 2022 01:02:25 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:57:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:57:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 23 Aug 2022 11:57:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 23 Aug 2022 11:57:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:57:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:6f683b9c66ef80b527ee5e4cb11969c6e0c1400ab69a4f1279af90f5766d70c7`  
		Last Modified: Tue, 23 Aug 2022 01:07:53 GMT  
		Size: 56.0 MB (56012624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf83eb62a91d0fdc8157fc158481d63d03e60b89076fed1b987644451ca3f351`  
		Last Modified: Tue, 23 Aug 2022 11:59:30 GMT  
		Size: 11.5 MB (11499703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e223068094fb93335f3b53abd57cd15a642aa20735bdbe41c7e021b879bacd6`  
		Last Modified: Tue, 23 Aug 2022 11:59:28 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3054dfd7661eac1ec6f11e8411e6a0717cb7e396d77bc058f9e33e24b8014c8f`  
		Last Modified: Tue, 23 Aug 2022 11:59:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169cf368c015fb808d904a5b66c3b5eb9e45984e12e7805303b69f918ad0b0a8`  
		Last Modified: Tue, 23 Aug 2022 11:59:28 GMT  
		Size: 105.1 KB (105105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc4e378164fccd6750f08d25e29df073dd44f25add43c2954e435e1b6b2585`  
		Last Modified: Tue, 23 Aug 2022 11:59:44 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

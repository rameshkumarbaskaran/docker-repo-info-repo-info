## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:b89726741f675cd93d2789a4f5cabce56903d6dd10ce116f0cbccd0171846ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b89bbc82aa854d867b19d72bcb09ba4855ea65605d381abeabddc80d744eede1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65027361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3753a614b5775fd3753abbd40481e95b0d863c35129f0840acdf5651d70d7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:55:59 GMT
ADD file:3b3b943815afcac58f0e8a49af9b3ab289e32cdd69d4c6bb0c64665439c8619d in / 
# Tue, 13 Sep 2022 00:56:00 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:43:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:43:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 13 Sep 2022 13:43:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 13 Sep 2022 13:43:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:43:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:97357bf36a88b062ffcf42d1d32358484d7f104afddf68a27fc780d5e4b35747`  
		Last Modified: Tue, 13 Sep 2022 00:59:24 GMT  
		Size: 53.0 MB (52983612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6958830299094274cd28a7633f5b862d12889aa0fdf900cd74f970c82736b410`  
		Last Modified: Tue, 13 Sep 2022 13:45:34 GMT  
		Size: 11.8 MB (11755685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918d7577da10e87eee101d6e704573438525d726132c9be5976e03658e8ae1ea`  
		Last Modified: Tue, 13 Sep 2022 13:45:33 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94dd251b74215c202680e3023fcc2a87093174b006bd659050c2703b317e00fe`  
		Last Modified: Tue, 13 Sep 2022 13:45:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d642afe5dfbd462e3f3114441351f2fcddfb78c96985e0831ae4d3f988a6a0`  
		Last Modified: Tue, 13 Sep 2022 13:45:33 GMT  
		Size: 285.7 KB (285688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e9d728118393077e9531efbe480c737d41f31d7ea76b856c1e13e2edcabaa5`  
		Last Modified: Tue, 13 Sep 2022 13:45:47 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9fb15b3ee57c8ecf0c6fad7fbc5ce41d2124d2363d6d2532d4c74192ed6f5e4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64610704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a146677dea1903a8763fe0202bdc02ac58275e1db107f7d1a45d48d360d56b1a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:00 GMT
ADD file:269c8bec4871d84b9133706a2f391209619d53c0bfa56121c740757cf5798fcb in / 
# Tue, 04 Oct 2022 23:44:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:59:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:59:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 05 Oct 2022 03:59:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 05 Oct 2022 03:59:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:59:30 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:2debf9e7f23054c81a936da9b01c5db9f72a55d4810f7bf0e5641bd1748d90b7`  
		Last Modified: Tue, 04 Oct 2022 23:49:11 GMT  
		Size: 53.0 MB (52980389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0ef51f5528c6564ff374a45d9cb4c4c6eaf535c3565cbb4ba763bc55b22343`  
		Last Modified: Wed, 05 Oct 2022 04:03:24 GMT  
		Size: 11.5 MB (11531064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469c79e490be5fc87427c713b2cff0a58e2d249f09613ea11f6d6a02ed9e62f7`  
		Last Modified: Wed, 05 Oct 2022 04:03:22 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52a22ac0a033238596c38df2f9af0747aa62ed9470c2a82f61ed8978d6ccc5f`  
		Last Modified: Wed, 05 Oct 2022 04:03:23 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bc59e065b02635051c28a8a2b68751fbdc3486f83ce39b848da35674d67b13`  
		Last Modified: Wed, 05 Oct 2022 04:03:23 GMT  
		Size: 96.9 KB (96904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86addfd21f29a2b3cc2f2d4caa2e71233a7f3263674e19b65321fcf5e03cc560`  
		Last Modified: Wed, 05 Oct 2022 04:03:36 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a0419b3921c4500ce8017f99b534dd4c66e6641fdd63cf8d17d36a607b17dead
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66022979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee04776b466810c25260cd640d93dd96840d94e5bf91857e004aa6b5f454b5c6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:38:57 GMT
ADD file:2a0c743e373aeed6462c2f3ae8a138fb0e240e935ad7ca5bf008aa3efd3673a0 in / 
# Tue, 04 Oct 2022 23:38:58 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:15:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:15:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 05 Oct 2022 02:15:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 05 Oct 2022 02:15:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:15:50 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:c68776dad61a299b8e65d1a6a02e376b8ed2e9b241bd753bf6c35d497055ecdf`  
		Last Modified: Tue, 04 Oct 2022 23:44:23 GMT  
		Size: 53.9 MB (53932827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b23a7101cec8d64ddc2337801957f17d5366b0725dfb359c4a75a69d6a5e59b`  
		Last Modified: Wed, 05 Oct 2022 02:17:53 GMT  
		Size: 12.0 MB (11990988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bc6ea3e1edb50b087a2d132755dd424f332df905fd3ca53fc106283fa89192`  
		Last Modified: Wed, 05 Oct 2022 02:17:51 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f7492185dc14c52e2b31a59607eac615a02bb456adcdd05c611ea2b460da27`  
		Last Modified: Wed, 05 Oct 2022 02:17:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156209dfa890bcc23c8e351f1f08baad61399ccb713ea04a5f81e3d9a8d3760a`  
		Last Modified: Wed, 05 Oct 2022 02:17:51 GMT  
		Size: 96.8 KB (96816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e038e92cc95c6ee9d08edbfccb0fd01d6cc3153d445b6ea5717491f57216b426`  
		Last Modified: Wed, 05 Oct 2022 02:18:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

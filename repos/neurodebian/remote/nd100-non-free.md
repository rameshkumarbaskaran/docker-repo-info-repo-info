## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:548b1ecd5faf1a7c9885a5c49cbc1f8fb6e6c707c47cf570a5c3d9fb4860880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d47e4100b13330b3eb27dc09382a1f68651cfc1ca2295c90c557208f9b01b0d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61309710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fbbf2da0542273de38c4547374cea0eaf41e6780f0689b79d7f6a46361aea5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:17 GMT
ADD file:46b31c893ada083f38702e21d80e5ea4b674cbc78bddd3d80020d7b8e8beb467 in / 
# Thu, 27 Jul 2023 23:25:18 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:26:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:26:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 02:26:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 02:26:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:27:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:9918064ebccea7fc961fe71dad46105b217763b4b1b3a9dfa7bee2ab29d2039b`  
		Last Modified: Thu, 27 Jul 2023 23:30:27 GMT  
		Size: 50.5 MB (50497996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df2173112ea07bd3af648a97be52b1099564a063941b34513234f077b78a178`  
		Last Modified: Fri, 28 Jul 2023 02:28:24 GMT  
		Size: 10.5 MB (10504692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecfc80bfc24d45f36657dc8efa932fe232fe84cd2c19317c9f8b42816faa23d`  
		Last Modified: Fri, 28 Jul 2023 02:28:23 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28035d61fe1bc4cc48da6e2b52ac73d4212a8ae6f36da39d87db4e7c5f9642a1`  
		Last Modified: Fri, 28 Jul 2023 02:28:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c5ee1fb9c82ac17c7821bf241821aedef97d44712eed7e0f522eb7954dab71`  
		Last Modified: Fri, 28 Jul 2023 02:28:23 GMT  
		Size: 304.7 KB (304652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4482150fcd5aa1d2ce27f4c365dc8c3de72e12f363bddfdf8130fce44dd5445`  
		Last Modified: Fri, 28 Jul 2023 02:28:32 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:402c6e0b4b93c7ce62e265ddbc80129342bb26a6a786597e2467d778ced18c93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60108582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8767702d60bba1170f1b735fd77cd44587859e247a5d77d65c7f18edb770e3e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:21 GMT
ADD file:7472c3a6e583fa549b0fdf510b32407a4ed40f255a30199cdd2c5fb367794d45 in / 
# Thu, 27 Jul 2023 23:43:21 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:07:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:07:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 14:07:21 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 14:07:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:07:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:89b61c8397133d3e1d24ef0453eec8370033046cc0fc0854b595eb1e3c6d73e7`  
		Last Modified: Thu, 27 Jul 2023 23:47:32 GMT  
		Size: 49.3 MB (49290895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80b36e72ea055ad83c83d618f55c7a3780e7a661d043514faf24738866b5cb7`  
		Last Modified: Fri, 28 Jul 2023 14:08:40 GMT  
		Size: 10.5 MB (10510681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29608a7a518068572d52524a7dae9061aa62c329bf1f3b091e22fd8b4eb07d89`  
		Last Modified: Fri, 28 Jul 2023 14:08:38 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576e72eb1ee42357aa3cc3917036a1fd8ac5f5002f7c535627589af959ac9d56`  
		Last Modified: Fri, 28 Jul 2023 14:08:39 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479283e8e881533aabf28d2d765da2fa0bcd8108f205cc3127fbe343b9662ec6`  
		Last Modified: Fri, 28 Jul 2023 14:08:39 GMT  
		Size: 304.6 KB (304639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bee6b22571a922e0c984926869c9661a8818399f7c4fad08ef700f3a2d56388`  
		Last Modified: Fri, 28 Jul 2023 14:08:47 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:154a6e8bf757c2a56521e555e827e8fae62e40bf29faf9ddb9394675c5121665
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62430792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075469979bba1f5bb176d7fd582c03fd8e81905fe4f61b9db283c17dd2a6825e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:29 GMT
ADD file:a4caa39d69b463e1f2628cb32f33763655fd873129cf98dd26c431183c53b6d6 in / 
# Thu, 27 Jul 2023 23:39:29 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4b5eb5e3691ae17e5aaa83c175523a7a17d58c9c61698ed6bba826d9acc809ec`  
		Last Modified: Thu, 27 Jul 2023 23:44:34 GMT  
		Size: 51.3 MB (51255427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a9546696cfc41507830169b067ee13ec325fe6700c48dd0cbc5305fc2e7ca5`  
		Last Modified: Fri, 28 Jul 2023 00:27:38 GMT  
		Size: 10.9 MB (10868456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248c8a0326f730ee26d03c9b5aa23067f9422968d77aba57711075b6255677b0`  
		Last Modified: Fri, 28 Jul 2023 00:27:36 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b42292c3c0cc2f12375716e1845d09e94189548afab4c0355ab61f7475c862`  
		Last Modified: Fri, 28 Jul 2023 00:27:36 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50994e1702ad118d42ed1c2ed85ff7a2cf5a158ca8cbd886ee714d44efa66a7`  
		Last Modified: Fri, 28 Jul 2023 00:27:37 GMT  
		Size: 304.5 KB (304539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c3b2bb602d2b7f4c6da3126c6bbbf3940a26e98c1aeb3045a3fb2f218da43d`  
		Last Modified: Fri, 28 Jul 2023 00:27:47 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

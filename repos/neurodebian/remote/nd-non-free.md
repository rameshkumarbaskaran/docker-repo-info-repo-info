## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:e8f70d73342ef5cbcd4b4c062f13d74a07595cebdfa3e1b6b8326e99b50b6c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ba6a6e0b675e70c83bcdbef7cfadbae8facd26202533b736e1878bc9dfc67c76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62440838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051a7cb71c2fd3a5721750720547aba168855c33a10cd2526bbf680a4b83e610`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:41 GMT
ADD file:635f36e1a46e6c28b2a6ab0637cca9e47837c3547b17916d1dbb2595fbeb0821 in / 
# Tue, 25 Oct 2022 01:44:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:14:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:14:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 25 Oct 2022 04:14:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 25 Oct 2022 04:14:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:14:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d90f8b044e56f2589b41d1fe9b249b85bde027855731c6f512f0f9401c99e68d`  
		Last Modified: Tue, 25 Oct 2022 01:49:42 GMT  
		Size: 50.6 MB (50641226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940e2a7702be736f2aad5111fec997e5d6fbda3112a52885fe56600b9f20506f`  
		Last Modified: Tue, 25 Oct 2022 04:17:04 GMT  
		Size: 11.5 MB (11517246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90729320165f6559c49f8bc4ce3506f2b3589d4e506fa960c53d2a9f6d25e086`  
		Last Modified: Tue, 25 Oct 2022 04:17:02 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcff98e07edcf843907a8559602876590355c68e7064ab6055f44485f8ddec9c`  
		Last Modified: Tue, 25 Oct 2022 04:17:02 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2861bf0d5d9e8ef934651360c457bda665e3726d7085e6a97345af3a59b1cac2`  
		Last Modified: Tue, 25 Oct 2022 04:17:03 GMT  
		Size: 280.0 KB (279961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9278afeb2bdd42daf971104bd30c60e87c36f2c2150f2839735e56cdb9539b`  
		Last Modified: Tue, 25 Oct 2022 04:17:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:dc87eb27afe1d66aedb864fb02d78350244d2f91adddd2e3691834c63b4bf334
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62400629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6cf06bddb88d8f41b1687c80ffe1d045f85bc2f40e3bef603fab582a78984e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:29 GMT
ADD file:6a2d69a5a731490271c915d99634a89755f7236ef56712924ea061730d8552c4 in / 
# Tue, 25 Oct 2022 05:46:30 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 00:34:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:34:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 26 Oct 2022 00:34:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 26 Oct 2022 00:34:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:34:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:63a396bb133ce57141398b6c6d776ce17e3e973085b5a1b746d76407240a376a`  
		Last Modified: Tue, 25 Oct 2022 05:50:38 GMT  
		Size: 50.6 MB (50643735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e025aa9977352d79bce97076b455544eb3f81d16ba3cc9a573b3f677be5f0d`  
		Last Modified: Wed, 26 Oct 2022 00:37:43 GMT  
		Size: 11.5 MB (11473994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c58a8d469f3b8074c076ea5d8d4552b2e4702948ac0f974cbfc461e52049389`  
		Last Modified: Wed, 26 Oct 2022 00:37:42 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3691d8dc109f9468f9244123c733fc73ba87491982503c07525d9860441869`  
		Last Modified: Wed, 26 Oct 2022 00:37:42 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49388cd3409ebb5983feb01a2c466ca600c3064f44c9b5ddcd0421558098997`  
		Last Modified: Wed, 26 Oct 2022 00:37:42 GMT  
		Size: 280.5 KB (280498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24230c4d1ce07c8d19f1a39f36e953a2f362072b8fe5c5f2eb68152f84c08d78`  
		Last Modified: Wed, 26 Oct 2022 00:37:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:0365060b6fc7f32de44aa5828dc5dcc6c6c163c96ef838ee165c4bd134c7dd30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63357156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0891dc71cdf2d231bbc525635104af99a5f9bf7e4f9990ee1ee70e31f7399389`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:30 GMT
ADD file:6c7cf2ddf77e13ddd1b27b3e2895b29bf27b8fd6d38de6f5fa7330138f69523b in / 
# Tue, 15 Nov 2022 01:42:31 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 09:05:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 09:05:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 15 Nov 2022 09:05:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 15 Nov 2022 09:05:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 09:05:39 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:3d85d48acbb26d22f92c31ab4d483ab5c9fc0a7db5f67806b2c05a4460060ee4`  
		Last Modified: Tue, 15 Nov 2022 01:48:49 GMT  
		Size: 51.4 MB (51364090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3887b92b4ad68d9d5e5503e23593e9661fefd8731a408ad6ec041d8f9bdc40a3`  
		Last Modified: Tue, 15 Nov 2022 09:07:30 GMT  
		Size: 11.9 MB (11898906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cb0bbf6323ed1dcfff60e3bc5cdc9d1de705bc4041fb7e52e8a8db8adde63c`  
		Last Modified: Tue, 15 Nov 2022 09:07:29 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0b9a876957a6900b02d81753d0dd82fa9271900c22b0105866cc6923451886`  
		Last Modified: Tue, 15 Nov 2022 09:07:29 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6261ff7924cf90da06060a1f91e9bf598d7e2467fcffab73679ad426349f8aec`  
		Last Modified: Tue, 15 Nov 2022 09:07:29 GMT  
		Size: 91.8 KB (91785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe6ea623698f0472e209d44a0c8ad8a1272195f8dc607c967f26087e557f1f8`  
		Last Modified: Tue, 15 Nov 2022 09:07:40 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

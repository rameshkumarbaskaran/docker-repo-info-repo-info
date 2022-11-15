## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:ad96cb767bd6c28d7799a0228260bb08cdd18ffa1bbd8bd3b6c1cb9c40436790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:9a5b5ea5402fdca8b78b46425b150a95aa35933f63491c1a699b52b7483e0340
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66672846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99de7e2645a583e01a0e4c80044fc9658356c94b66baaafa56cb0dafcc976cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:13:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:13:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 25 Oct 2022 04:13:28 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 25 Oct 2022 04:13:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:13:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed2c6a9f12c16bef8e9d62b2f3919ac5cfe7e4dcdd2a410c5d1512470357546`  
		Last Modified: Tue, 25 Oct 2022 04:16:19 GMT  
		Size: 11.3 MB (11311651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32085ba5b820cb53d95f1c5a64d3d44cbe004ad8a7056e472f598b69831a4ec4`  
		Last Modified: Tue, 25 Oct 2022 04:16:18 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f70df6cc7ad4d9bfaee7502c94223d7de09183ffebe612ee0ab3d6d6889f94`  
		Last Modified: Tue, 25 Oct 2022 04:16:18 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd775cdf48cc3d8cdc1cf2b8241d7861683a6829d2a99a0ee00989807b1b2420`  
		Last Modified: Tue, 25 Oct 2022 04:16:18 GMT  
		Size: 312.5 KB (312491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc389d1eb8f25a823081706d235961f0be5e0e19cf04af6bfcf53463c3ee07`  
		Last Modified: Tue, 25 Oct 2022 04:16:30 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3019824cc40c877d6e6f042c84fe28e9372ffab0e77562e7ca98dd8f48a950a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a710f59571947d994c40cc232bff702000937bb8eb1d5c9eeb60a1b6a4974a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 00:33:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:33:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 26 Oct 2022 00:33:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 26 Oct 2022 00:33:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:33:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c78c4f74e114e23cc686025bf9609af276f4397ee1dc469af3d51677730c458`  
		Last Modified: Wed, 26 Oct 2022 00:36:59 GMT  
		Size: 11.3 MB (11313743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1f521d25f8bcbbd319d4e008feacfde0c32f6850950047e2848576c01779d3`  
		Last Modified: Wed, 26 Oct 2022 00:36:57 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcecc4862af153485c185300e85bd9bdb812b14ab1e7ebdbac1dde0cd09a5e8b`  
		Last Modified: Wed, 26 Oct 2022 00:36:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3fb85a7cb85d3bc5d33539c247070a55bd518bd25f3cb196fc93063ad70393`  
		Last Modified: Wed, 26 Oct 2022 00:36:58 GMT  
		Size: 312.4 KB (312409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520a7f45c68fd790e2db7da87b0489791788bf87e9c853fd8a5702146185a984`  
		Last Modified: Wed, 26 Oct 2022 00:37:10 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:79fe39ccfde513416bcd82cb75450161d0a80892ce0540bba7cb005efa965121
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67628208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32ad243dfb6ed086ce6c05ed9c290f93bd4951b39af8a689bea70a9058dbb3a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:11 GMT
ADD file:2962b9f6c2d1271d6b4d04e8eaf82fb990726e0593bbe685576851ef47447301 in / 
# Tue, 15 Nov 2022 01:41:11 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 09:04:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 09:04:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 15 Nov 2022 09:04:31 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 15 Nov 2022 09:04:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 09:04:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:9c6907f3cae53506b5149dd6542c3e51b750fdf5adbe19d7e949974888503c1e`  
		Last Modified: Tue, 15 Nov 2022 01:46:36 GMT  
		Size: 56.0 MB (56020725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02f4da13f5b313c8ccc51437a91b6daa971d5bf4c394df0eff89efb6005a03b`  
		Last Modified: Tue, 15 Nov 2022 09:06:45 GMT  
		Size: 11.5 MB (11499823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9291c78309912f933412d05c322ce5f5f79988bb29d3c3d6ccbac394b2a172`  
		Last Modified: Tue, 15 Nov 2022 09:06:44 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9748c95c991c7a56a69ddb537e1ac849f12dcc7b259a9f1203507cd770517cf7`  
		Last Modified: Tue, 15 Nov 2022 09:06:43 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b929d49a15db606a7cb66f8f346d8c890503b8d52ae93cf6aed44ada774cdac`  
		Last Modified: Tue, 15 Nov 2022 09:06:44 GMT  
		Size: 105.3 KB (105312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd2b9cfb07a4d4b91f14c4d62730efd59f23f6917165b2972560fdb01bcc552`  
		Last Modified: Tue, 15 Nov 2022 09:06:57 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

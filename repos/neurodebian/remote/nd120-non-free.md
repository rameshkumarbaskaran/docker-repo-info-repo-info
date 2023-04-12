## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:fdc47f0f54b0abbc3718f9df3e3317351e24b2390c01b460cfef928e500244f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c2ac47126d4eec7b0cf5c1b53060be889f4499257a184f64767686da33980eef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61294195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1e4b375db119eccd841104ceea26acc52b1cba1a58d33ec2312c74b71ab4a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:35 GMT
ADD file:1cb6c660a2e3ea14b2a11bb8b80f53920c3da423a0ad7004391bfab4db4d0177 in / 
# Wed, 12 Apr 2023 00:19:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:48:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:48:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 Apr 2023 08:48:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 Apr 2023 08:49:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:49:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:cc556c281183180fae02d57fa6fb60ed0a99d9040936278743dc4022bfb0c686`  
		Last Modified: Wed, 12 Apr 2023 00:22:48 GMT  
		Size: 49.3 MB (49292938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4683c8c9aa2ceafb2f2cbe3d59d5be8b06a55eb791c922753d76e68fa570b32`  
		Last Modified: Wed, 12 Apr 2023 08:50:25 GMT  
		Size: 11.7 MB (11716926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35662ef56b523fbfe6da412813b4361a7a392a6382e782a3a9713bd1fa5723a`  
		Last Modified: Wed, 12 Apr 2023 08:50:24 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774a45006a097d2ba07f389957e47ac004f97003bbb6d16ae27c5ab8faf24c90`  
		Last Modified: Wed, 12 Apr 2023 08:50:23 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee933995cf50aba77886e19e11e952adef6af3ec0692f358cd98db200b12ec6`  
		Last Modified: Wed, 12 Apr 2023 08:50:23 GMT  
		Size: 281.9 KB (281898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c845afe57396a2e7e6b476e7b0873e011803283727839f6a52026994dedc49`  
		Last Modified: Wed, 12 Apr 2023 08:50:32 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5f1eb0a0bc4526259d30403a58982981ae05f8110a4bad6079809eb913cab469
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61312686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd0a79322f3d6dbb79add8637c8958563d3042ae5d2cb88482a82a8ecfd2d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:27 GMT
ADD file:efed18ef2a003bff7e64e7049455216e51876402083581032c35085328e416f6 in / 
# Wed, 12 Apr 2023 00:39:28 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 04:37:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:38:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 Apr 2023 04:38:01 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 Apr 2023 04:38:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:38:06 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:b0f987ce91d920ae0a705ed6c9824f1bbbfa282defb8986614030eb8e2bc0b4e`  
		Last Modified: Wed, 12 Apr 2023 00:41:45 GMT  
		Size: 49.3 MB (49345365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc55b1647433c2ccb4259c92195c7472a7284df2716ece70eb0315be533b9235`  
		Last Modified: Wed, 12 Apr 2023 04:39:20 GMT  
		Size: 11.7 MB (11682554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841ca48051852864959dd87d2d7effdc406517cbe2ae3c860fa48ea5864a0231`  
		Last Modified: Wed, 12 Apr 2023 04:39:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d5506bfd0a1c3a44f6c6c1efb24c5ef1af21706f73709f1ff2ed04efd5d360`  
		Last Modified: Wed, 12 Apr 2023 04:39:19 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280d60a70e4f94f3652486ddda8a1f4b1ec0a3853b1ec2b1a871c1e09691115e`  
		Last Modified: Wed, 12 Apr 2023 04:39:19 GMT  
		Size: 282.3 KB (282325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473ef883311a032a01d8229514ecd026cde2c5d41a57828912c20d279629e49f`  
		Last Modified: Wed, 12 Apr 2023 04:39:27 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e826bae61d01eaf63f7b8ff3da3e21ef833e8f96c12e29bb93096789e0f949fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62743614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38480811c25376914a7ef027cdfdf98e96762fb28f55b266d97025f5b6d54859`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:30 GMT
ADD file:7718865253a3489583d40f8c7a7beede0c20cebbab68bb3e97ad2e84082afcb7 in / 
# Wed, 12 Apr 2023 00:38:30 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:06:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:06:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 Apr 2023 05:06:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 Apr 2023 05:06:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:06:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:a4ce9e81f634822e5166ef3eef875a4140795ac18afe0391433d72c7865bf67b`  
		Last Modified: Wed, 12 Apr 2023 00:41:43 GMT  
		Size: 50.3 MB (50317977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84da2d04e2213936972561f29d3c5c24b05c603098f55c356f500ff85c6ff72a`  
		Last Modified: Wed, 12 Apr 2023 05:08:06 GMT  
		Size: 12.1 MB (12141193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735656053c05260073c2e268f1a3dd6948d897c43a71237e34eead3d43ac135f`  
		Last Modified: Wed, 12 Apr 2023 05:08:04 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d0ea8ef8f29386c675e5ef1cd64a54b382852d99f3e19d57cce6e04a0eec72`  
		Last Modified: Wed, 12 Apr 2023 05:08:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46a95e50e161e774a1c7d8aba905988057369c3116e44a29c202e91dd4697ed`  
		Last Modified: Wed, 12 Apr 2023 05:08:05 GMT  
		Size: 282.0 KB (282004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9f44dafd7d26e7ad2ddbad38c4db517e396ec88a0b5464044750525196d146`  
		Last Modified: Wed, 12 Apr 2023 05:08:14 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:5e21a5d696c2f24830b17ace2b22b92906df3aea7964965f403f18da363e180f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:4eb056af4f99e5cf0e4bb36fb041598be17061b2f5badeb04de061d8a0d08e4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a65bb4c1dbc843123f57fbb6c227e448bf36bc91540efe30571d2e7373cd032`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:54 GMT
ADD file:2f52161f98fff6a77f865fbd61397b76f3ad3391fa6d694a50a08ad43fd5c8c9 in / 
# Sat, 04 Feb 2023 06:51:54 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:48:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:48:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:48:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:48:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:48:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d42a0fb443d7323eac0a2073d5a229cf6871c4cbddd8e85bad4b0301b2dadedb`  
		Last Modified: Sat, 04 Feb 2023 06:56:36 GMT  
		Size: 50.4 MB (50449110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de2c6114af2471df54db6a6f68996f51e5c6725dc13cd50218152e6b734fc9d`  
		Last Modified: Sat, 04 Feb 2023 09:50:29 GMT  
		Size: 10.5 MB (10504469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ad61b917527e7bc9d3081b7d815d4312d7cd7b898cbb8a8a454c994afa032c`  
		Last Modified: Sat, 04 Feb 2023 09:50:28 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894fb81d9c36b05fd865441fb72d450686bcabdd720cb053a0e26bfc4d172e9b`  
		Last Modified: Sat, 04 Feb 2023 09:50:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c75efa50c7d459603199041a9d1229bda46816a8c61d7e37754c14bf032d41`  
		Last Modified: Sat, 04 Feb 2023 09:50:28 GMT  
		Size: 304.4 KB (304369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d9bd0a1405d1b177e4fbba26da0f9cdde3947700b1810984c35e9b994dd984`  
		Last Modified: Sat, 04 Feb 2023 09:50:37 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9dbc4060d63354fc168ef4b4ce8d6572031d397dbd61b0240a71078697e7bc8d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60056397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e52ff1f01210e669f87eece484b274a1c9ed6dfe5aff7b6a0451113022b17b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:45 GMT
ADD file:0241487c3fb43506be1511724644c00339c32361e6b4c21a224d7190e4e1063b in / 
# Sat, 04 Feb 2023 06:17:46 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:48:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:48:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:48:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:48:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8e0a5a2afd38370f358c0a7154362a8d17faf709c206b40b1553a077f810c3b3`  
		Last Modified: Sat, 04 Feb 2023 06:21:43 GMT  
		Size: 49.2 MB (49239373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda0b3f7673107c2204b83097e20a33728ef30d2e731e41727e0915eb8eb7c9`  
		Last Modified: Sat, 04 Feb 2023 08:50:17 GMT  
		Size: 10.5 MB (10510366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0e7e8e9562ff77a3d9a1bc9b20bcaaffb5ab25e375ce28460ba3a4018788fb`  
		Last Modified: Sat, 04 Feb 2023 08:50:16 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c8ab4aac39ddf7a0f79a2cc135d4c299bb4a80b3282626e03ba7581e2ec733`  
		Last Modified: Sat, 04 Feb 2023 08:50:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fc1d1a5e62555249343f0f0e4c5483c04f9b57bd28318895d6a9f14050a7e6`  
		Last Modified: Sat, 04 Feb 2023 08:50:17 GMT  
		Size: 304.3 KB (304289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb106862c94d1d9cf42027a0b8de792e548f97d4bf206491e472fc6159c7e0e`  
		Last Modified: Sat, 04 Feb 2023 08:50:25 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6c16c1e38965d822f79bb63927ab57cf8eb2cbb537d907e84a89bbf24e1af8a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61991341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2a0b1b021d82a33722be844bc6183dce33deab6f76ce2360e0f03a1e01fc2b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:33 GMT
ADD file:23aa007679cd84321e9278c9f6261256b1734b2e27727d84ecd3e3418e6b8dff in / 
# Sat, 04 Feb 2023 07:49:34 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:17:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:17:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:17:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:17:20 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:18e547e593209084f2c8150bc5b70229a02a902a855c32fb560765e6a40891a2`  
		Last Modified: Sat, 04 Feb 2023 07:55:26 GMT  
		Size: 51.2 MB (51207661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b5157c7f1fe625aba139644ccc5d778bd2612aa09dbb07647cc8fb1645b7e2`  
		Last Modified: Sat, 04 Feb 2023 10:19:24 GMT  
		Size: 10.7 MB (10672599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c575c89dc25a96f058de33b540b31bcbcd0806e12baaa42524df5b83b25bb00`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4549d3ced6edebcf3acdd958851b03298abe2d86782697f48fadf3ab90bd27f0`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4007a5e6d2ddd44a5c7d604ca425380f910138e3f9ccb53b3bb41818c2b57068`  
		Last Modified: Sat, 04 Feb 2023 10:19:22 GMT  
		Size: 108.7 KB (108736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c5f1cd364eb20620bd7ecfd8199b217eadb409140aa90a44a7e992a2c3e2c4`  
		Last Modified: Sat, 04 Feb 2023 10:19:33 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

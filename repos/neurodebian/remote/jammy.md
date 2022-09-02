## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:16e6857551efa7fdf4c0fbf96f9c64476ff40b5268510d491a9b6aeb425249c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:d200e4aa5aa7743c775f2217a6542dbdf56742b2658e925370c5af69f46ebeca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34451368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1577f99f457d98445f6d61331268f86d4ac1ea2fc0fa9bf817cdde80fd409b82`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:01:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:01:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 02 Sep 2022 04:01:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 02 Sep 2022 04:01:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63317807c3bb0eef62cf42889b55a4632c1c74c0c72311f638a215ad205e8aec`  
		Last Modified: Fri, 02 Sep 2022 04:03:42 GMT  
		Size: 3.8 MB (3765487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d3b8526af090418d4635ff5db733a63b3fd98439260abd29b2c058cd757563`  
		Last Modified: Fri, 02 Sep 2022 04:03:41 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2406ef15cac6acd7155bd1a4a5eb46a43a3ce39a37831f00b529b8dd00da262`  
		Last Modified: Fri, 02 Sep 2022 04:03:41 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80e1b5b1d62cb7e96a17943fffad8a08bd72c727262d1a6618807ccb55736e8`  
		Last Modified: Fri, 02 Sep 2022 04:03:41 GMT  
		Size: 257.2 KB (257156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f40e65919dbaa2ba02acbb59b15e9b2f653d84606ac63cbd75b0cd84a6cb9754
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32091124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af1b2e991dc0fe6b1e0d827af00813e4411e222309b3fccccd19720d41932e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:51 GMT
ADD file:550e7da19f5f7cef52c6ea160a33daa482f44df086ddecffca8ec9be6385b848 in / 
# Fri, 02 Sep 2022 00:57:52 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 06:53:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:53:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 02 Sep 2022 06:53:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 02 Sep 2022 06:54:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:00f50047d6061c27e70588a5aab89adada756e87d782a6c6bd08b4139eb8ea10`  
		Last Modified: Fri, 02 Sep 2022 00:59:40 GMT  
		Size: 28.4 MB (28381340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42c01f7ed819d10d904acacb8b6235f7a5e666bd269ac4bd769bbabdd4231ea`  
		Last Modified: Fri, 02 Sep 2022 06:56:51 GMT  
		Size: 3.6 MB (3593242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fc7799e07f92e5b888755ed6df7b70de9d14d9ef6bf208b8ab1c0a4f50e24a`  
		Last Modified: Fri, 02 Sep 2022 06:56:50 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a6efce2a24263fe08b837ae964d0454e234129487bc3f013f28ca3630074f2`  
		Last Modified: Fri, 02 Sep 2022 06:56:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da2c1d32a498e1baa2202187d10408034982dcebdc8d7b176a55526129d1322`  
		Last Modified: Fri, 02 Sep 2022 06:56:50 GMT  
		Size: 114.6 KB (114551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

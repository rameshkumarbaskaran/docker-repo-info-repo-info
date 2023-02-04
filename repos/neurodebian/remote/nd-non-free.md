## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:d2853d988feabf7b38fafbed14a52b7cd5b4cf0a7185d34f416c17870c906c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d9da91cb3a9f07c8da425c7cda24799df726d94aa9eb22e4514172aa4c932ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60971700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4695c4028d7039b105e47bfa3cc8ce9dc902a609c9256f299e0ae37dbe6ea4c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:42 GMT
ADD file:a2e9c6618e31202c1b929d106d9d8f2e98a0d6a45ae13b56e9149536eee01769 in / 
# Sat, 04 Feb 2023 06:52:43 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:49:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 09:49:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 09:49:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:49:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:9338402809c6c0e98dbcb30453239ee887fa0b3378ee26565d576b66c08dfdea`  
		Last Modified: Sat, 04 Feb 2023 06:57:50 GMT  
		Size: 49.0 MB (49039305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dbacfb02619ae2748fd777216ca57eb38e5958cd05817de0397094f56ebb67`  
		Last Modified: Sat, 04 Feb 2023 09:51:24 GMT  
		Size: 11.6 MB (11649187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7de9daa7ecef35d8e3cf7220527b1f3229fdd919fd1a88eab5c9c39c14b885`  
		Last Modified: Sat, 04 Feb 2023 09:51:22 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e71ee3cf5d725362eefcdd5f053e155b961b5711ab2a14608a8d76ce970798`  
		Last Modified: Sat, 04 Feb 2023 09:51:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ebce64a4f447022558af3e39249236b0fa69567c48b15ecd943ba9e02d824b`  
		Last Modified: Sat, 04 Feb 2023 09:51:23 GMT  
		Size: 280.8 KB (280803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6174d2bb6eaf520ae243de994338976e5cf76d909ba7dbfe4b4c6593857ca1`  
		Last Modified: Sat, 04 Feb 2023 09:51:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0dfc6d72a79ebae3679ff6b7311d814ad650c536b908466f05bfedab09c0c447
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60961744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8d4407ad794329f99fbc45860becd38ed0ebb95f343004673e640cc94f0e34`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:18:18 GMT
ADD file:e0f39d8fee93f482160beca25b949b1de50ecc55ac86b1c276bed0b5c9955393 in / 
# Sat, 04 Feb 2023 06:18:19 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:49:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 08:49:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 08:49:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:49:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:541de84dec560e0a7dc13f9e5246f1a165b0955a6aefdc92d0bc46a50138a249`  
		Last Modified: Sat, 04 Feb 2023 06:22:53 GMT  
		Size: 49.1 MB (49064951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feef954a467cdbd9442f76eae26dcce65b43e942cf51fb0fc9932a2ce11a37a5`  
		Last Modified: Sat, 04 Feb 2023 08:51:11 GMT  
		Size: 11.6 MB (11613149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1fb0ddc7c21670259cb7fa6d33e4a66293440c6bb9ac9b12014f6ad578ba76`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b3ab955b5154981b3ebc74d79cacb2c050f8b3045d9e3b9bb5d5b3c6d69a3a`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e036d4fa82c2440e6b7a89404b4a9cdf679911cccfc91b67183e47fac4bfe42`  
		Last Modified: Sat, 04 Feb 2023 08:51:10 GMT  
		Size: 281.2 KB (281241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69955de265518b9a0350d0446a8659f1d17fbd7262785ae52dae2c7b501b6e42`  
		Last Modified: Sat, 04 Feb 2023 08:51:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:16c8d81d15b568e86d9af3adb0b43b0045b75e3802336254f7698eb580837343
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62071782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4acac41d564ed2278b89367728dae97579fd7cf11a1596bab17e37c117107d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:50:25 GMT
ADD file:e52d2501a6498b9d4b4b7c45345d2dd2f2fbfa7df2849d1f794768270c0971a5 in / 
# Sat, 04 Feb 2023 07:50:26 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:18:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:18:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 04 Feb 2023 10:18:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 04 Feb 2023 10:18:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:18:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:dc17d0499e93f237d6be86c3138e9cea4fd1d950920edfec3d640e8d8b6e6230`  
		Last Modified: Sat, 04 Feb 2023 07:56:51 GMT  
		Size: 50.1 MB (50095432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656fbc116e7839c44add365bae3bd4349d21d05d7b091ea4d2098e710f66b512`  
		Last Modified: Sat, 04 Feb 2023 10:20:31 GMT  
		Size: 11.9 MB (11882314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb95e1e52ca35e75a37712cbc5eb1873f15267dec919dd455270db0a0f23b8`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3a639ad9981483ad2e7134d897588b58d1ae44602db925d37a3df4025cbe07`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fa136b4bccdbd7b70f5d182c78e89a19c4e9913b13cea10f72535f20aa0e3e`  
		Last Modified: Sat, 04 Feb 2023 10:20:29 GMT  
		Size: 91.7 KB (91654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251101bfb24b59909f35cb1c42a6ff833e72f3fcdf46088571875c7b51a3f53b`  
		Last Modified: Sat, 04 Feb 2023 10:20:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

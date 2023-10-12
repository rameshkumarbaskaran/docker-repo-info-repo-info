## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:f0475edce89066a40e10b131edb8c0591fa85a3e8969d0109f53e54a0156a56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:16cbb1eda9345f0324ba6c70b41c88e505255c045e5f13483f0254954647dc74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66680291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a927db3d853ac6bb8fb07e2d1fe765a3c9c8306ccee7d6646d29ff0386d60f0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:01 GMT
ADD file:8a9222387b89a9ac763fd72610ce01ab17f64387cbfde30a6af1861a82030aad in / 
# Wed, 11 Oct 2023 18:35:01 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:04:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:04:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 12 Oct 2023 00:04:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 12 Oct 2023 00:04:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:04:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:69b3efbf67c2d9a46fdfdc8480b5a03ef73e9999a53aad57213447784f01eb6e`  
		Last Modified: Wed, 11 Oct 2023 18:39:54 GMT  
		Size: 55.1 MB (55058028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de2ad54e1d28ab4d0732492b0f71058743b3cc1ce462b29be67a2debc5d5a62`  
		Last Modified: Thu, 12 Oct 2023 00:05:51 GMT  
		Size: 11.3 MB (11311877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf7d823d1d463224a1ab066db12554e4aeea339c0b4344e6f50e7adccb86856`  
		Last Modified: Thu, 12 Oct 2023 00:05:49 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366688f505d55ba660fbe5bb2ef0f37994a0101651de6f4c1aa10003e9e2196e`  
		Last Modified: Thu, 12 Oct 2023 00:05:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e528550edeb59eb9246d8a8a6dd809d93e8441f73471395925c4f6552f369e`  
		Last Modified: Thu, 12 Oct 2023 00:05:50 GMT  
		Size: 308.0 KB (308016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6529f4eb6c5ea17807fd52a28a3fa2e38e4e8a8ccbd85f3bd4986e3533cd071`  
		Last Modified: Thu, 12 Oct 2023 00:06:03 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:28def5736de41e3ba1fea148b1337741df2b4815608de291fba9a6d380aa3cf7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c0d8d3b7ff2f05744311da620203d7c069141115a261b24b3cba2cc1b59291`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:45:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:45:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 11 Oct 2023 22:45:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 11 Oct 2023 22:45:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:45:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32e12846041adba4a404eb129631f6294dcf02d8fb43ea2bd12735db6dfea79`  
		Last Modified: Wed, 11 Oct 2023 22:46:39 GMT  
		Size: 11.3 MB (11313705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fb4bcfc75c35dacb5cef8b52c9a48bdefaa66e91b710eef04fb107d25d74b3`  
		Last Modified: Wed, 11 Oct 2023 22:46:38 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22563274bb8828acfa2bedcc64978b24b6084cd9e986fe1d0610426464ec97cd`  
		Last Modified: Wed, 11 Oct 2023 22:46:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9016621bb003d3e013b4b589b560296d95ec659fa5a0d0348c60f5e950a4007b`  
		Last Modified: Wed, 11 Oct 2023 22:46:38 GMT  
		Size: 307.9 KB (307865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeab6b1861c25d0bc76b42fa35dffd46af685c88d450e64e6dc2bf4059966aa8`  
		Last Modified: Wed, 11 Oct 2023 22:46:49 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:669085a6cfe6f100b6d8bbd4794c7d0f7959105f2d992523bf751db6c9dc5a33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68058102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87acb7a5cff2cb1676b9d6bff3d81770fc0b5d1b82366ab21b80a226176b38dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:42:07 GMT
ADD file:342c36522089238a534c0912491a4cf64b89133969e051cdad2e694ec761142c in / 
# Wed, 20 Sep 2023 00:42:07 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:50:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:50:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 20 Sep 2023 15:50:36 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 20 Sep 2023 15:50:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:50:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:00121bf241b18e981bcc804f905be7b34f95cce415db622599e21dc1a496ee8d`  
		Last Modified: Wed, 20 Sep 2023 00:47:11 GMT  
		Size: 56.0 MB (56040498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67b1bca31f3e1143c1877091fd845e9e167401f9da771c81a4aa03e152b4f8b`  
		Last Modified: Wed, 20 Sep 2023 15:52:11 GMT  
		Size: 11.7 MB (11708035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34050745c85bdb5b40ec2b02763ee30ec0a21db5c7c835de7c920779c824455a`  
		Last Modified: Wed, 20 Sep 2023 15:52:08 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23386bc675f890f16e0f2e5a06b61d9173341d61ab99cb75de1acaca0b3061b7`  
		Last Modified: Wed, 20 Sep 2023 15:52:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8095ebc692f8ff9f9a2ee3d6f337161bd68324b5512534ae1da1f62ac0753d91`  
		Last Modified: Wed, 20 Sep 2023 15:52:09 GMT  
		Size: 307.2 KB (307195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fda5209c8ff66bd769282bf04f5c83d30bb7c7de0847525480e3f9fae64459`  
		Last Modified: Wed, 20 Sep 2023 15:52:21 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

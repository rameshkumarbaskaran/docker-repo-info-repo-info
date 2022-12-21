## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:cfb3eb664c562393f5306fb8fd38d225a8c561166d72ee8328d87838a397f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ac5d865e72c1f1126c1065045c832ded9bffeba8fa20877caffff16e33933313
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66667884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06d13b3f4e1c7d10a68ddb04582acc951da3d05bbae15b7dd3faf9a21ebdc89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:41 GMT
ADD file:553d20b03d45305e58cde07e0c259421bba044155ac90b4559e5cc0b69093347 in / 
# Tue, 06 Dec 2022 01:20:41 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 08:59:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 08:59:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 08:59:25 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 08:59:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 08:59:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:f2f58072e9ed1aa1b0143341c5ee83815c00ce47548309fa240155067ab0e698`  
		Last Modified: Tue, 06 Dec 2022 01:24:48 GMT  
		Size: 55.0 MB (55041342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b37f12e58f1fc4a705a4daa73d8307d70c908d796109e35f5f6d4526a6c1f6`  
		Last Modified: Tue, 06 Dec 2022 09:01:26 GMT  
		Size: 11.3 MB (11311664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67e2b0787f31737b041e1ab2e2c79b3bd255db7592ca43a024ca67b6b56637a`  
		Last Modified: Tue, 06 Dec 2022 09:01:25 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d80f6f0895821ce27e55a64a62f240fc74667218fe1233dacb4e7e62833533c`  
		Last Modified: Tue, 06 Dec 2022 09:01:25 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d31da791920bb13ca8ce6e79f290caad9cab1a04417f88b78c1b3f91414a95`  
		Last Modified: Tue, 06 Dec 2022 09:01:25 GMT  
		Size: 312.5 KB (312508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac51fe2f086b8ef910e2ca261cb599a338796aa8592face0022d3f763bf9a8f2`  
		Last Modified: Tue, 06 Dec 2022 09:01:36 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:db5d510a21bc3996283fd5e28f235628499888280a14f0732e5b9a0e3cbc4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65327713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf84fa41ad97853569ec9c87a8881761862056c71be758aa515859220af29a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:06 GMT
ADD file:b1e7652678bbfc9556636e77d79c947ff1436888e2929f9c5c3ddb42a50c1176 in / 
# Tue, 06 Dec 2022 01:40:07 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:06:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:06:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 04:06:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 04:06:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:06:45 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4948a51a9a3f176f30ac619014f4a2da453a943244eacb53096ee9742eb7cef1`  
		Last Modified: Tue, 06 Dec 2022 01:43:33 GMT  
		Size: 53.7 MB (53699146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da28d44e099dda5a3439e3df6b208731c33e42617904d30fc960019094d83999`  
		Last Modified: Tue, 06 Dec 2022 04:08:30 GMT  
		Size: 11.3 MB (11313742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5939d42b5409aaf562108671d59657ecec104e608fe3924506ddfb7b58e9cee0`  
		Last Modified: Tue, 06 Dec 2022 04:08:28 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ab68dd460351f87b06f6cb615f0e4eb37b6777dab2ae1f37a7fecff8e48215`  
		Last Modified: Tue, 06 Dec 2022 04:08:28 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fcefb8b25de6520d9278ebc894ccb55b6a83dd81c6665faf9658e5057777ee`  
		Last Modified: Tue, 06 Dec 2022 04:08:28 GMT  
		Size: 312.5 KB (312457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ca175b87cf91702919efb70008a9911fdf997fd586aca62136b33289ad83b5`  
		Last Modified: Tue, 06 Dec 2022 04:08:39 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ad233ee8973804610538bacf987715e91cace3ec692588a58eb0064290a47290
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67612941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a023e9ecb362d69343b2c128861ebe6b4ce0cc65056836bab05eef3266fa86ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:08 GMT
ADD file:10d2f443f55d8ba9512899b3dff08f6e9a6c7ca096f407e3477e9798e1063785 in / 
# Wed, 21 Dec 2022 01:39:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:35:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:35:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 21 Dec 2022 02:35:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 21 Dec 2022 02:35:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:35:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:bde501e1d960005aee2bdf2fc8c89b26bf694dace8740c72deda4d7705995ab7`  
		Last Modified: Wed, 21 Dec 2022 01:44:18 GMT  
		Size: 56.0 MB (56005267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f053812d272c66bbb242fab63518b6139e26a79181bfc6fd938e1ca69ca02696`  
		Last Modified: Wed, 21 Dec 2022 02:37:16 GMT  
		Size: 11.5 MB (11500004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146889a8f585cb3957b5e50897c6d16f694d243386ef0980d33c5f4570fbb77e`  
		Last Modified: Wed, 21 Dec 2022 02:37:15 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7036c4eccd3fa52a00274450ed46d8e38da216995b01e04fb4ceef4279865f44`  
		Last Modified: Wed, 21 Dec 2022 02:37:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cc1f907e1f0ad95bc9374d42f6173c6b198fafe8b5425a6fe39c3e5d763d8d`  
		Last Modified: Wed, 21 Dec 2022 02:37:15 GMT  
		Size: 105.3 KB (105322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6f113576b62eb5e48b4245673dfae0a1d2fedf2c6606b90d0812de61b0ff83`  
		Last Modified: Wed, 21 Dec 2022 02:37:28 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

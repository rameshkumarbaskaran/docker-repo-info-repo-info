## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:d8f1c24640d1cde1cff903d42607dcb3d8c5d39783624611d95fb83f33b7f6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bdfe03cdeeda71223eef013f01330d44befb726694c7f0d4d7bb7bc825b9ce29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62255344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cadd3e12dbc5149955cc6f800cbe73583dd2f1215c04bf204269a3ae5afda05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:52 GMT
ADD file:643fde45a6d11f36b1178a022667e74288e58a263ac7999c7cb023cb3fcde3a8 in / 
# Tue, 06 Dec 2022 01:21:53 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 09:00:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:00:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 09:00:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 09:00:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:00:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:f8db6e5cd5802a750fd04af4eb64a857f779b9c2333d2d830a50d7b2983365c1`  
		Last Modified: Tue, 06 Dec 2022 01:26:42 GMT  
		Size: 50.3 MB (50309617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda33a9cd6f398243ba530ed6334bda146848aa4316787c0930b2daeeb2686ba`  
		Last Modified: Tue, 06 Dec 2022 09:02:03 GMT  
		Size: 11.7 MB (11663180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd69bce09da306b47bc798ee98afd88bb7558f4434f4f88e2b7162560cd89cb1`  
		Last Modified: Tue, 06 Dec 2022 09:02:01 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58013dd6eaf6025ae24d48982e89d252e94782372b25f11f3f9f5f7214893cd0`  
		Last Modified: Tue, 06 Dec 2022 09:02:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65caecbc3d9520528bc570d293912e66cb36948f64d5f480705849e1c514aaa5`  
		Last Modified: Tue, 06 Dec 2022 09:02:02 GMT  
		Size: 280.1 KB (280149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb2fba46a2e68ce1009e054dd8a08c2e4f7e959f356e936fd549200f0db7edd`  
		Last Modified: Tue, 06 Dec 2022 09:02:10 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:612bdf7104a40798afc189b952035aba92177708e85381708e1ad1c218c000bc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62260370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd937e813eae9709bb76589395ffa8b6beb628b88bebc8eccdcb6c3e8cd90619`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:58 GMT
ADD file:465db2e68facfda9a8a0c90d74ca46eaa4c6678539ba23e8b95ed5245b4c014b in / 
# Tue, 06 Dec 2022 01:40:59 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:07:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:07:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 04:07:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 04:07:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:07:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4eadaf994967069fdc4c6fb0c34ba7ff8466eb883bc166d386d6891cfde0d540`  
		Last Modified: Tue, 06 Dec 2022 01:45:23 GMT  
		Size: 50.4 MB (50356726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed6f64ec4652b7c3171c2645831997ab69b35317be6c56a1bb3b4caa4a36bd9`  
		Last Modified: Tue, 06 Dec 2022 04:09:07 GMT  
		Size: 11.6 MB (11620570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e67b31c0d7e5a83a1d975eed64de87d955972ce25a958e31324818cfe53169`  
		Last Modified: Tue, 06 Dec 2022 04:09:06 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd7ec5c16dfa5fc993395782ab3628879ad831177eae3e603b74d413cc749f`  
		Last Modified: Tue, 06 Dec 2022 04:09:06 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7017d11de64ba4289abd26711c68c33abb56ac774ec33a00329020e01d368ed3`  
		Last Modified: Tue, 06 Dec 2022 04:09:06 GMT  
		Size: 280.7 KB (280671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca967002033c47687cbaa4bfe1f29c1e321d17ec211b3134b43bc4a6559774c`  
		Last Modified: Tue, 06 Dec 2022 04:09:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b710fea38e0357114d38930b237fc67915a184f7a18119cc32956ad0720e7aa3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63328224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7e7878b19c236e6ae36609473643932806fd59b539ef80ba858749cadb92b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:20 GMT
ADD file:d73a77dc412cd093f533d8c6403c7a4a629d7a7d31b1ffc8555e0f7876d98ec3 in / 
# Wed, 21 Dec 2022 01:40:21 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:35:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:35:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 21 Dec 2022 02:35:58 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 21 Dec 2022 02:36:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:36:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:e5477ffb90e4da3fe8a2c9a63f402783b74fb55b190b59240e4d1d7e5b55a2da`  
		Last Modified: Wed, 21 Dec 2022 01:46:35 GMT  
		Size: 51.3 MB (51340127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d92863b0984c35ade24a3882575fbfd8ac767d35384197e3c0d4c5b731e041b`  
		Last Modified: Wed, 21 Dec 2022 02:38:01 GMT  
		Size: 11.9 MB (11893979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d617dc0f09c96e3c740baaa4027e01904b673f0548980cad9c898b827a17f9c0`  
		Last Modified: Wed, 21 Dec 2022 02:38:00 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e498c854697dd765d238b033958dd49256053379844767559406327d0c2aaa`  
		Last Modified: Wed, 21 Dec 2022 02:38:00 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819c827a993dfc1ea0a4fa2b75014a0d9f3f02d4f311f7564925e738bf542b4d`  
		Last Modified: Wed, 21 Dec 2022 02:38:00 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd7c80d9196d3f169bd6032192af737e119f51cb32ed5ab0dc8aa9f70ac403f`  
		Last Modified: Wed, 21 Dec 2022 02:38:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

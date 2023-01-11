## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:b60158e1da3eefa4f28b1ebe92e2d338dc63f9aa86fb91c9da8fcddf44101789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:cd2452e7e1652421c5554a9d102404b1ca4ff041b6ab49a093d11833a38cbac6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62231198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe17906ae0e0e85a9637d9327507f9e129d670bcc77faeb83ee41a6bb6cbb058`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:21:21 GMT
ADD file:e1060039de636fe2bfa207b8a071caa2d6ead322d1c2621e322409706dd97730 in / 
# Wed, 21 Dec 2022 01:21:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:46:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:46:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 21 Dec 2022 12:46:40 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 21 Dec 2022 12:46:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:46:48 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:fd14438c7d22fef775ab49a94c6b4c250839f557fcdd15c31806e0fd16591085`  
		Last Modified: Wed, 21 Dec 2022 01:26:09 GMT  
		Size: 50.3 MB (50286143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9f2ddbe13d094e2fcd4a3a2ea3ea0e07d46b9a443adf8af73cc842293bda80`  
		Last Modified: Wed, 21 Dec 2022 12:48:25 GMT  
		Size: 11.7 MB (11662266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9160daa861d010826912219cab107777a204d82a032a23cd5a3f4f6e53c4635e`  
		Last Modified: Wed, 21 Dec 2022 12:48:24 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c2f164fdab89b478fb26bb5c679504e1503e46781ddaa9706a2fa2fd12993c`  
		Last Modified: Wed, 21 Dec 2022 12:48:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d8ca673ddef49f7d2a1baceef84d260f2a2665a710f1d1a4ccc49096597c4e`  
		Last Modified: Wed, 21 Dec 2022 12:48:24 GMT  
		Size: 280.4 KB (280374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbb181b7e35f35019e87e42a96ce0a732f3965e29d68e12fa1df405b59cfdf9`  
		Last Modified: Wed, 21 Dec 2022 12:48:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:af88b34894d7b7f01c2765c14f299b63cd755e36de76165af94fb5cf43cd9f8c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60979567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a17336e16bd22b4b15623961817e6c84f58d5ff4842686b5d3dfaf0c0b37d96`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:58:15 GMT
ADD file:b780242785904e4fb27dec85c00f7e10bcc0dbb0d7006b133d9038c4328c7d83 in / 
# Wed, 11 Jan 2023 02:58:16 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 05:50:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 05:50:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 11 Jan 2023 05:50:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 11 Jan 2023 05:50:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 05:50:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:57ec0bfa7127b6c459b1b1f099459b850b4fa150e388b2c3ba10105c4a746caf`  
		Last Modified: Wed, 11 Jan 2023 03:02:47 GMT  
		Size: 49.1 MB (49084551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd28cb560887d2b6183375fcc67b6d3071f1c6e08bc75e07457c5dff669e0b5`  
		Last Modified: Wed, 11 Jan 2023 05:52:33 GMT  
		Size: 11.6 MB (11611494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2888f25ce7d2a0ba18d18a36262e18e05aaac6aa1157c90c9524bee3cdf99332`  
		Last Modified: Wed, 11 Jan 2023 05:52:32 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbb3ddee4c421e251b23894f08b3655bdd6acb794423c14c6d87826230323d4`  
		Last Modified: Wed, 11 Jan 2023 05:52:32 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc38aec5ff07f18cc019948b2863d7f98c6d10b79ae4060c655a6e72ccd11d35`  
		Last Modified: Wed, 11 Jan 2023 05:52:32 GMT  
		Size: 281.1 KB (281118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d774519926945c6539a9c64f729d787869711d3fcacf7eff02fbef4eb7480d7d`  
		Last Modified: Wed, 11 Jan 2023 05:52:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:774b377396445562c86816c5c6c8aef8b4c9df61e0ff328853abcce8926f63af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62058186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0073958a65ce70cff308ad4be5bda5a72460d9bcc738a7f1b68aeefead70f52`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 03:17:15 GMT
ADD file:70daac43e15ae08f49ca2f191e46f20fb9df90f6fa25b199b61103e75ae43d16 in / 
# Wed, 11 Jan 2023 03:17:16 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 06:01:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:01:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 11 Jan 2023 06:01:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 11 Jan 2023 06:01:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:01:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:19edd03a92bb4010fb5a10c8cc739c02db9ae484e4e25247ce4b7e0977cf1e9d`  
		Last Modified: Wed, 11 Jan 2023 03:23:48 GMT  
		Size: 50.1 MB (50082487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f499715b73481f8ed830e3119b016f36fbff9017066f4501e5d2292e80ec6d`  
		Last Modified: Wed, 11 Jan 2023 06:03:18 GMT  
		Size: 11.9 MB (11881711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd3157fc8065bafacb7cea031b92ef19ebf4a95828b4891548b2ed70279d295`  
		Last Modified: Wed, 11 Jan 2023 06:03:17 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993baf5675aac33222c34733d36710a1a9a8989f8b60b85486f77fd339ee55f2`  
		Last Modified: Wed, 11 Jan 2023 06:03:17 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b981c6b645a66da18351c765208968b066e0172c6f98a173ff8553106121119c`  
		Last Modified: Wed, 11 Jan 2023 06:03:17 GMT  
		Size: 91.6 KB (91612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e088fe89051c220a7ca3156943daf14b4dd286d3fec02aa43027b70a0c68a91`  
		Last Modified: Wed, 11 Jan 2023 06:03:27 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

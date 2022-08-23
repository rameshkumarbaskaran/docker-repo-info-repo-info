## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:17a5cdff7d0704241a872c72774bf69b0bbbb6fac8660264dd6df2c32a9f7014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fc0676b486d9fb81a658bfb0437aad832de7cc1bd4fdb3921f046ba0a0b19e06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64714808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d38f7230946bb568bd5d6c13c5575905fb3170262c5dbe4cf23af7a0e2e6c9b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:39 GMT
ADD file:0ded1ec762355d6c32b4a9f1eff5fbd5e60d15824d6bde678ef85cbdd03fe0ce in / 
# Tue, 23 Aug 2022 00:21:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 03:56:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:56:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 23 Aug 2022 03:56:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 23 Aug 2022 03:56:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:56:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:6649fedb76d916c1041e321eca86994acdb4cd14cc61ef93b5d2a397c15af4ad`  
		Last Modified: Tue, 23 Aug 2022 00:26:41 GMT  
		Size: 52.8 MB (52768784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154f30b7649dd9ff36175e6592055cf8360c6e985876034a2272424287be1cd7`  
		Last Modified: Tue, 23 Aug 2022 03:58:18 GMT  
		Size: 11.7 MB (11650922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c00af28db2666c58eba10693268b55f170ca7e71d33f6cfe0d665fca65b1b7`  
		Last Modified: Tue, 23 Aug 2022 03:58:16 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f335f65a3d201956ff81ba9ecd2c1f5355df35fc67a4b449123d4d0d3dbf09`  
		Last Modified: Tue, 23 Aug 2022 03:58:17 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4abb7659ae1e8863abcaf9faf27843788a20b3d8a6ab97236c67a4ab6ae8e3`  
		Last Modified: Tue, 23 Aug 2022 03:58:17 GMT  
		Size: 292.7 KB (292697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e31bea2350446c52f2efeef74112da2d2a9bb4c743a40f71aeb2974c793b3e9`  
		Last Modified: Tue, 23 Aug 2022 03:58:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ef1931aeb2dc2637262666afa31baa78eb95a4c3f42dce9b45b899a8bf46db99
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64761875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0322aaa2da07a1c49171cc6eef784dff0e92c8731bcbaaa8c8b384250ea06daa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:53:33 GMT
ADD file:03a6abbfc4f7f5b036b595b68d32dab2760788223365adbadd691cc6b97d3f9f in / 
# Tue, 23 Aug 2022 01:53:34 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:41:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:41:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 23 Aug 2022 04:41:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 23 Aug 2022 04:41:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:42:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:11a10710f625b85736b19b89ebf063edde4e3f2dedab0a6cc94db39e134d8cfe`  
		Last Modified: Tue, 23 Aug 2022 01:59:52 GMT  
		Size: 53.2 MB (53220635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabdc86a9e931898b29cf7967f9c2c28be4a58cfb19625fd045f236cfbbd1eff`  
		Last Modified: Tue, 23 Aug 2022 04:44:55 GMT  
		Size: 11.4 MB (11442062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f141774c9f2726ce456bb8db9225b00c099880e9c75c863d353c056381874a84`  
		Last Modified: Tue, 23 Aug 2022 04:44:53 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734280e5856004aeb3ffc8e40a0c8d7875c416d49365eb667d29948575074c15`  
		Last Modified: Tue, 23 Aug 2022 04:44:53 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2279498b9bf492480b20ce42e94635529006ead02329ad0d6c9206cbced5ab6f`  
		Last Modified: Tue, 23 Aug 2022 04:44:53 GMT  
		Size: 96.8 KB (96795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bb5d22343bdc21a6af5088ae2c94ab6d76d92ea9502744c796eef68512ca78`  
		Last Modified: Tue, 23 Aug 2022 04:45:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e3bf97218db5f0bb37164d423c9c5ebfd985f1f11b1010d397e9bb219aa11952
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66114497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bad15dd07a4ea199966e87283ae4341f4b0c244238767718e14aa78630e3ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:03:44 GMT
ADD file:56a765ed5b9c59576a105c4e82da61f928406a2ef950e7cada80b5c269a1acda in / 
# Tue, 23 Aug 2022 01:03:44 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:58:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:58:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 23 Aug 2022 11:58:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 23 Aug 2022 11:58:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:58:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:05690d5133887cdda89e6ae4808c08e8a92acf2163ce992d8bacbed497b1ddd7`  
		Last Modified: Tue, 23 Aug 2022 01:10:25 GMT  
		Size: 54.1 MB (54133693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5ad1d6167334fb78c0d0b64c9cbe4f7752fe54552840d07f8ac565e9ee91ad`  
		Last Modified: Tue, 23 Aug 2022 12:00:25 GMT  
		Size: 11.9 MB (11881634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b29ff2d158c1759c00d6d871c7e9c354245b1015ae31c3f75d222ccbc8a06cc`  
		Last Modified: Tue, 23 Aug 2022 12:00:23 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e3a5ce63d84cc0086a2a31072cfbf0e8fd15facb6012bb1a4f83731914df80`  
		Last Modified: Tue, 23 Aug 2022 12:00:23 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fec682e60212accc2fdb5c168a688ffaa7f67c356eceb14a6a5ff7ff0ed3515`  
		Last Modified: Tue, 23 Aug 2022 12:00:25 GMT  
		Size: 96.8 KB (96787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc904c24e6338eb2457eb1f810b70e7643d5fbcd8bb9ba7ab74fab4e5197079b`  
		Last Modified: Tue, 23 Aug 2022 12:00:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

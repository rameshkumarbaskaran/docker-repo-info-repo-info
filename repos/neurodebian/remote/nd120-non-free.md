## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:6e5bd37a4f6d898b500f3b3595c4407b19ec6581fccd9b44986f3343d18130ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:0e1859f5f6323c85cf124642e586dfdb8c34129c05271e0c665099db94f8323a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62205756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eb701a486f658b67be548b96faddc6b58c6e2f9e4b7d7b13b6f8415765aeb6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:17 GMT
ADD file:bc800ccc3502eee52ab13da7e930beeea45bff7ec8e6f625f2958550a0e0c4a0 in / 
# Tue, 06 Dec 2022 01:20:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 08:59:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 08:59:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 08:59:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 08:59:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 08:59:55 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:3d5213c1b98149df5de6014f7a0822d3f7c1239b55b191918b5019861d2385bf`  
		Last Modified: Tue, 06 Dec 2022 01:24:15 GMT  
		Size: 50.3 MB (50260519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34f3b713ff24584fbc4f0d01232e38cfc50e552901e86aff81379bc0b91dec7`  
		Last Modified: Tue, 06 Dec 2022 09:01:47 GMT  
		Size: 11.7 MB (11662865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038ac8a6e4b8f2ac7e55d5681f5200702296571cec417384e1b85b8996a24729`  
		Last Modified: Tue, 06 Dec 2022 09:01:45 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813b288bae82dad23a32a4ab481dfeaa06c02934f9db7d57644b0703ee85cc1a`  
		Last Modified: Tue, 06 Dec 2022 09:01:45 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f8e7214605a66deddc72a2f21f3d62d61dffbaa0cd2d60a50c46d3a85c23c5`  
		Last Modified: Tue, 06 Dec 2022 09:01:45 GMT  
		Size: 280.0 KB (280006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac62ba8aea59e8321f762d3963936c09c7833a846c8496a92386188343a7195`  
		Last Modified: Tue, 06 Dec 2022 09:01:54 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1731ec90ad96035db67c308caacfa64f0a9d669b92ebbcbccf53aa7acafaf2f9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62210962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c410435d08a2500d078bc7ae139ea2dfc4d0e63a7fa6ed4116defe26014844`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:39:50 GMT
ADD file:de3ed89259c63b45a553c11db2206a6ca4201bfd264f04890af2c672736c15b4 in / 
# Tue, 06 Dec 2022 01:39:50 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:06:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:06:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 04:06:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 04:07:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:07:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:6d78ccc24e38e1c539440b7f90d65e136bba8366864c2b4a45e3956272709049`  
		Last Modified: Tue, 06 Dec 2022 01:43:02 GMT  
		Size: 50.3 MB (50307715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da1d2c5c78abbf06d9010fd7c00be00e933cf8bb9a9a6ca3ea75916a4d7c7f`  
		Last Modified: Tue, 06 Dec 2022 04:08:51 GMT  
		Size: 11.6 MB (11620429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620697d3a391fff2ec179cf047b34d9c3c017d1179d5e34f93cf09bea4a839b6`  
		Last Modified: Tue, 06 Dec 2022 04:08:49 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255eb1b1c1cb6d5420f4f5b269c5013e04880ae731ce777e2c7867d2a36e9cd3`  
		Last Modified: Tue, 06 Dec 2022 04:08:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b272eb0ad91c8281832a02e75285913e08469432d7053bbb8aadffb8f9940ee1`  
		Last Modified: Tue, 06 Dec 2022 04:08:50 GMT  
		Size: 280.4 KB (280447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026565b9937b01c4d1ebc6afaedb12e6e09b087d8aab11e05a167871e7b7aa00`  
		Last Modified: Tue, 06 Dec 2022 04:08:58 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7ffacaf0b4c4cbeb422eeb64ffa8cd45f56565d87eee306f681fd0269c709886
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63350048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be6a3501ebf03162b51d2fbd38da65c5ec29a1292a6302a9e52e26022faa975`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:38:43 GMT
ADD file:f11f9a6e73a1ba42c97eb037cc53f119df6d6b050eaeb10df2ae716f4eabd8bf in / 
# Wed, 21 Dec 2022 01:38:44 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:35:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:35:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 21 Dec 2022 02:35:31 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 21 Dec 2022 02:35:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:35:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:bce8ae6c08a69b30b85b1e939b782fc4dee31791e21ed3abbf56d1ec1dde0381`  
		Last Modified: Wed, 21 Dec 2022 01:43:40 GMT  
		Size: 51.4 MB (51363529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731a3936d5c3e3fabf78ed8dcd67354c86b32b5d07ecffb1b5b7fa096e8498be`  
		Last Modified: Wed, 21 Dec 2022 02:37:42 GMT  
		Size: 11.9 MB (11892514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3a0ab91c86ade96a325852c7e36e65aa3ba3e48bdeaa11f860435d179da130`  
		Last Modified: Wed, 21 Dec 2022 02:37:41 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff654b887ee0a812a6e1f448a6c38ee3cec9ba594df8c2df7f5111ac56e1aaca`  
		Last Modified: Wed, 21 Dec 2022 02:37:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1a95849452ddc55f1e591df86d4f1248a78afe557bc4440a0649fe5f711bfa`  
		Last Modified: Wed, 21 Dec 2022 02:37:41 GMT  
		Size: 91.7 KB (91652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bc11abb333b5140a1621224c6b8b5d9dc2e79e7b4214cef44569df55bad1fc`  
		Last Modified: Wed, 21 Dec 2022 02:37:51 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

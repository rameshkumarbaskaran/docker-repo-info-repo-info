## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:b96f62762c24f07f75d60946e8b7d33857a78e417d1887a876c36796f0baa344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b4892cc47278d517c83054fd0bc44b0d57bab3a4149c87ba75ae5071f7af2bdc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31767993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e756c93023eddbffa6d28b4e8d8ac731f66e22f776b86d79678639f3ebd56f3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:01:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:01:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 02 Sep 2022 04:01:11 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 02 Sep 2022 04:01:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:01:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112841374cf427611c9d370ecaf3cccda8eb4c1b0d5db2db0cb67774a8f22f26`  
		Last Modified: Fri, 02 Sep 2022 04:03:02 GMT  
		Size: 4.8 MB (4815636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f47dba823027f0dc873af646b1edb234f4cec76f094e78b1af836aa84c94fa`  
		Last Modified: Fri, 02 Sep 2022 04:03:01 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9886b798b9ad3c31299f08248828d875afd8f2d9a3f5e1e92699aff48d855cf5`  
		Last Modified: Fri, 02 Sep 2022 04:03:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d2bee5d739b6faec2a288b94df1896ab7e4814b128a4b45d857912d7b61fa5`  
		Last Modified: Fri, 02 Sep 2022 04:03:01 GMT  
		Size: 240.1 KB (240113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bca31d7fa8577890035adb1cf5ed6dc94e3353a22254965d907b6d5a1ebaf7`  
		Last Modified: Fri, 02 Sep 2022 04:03:11 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:515f2929edf7b52c8361745c27fe001a9b02bcf4712e962f8266b082dedbbc19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28107573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1551ea40a4ba632e8b1a7b27c728a003bd80da13edb9980eca3bd0fe1f1f10`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:32 GMT
ADD file:7a0b62af1ae0ff529abfef9c94385824381baa3a79aaf52940bce9508f9fc3c3 in / 
# Fri, 02 Sep 2022 00:57:33 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 06:52:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:52:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 02 Sep 2022 06:52:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 02 Sep 2022 06:52:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 06:53:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:dfd1fb90fd33185f74ada410bb05d51c40a41dff4883165698330ddc208f0b2d`  
		Last Modified: Fri, 02 Sep 2022 00:59:06 GMT  
		Size: 23.7 MB (23734081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2082d38a7066e6e5c48f5f39047511f9f72c9e04bd8ab90b065dfd79d286c587`  
		Last Modified: Fri, 02 Sep 2022 06:56:06 GMT  
		Size: 4.3 MB (4263971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23edad06e4e6d72cf0f6dfdf3b11f583733dbddd3c23600cadc39d00979ce01`  
		Last Modified: Fri, 02 Sep 2022 06:56:06 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e7385a5e40b0eed565936e4f236040375d33052983bc74ce94f830693c2e43`  
		Last Modified: Fri, 02 Sep 2022 06:56:05 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a07bc775482f80db77576757182953c1db655b343b04638ac07a3e01532cd4`  
		Last Modified: Fri, 02 Sep 2022 06:56:06 GMT  
		Size: 107.4 KB (107384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23620f025a7001001666c505de88785afa58a39d01f86c08e9b096a605f17c83`  
		Last Modified: Fri, 02 Sep 2022 06:56:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

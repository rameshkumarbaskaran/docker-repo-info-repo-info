## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:6f7e4158a693399b18534ad3267f8035795545efc4892c51964046995498bab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bf750fa0661d3e6298cbccb895b45468025b1429865e249acbbf1c5854a6410c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65177036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d215977ddd052d39f939db1e5df922389edb9c2077f6343fbceb0647a8e328b3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:52 GMT
ADD file:8f3d1b2e7474fdc04cd1135312dce29db677e5567ff094e59c8338f5bd2465c5 in / 
# Tue, 02 Aug 2022 01:20:52 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:13:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:13:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 02 Aug 2022 05:13:35 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 02 Aug 2022 05:13:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:13:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:180517453f08358cf15a4972d7eafc4c2c649be2333940572c68856727b63bdc`  
		Last Modified: Tue, 02 Aug 2022 01:25:57 GMT  
		Size: 53.2 MB (53231560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd26774dfc2ca7add988708222d2ec5a8b271d124e8e613900b0ada08382418f`  
		Last Modified: Tue, 02 Aug 2022 05:16:34 GMT  
		Size: 11.7 MB (11650791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb26443561962761c21137e43dad6d243b32efdab5a5c5d702106976a9a9121`  
		Last Modified: Tue, 02 Aug 2022 05:16:33 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e59c400bdc10a6a8a04c00284a7b955c197a22f38a00d3c68eb104884dc862`  
		Last Modified: Tue, 02 Aug 2022 05:16:33 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132581afc4cd2fe14fd2f06def237abc733161ee4b2971d15f32a850fb2d3746`  
		Last Modified: Tue, 02 Aug 2022 05:16:33 GMT  
		Size: 292.3 KB (292278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d57cb3d81052503254a5793635da0dc5526efd63c19e0f3648de6c9e0403da`  
		Last Modified: Tue, 02 Aug 2022 05:16:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d6da1355fb08035ff6642e9a44a2c50f2a930512694c14d72d7730689036a5f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64856868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2239bfedc0b0b09064acc7d3944ea0e2c0af6eb2f5de108b4d1b2c6015b9469`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:38 GMT
ADD file:477966410dd9e274b01740d7af857db5c024b4c4e53a5e83b5da6854d5b0c209 in / 
# Tue, 02 Aug 2022 00:41:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:09:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:09:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 02 Aug 2022 04:09:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 02 Aug 2022 04:09:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:09:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:17bcb8e39c7f35480d4c2e5b46b6c0a58dac180206453cc49052707aa8053632`  
		Last Modified: Tue, 02 Aug 2022 00:48:00 GMT  
		Size: 53.3 MB (53311787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b23f22c8c00046bbf67cd59cd4f2af07dce5c5fa7a24ab5543ae0bb3564f4aa`  
		Last Modified: Tue, 02 Aug 2022 04:13:49 GMT  
		Size: 11.4 MB (11445839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155e679260259d507584bee8d944d898d1181db2db8ee4e81b619ee20fe55dd0`  
		Last Modified: Tue, 02 Aug 2022 04:13:48 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe48f40923db8199277d01e875d32310e9fc5ebbf9e02ea16c1397f9c07f2479`  
		Last Modified: Tue, 02 Aug 2022 04:13:48 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707dc6bc4aa4606f4136b46e3735effc8020caaff4770ef7e70e7cfdc6946bd2`  
		Last Modified: Tue, 02 Aug 2022 04:13:48 GMT  
		Size: 96.9 KB (96860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939008275e6fc63ae497488f2dd00411fc6aebe348e916c5aa4cf8740460deee`  
		Last Modified: Tue, 02 Aug 2022 04:14:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2664ba2001554b4c81910197606dbd5210149e9217d543f6b543217451c8f202
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66174221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7288077efa30d1f51895d8e4c18f4f3f0de8fb4bfbc5acb06bfff49e038cc3d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:23 GMT
ADD file:40a2042e14b22d803da216af628cd6e8603c923c4fe79ca3c4c79c95c1c1e878 in / 
# Tue, 02 Aug 2022 00:40:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:20:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:20:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 02 Aug 2022 16:20:21 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 02 Aug 2022 16:20:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:20:31 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:ef86b631f45587b4b6d1c16b80732997a4895ae8df072b14d68c25aeff8b901e`  
		Last Modified: Tue, 02 Aug 2022 00:47:20 GMT  
		Size: 54.2 MB (54195066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad56ce46d52bfd83905b2ba1001b937d0d384c2e9f52223b216e0205c495152`  
		Last Modified: Tue, 02 Aug 2022 16:22:42 GMT  
		Size: 11.9 MB (11879907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1643e5b63805dccebfbcaa3e8093baf3557f5e2d535c490c03e1dc32589240a`  
		Last Modified: Tue, 02 Aug 2022 16:22:41 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e09ccea7ebbf3f00dff13f17b94a50a8828ca7a220bc06fca82b09fd996b414`  
		Last Modified: Tue, 02 Aug 2022 16:22:41 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a54f18cb63a52981a30664a1778e0a688a3aa900a519ae5ca7ec36351fd2ef6`  
		Last Modified: Tue, 02 Aug 2022 16:22:41 GMT  
		Size: 96.9 KB (96869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b198f0f40db6b4de8cb7252ebc6718942cb14b2fbd559aebb205f5dc5301217`  
		Last Modified: Tue, 02 Aug 2022 16:22:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:f6d7debb042d01613481a9cc38b3977990e79f05f42c1df5314919e354ab47e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:8819cad84b33eb6c1bc79b66bc57442ec6013f1769b1a15cb94a3064929afd37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64949335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81d4b996394111a0bee98db43bb52d0082a16accd91893d10f379992a2bd976`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:34 GMT
ADD file:44585678df56989e743f0dcdebdd7e185769e100eba2a84aa9ae93a96dd39d04 in / 
# Tue, 02 Aug 2022 01:19:35 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:13:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:13:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 02 Aug 2022 05:13:17 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 02 Aug 2022 05:13:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9777db7a6b5e969eff343df5e4a008fcdc763cb3605175224b012d40044c2abb`  
		Last Modified: Tue, 02 Aug 2022 01:23:07 GMT  
		Size: 53.0 MB (53004390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59f5cb3889e4d9fd0bad3583d4eb2c01c548bb97b0c8ec4d461353358ce7d4e`  
		Last Modified: Tue, 02 Aug 2022 05:16:14 GMT  
		Size: 11.7 MB (11650664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab425347c427a23c6eff2ce7ba0defcf1af989e0cfbed8d47a8ec8b453e1b13`  
		Last Modified: Tue, 02 Aug 2022 05:16:13 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13d65f13daad5113e8dfe60b2b45d23f9c2fce238ed4b346abf2399b0aaa447`  
		Last Modified: Tue, 02 Aug 2022 05:16:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f028f283a4b811a56ca2711caefca693fb2c9ba1d92537ac097cb51fe73430c2`  
		Last Modified: Tue, 02 Aug 2022 05:16:13 GMT  
		Size: 292.3 KB (292266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fb50057f786f4b2c6e22bbbbc35e76bdf385d4505fe805e5c74b6c583fb1e986
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64642154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d85f229e0b7f2957ef7fefd986c043647a4ae1b7fbe4236bf2054a58d5701a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:01 GMT
ADD file:66ffd29b395276f108023b4be1a449714b6fb1fcbcaf770debb7ec6910e84294 in / 
# Tue, 02 Aug 2022 00:40:02 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:08:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:08:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 02 Aug 2022 04:08:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 02 Aug 2022 04:08:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c76fc726ec0ec853818bf6b42fbe47810086904b89f146d4ccce624e8c5a33e2`  
		Last Modified: Tue, 02 Aug 2022 00:44:53 GMT  
		Size: 53.1 MB (53097492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b768647485ba512058dc5e8741e2633c2c824515b3df68d6bb529b00c027383b`  
		Last Modified: Tue, 02 Aug 2022 04:13:26 GMT  
		Size: 11.4 MB (11445780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eedfc078f5df40bbb0cad3dbfc969497baef9523a741429b5b2bcd493d2a5a5`  
		Last Modified: Tue, 02 Aug 2022 04:13:25 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c29cbbb169da338ba631b8a90284fc7413927453ea27d1cfa4a2d378b78f71`  
		Last Modified: Tue, 02 Aug 2022 04:13:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89968d15418e30518b52b9a088f8c53d803dcc1fb8eb40381b333d096f88bf08`  
		Last Modified: Tue, 02 Aug 2022 04:13:25 GMT  
		Size: 96.9 KB (96891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:5eb5eb4acc8154408f13fc2a6b9ad02ceba4ae124c05666b50087a1f67df07e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65952811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbfebda63a0d1620a55e3595e28ab380dcf1387ac32ed9b6f9fb87bfbf9049c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:38:40 GMT
ADD file:f331e5b0e8626bfcbb682d701943586f63db1ff65d9add0d94759ecaeb8c8269 in / 
# Tue, 02 Aug 2022 00:38:41 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:19:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:19:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 02 Aug 2022 16:19:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 02 Aug 2022 16:20:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f78c3dc38f418186e278713175ef4cfc4bc70d85867d3597da89d03b5b956170`  
		Last Modified: Tue, 02 Aug 2022 00:43:55 GMT  
		Size: 54.0 MB (53974067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae8c66b4bb8cadf4b53644ccd234088106515eb05365f06331b37d3bc5eb099`  
		Last Modified: Tue, 02 Aug 2022 16:22:18 GMT  
		Size: 11.9 MB (11879913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bde24dd5326f2de30597d887c86597ef038a904e5dd0900a9d07c4662867ff4`  
		Last Modified: Tue, 02 Aug 2022 16:22:16 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0ab6157a1370156c19d5abf99e97f661c9e34b852d02789efe28253fbc45d0`  
		Last Modified: Tue, 02 Aug 2022 16:22:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415b8ec7e6730b1e84a05a158f37b694c42ddf99177223214958b8848f205c42`  
		Last Modified: Tue, 02 Aug 2022 16:22:17 GMT  
		Size: 96.8 KB (96842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

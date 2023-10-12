## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:9fa6af9d96c4b7833698b37e080a3b0e5466fb2ab0b6fa39e58122cd3d5812a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:87cede78ea8581b13aa6e4b6b326c5e85a0486ea94b9a92f627e85b4e117075d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61305603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d43b1e6aeac2909a1c8fb6159cba8dc3300c141ad3bc505bfb66b696bc369cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:23 GMT
ADD file:1efe9845e057e7029a1c2c26c148e6dc1bd9c65d0cbbb23cb49c86295d1f1f48 in / 
# Wed, 11 Oct 2023 18:35:23 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:03:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:03:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 12 Oct 2023 00:03:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 12 Oct 2023 00:03:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99db33be616a9a2a0b0b1bc913b548317bab7bd11cb6968d357457e201c44077`  
		Last Modified: Wed, 11 Oct 2023 18:40:37 GMT  
		Size: 50.5 MB (50499400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7caa4f20e587c305b46d0a06b84b849513566aab58c7020c1b49c60b2250bdc2`  
		Last Modified: Thu, 12 Oct 2023 00:05:33 GMT  
		Size: 10.5 MB (10504733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf1348294a5d4dab4b15acb8949053347c8eade80bae61aa2b027e95ac33539`  
		Last Modified: Thu, 12 Oct 2023 00:05:32 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d71e2cbf5c87b2aafc9a1f13f90fd533556379a2fc0c6c149d64d7d7f6dfd23`  
		Last Modified: Thu, 12 Oct 2023 00:05:32 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835c268da085a9e126d2aa37fc1f9fd7cc3790407c07518c452baf52960c7a22`  
		Last Modified: Thu, 12 Oct 2023 00:05:32 GMT  
		Size: 299.5 KB (299460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7fbf1698e1bcd5bd532980bfa1103b68e47d608a5ad4da5751c7356eb4c0e51e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60103250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93812c4bf943efae51ab811fbb103ddfa4b4f511d7689fdef9771f4f140d5b9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:12 GMT
ADD file:d97d8c89883987c89b2150923abea982086030e71970f5473a534e95252b4972 in / 
# Wed, 11 Oct 2023 18:25:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:44:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:44:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 11 Oct 2023 22:44:50 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 11 Oct 2023 22:44:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a7acee270b8289bdc6bb8836f1a4899f794d60337a0cdc46b58a717bd27ba89`  
		Last Modified: Wed, 11 Oct 2023 18:29:25 GMT  
		Size: 49.3 MB (49291086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd82631651b0be247be5c15b80858096e45f294834e89e72d7f5d9e0eed99c11`  
		Last Modified: Wed, 11 Oct 2023 22:46:22 GMT  
		Size: 10.5 MB (10510692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4de32cb195dcbbfe5db34eda870598c6fe8b3037920dac8fe030f4511630dc0`  
		Last Modified: Wed, 11 Oct 2023 22:46:21 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2ab50d1998ab74a191e8fc21dade576140664332f10dec9c3f39e0b2c84901`  
		Last Modified: Wed, 11 Oct 2023 22:46:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9655742ea7e48c66885785cb853feb23e701be06587e5fc5d1c3d1abd570a3`  
		Last Modified: Wed, 11 Oct 2023 22:46:22 GMT  
		Size: 299.5 KB (299461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:71e5c9783478625c86efcb64fc944f89054b7f934a8258ecc47a401973df8686
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62425270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300b9dd68032f1740af4a7dcc55c934ba883e8d35b98e05626f4372864ae9f51`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:42:29 GMT
ADD file:6603eb215d695ca693056401592eb42db80ae6d6fcd314b50322ceb7858c1f2c in / 
# Wed, 20 Sep 2023 00:42:30 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:50:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:50:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 20 Sep 2023 15:50:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 20 Sep 2023 15:50:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6be8533983dbe30a84ca98eed25142115c1c6e36639d1e5086fd77e3332abc10`  
		Last Modified: Wed, 20 Sep 2023 00:47:58 GMT  
		Size: 51.3 MB (51255415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67498dc1adefd160a039a8adbc0bd2286cb9aa4f836d52d29a196a826e264ded`  
		Last Modified: Wed, 20 Sep 2023 15:51:52 GMT  
		Size: 10.9 MB (10868432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50fb22897c317d5f10be78081ea623fc7d2ee80545630e2c2ccb88678bf6ed1`  
		Last Modified: Wed, 20 Sep 2023 15:51:50 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69ee5ed14e2116b3742cc47fe4a1473f70bf94708832c91bf861633c3811eba`  
		Last Modified: Wed, 20 Sep 2023 15:51:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34f73703175944520327704c5082b0f49d1bf711e10c7fd0b953a8638aa3781`  
		Last Modified: Wed, 20 Sep 2023 15:51:50 GMT  
		Size: 299.4 KB (299412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

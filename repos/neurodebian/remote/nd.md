## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:b057bcdd6e043e118210fded763d2b1583b5ec409eed8997ce1b6b864ca53797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:f3753567300bfb37e16eed09f3dc933b5dca9aac208815efc1e0e9625859c1ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61288810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5904d7ad98f1cf24aae4fd8cfc34b635d7dc96e9446dbae4b0a3bf7390da18df`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:55 GMT
ADD file:0936f6fccda991ba27a7f73ca61c23a436b7ca417e504b66d5a68f2283e1e81d in / 
# Wed, 12 Apr 2023 00:20:55 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:49:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:49:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 Apr 2023 08:49:17 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 Apr 2023 08:49:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:003dca91ec623536e08abc4e1bb2849836a84c44f82e24b97fd5423162a4d46e`  
		Last Modified: Wed, 12 Apr 2023 00:25:13 GMT  
		Size: 49.3 MB (49287652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647455f4f8b5d5742b5de7369dbb02d831ef39e2ad0d904d2591c27fa3ec0530`  
		Last Modified: Wed, 12 Apr 2023 08:50:41 GMT  
		Size: 11.7 MB (11717345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c56020c58f824610fcaf49b843e271ec384b788179d38eea836477c5142e42b0`  
		Last Modified: Wed, 12 Apr 2023 08:50:40 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fff5c0810b3ea2efc134ed04a10942534b6090f68978bd23390cbe48f5881f`  
		Last Modified: Wed, 12 Apr 2023 08:50:39 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4ebc188f3996c185074d048fb3bfa27ab111acfb8e09dac74a92847c47996`  
		Last Modified: Wed, 12 Apr 2023 08:50:40 GMT  
		Size: 281.8 KB (281812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2264913993d8f91a5a042d6d88402c0c89fd7d64345ac41192b5da11f69cee4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61292852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aca0b7014ca959e2a458fb8e50fd9981e7198019c1539d28fb3923c3f26b208`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:21 GMT
ADD file:2784bc6dba1e1dbea293e074ebf51fa7d89cb5545ea63ba2ed75b74d067387d4 in / 
# Wed, 12 Apr 2023 00:40:22 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 04:38:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:38:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 Apr 2023 04:38:17 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 Apr 2023 04:38:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43d214f7ab3ca35a0c9ed4d8cdf62b36248aba2fa1bbac4ecd64e82ba2520b70`  
		Last Modified: Wed, 12 Apr 2023 00:43:58 GMT  
		Size: 49.3 MB (49327656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ccbef40e57df4c4a758c5e2e2e9b630ae769e9262288419e923eb5a24ebc17`  
		Last Modified: Wed, 12 Apr 2023 04:39:36 GMT  
		Size: 11.7 MB (11680874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770dcb2b0bf4d63604f62684694e73903c581bb0003053b679e343b06a8dc89f`  
		Last Modified: Wed, 12 Apr 2023 04:39:35 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3812d60212b9fc4130a73a204f5b16475e3500440c079d9d6589fb1624529ee`  
		Last Modified: Wed, 12 Apr 2023 04:39:35 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50435e56d17531c16f9006a2c8803b8dbdb56b4dca58918a9a0b0ada9f5e3cd1`  
		Last Modified: Wed, 12 Apr 2023 04:39:35 GMT  
		Size: 282.3 KB (282318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:3b6b8e4d74f7b2e0588e78d57f42804b1199658d79edb63d4318bce88ee9a8e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62736224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a79bfdf9ea9569761583f71c192d487fe5e2b28c1b2d02afec5c88a11cdc50`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:51 GMT
ADD file:31710a830769b5e1f2612e1cd05380f677714bf52f61a54adbc7424087fd1378 in / 
# Wed, 12 Apr 2023 00:39:52 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:07:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:07:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 Apr 2023 05:07:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 Apr 2023 05:07:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35e4af56b8bda58bf958814bc36c8e3a9a1d719c8582c0f33d7d69cc5b416211`  
		Last Modified: Wed, 12 Apr 2023 00:44:24 GMT  
		Size: 50.3 MB (50310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6fe85e96c8c420958512f9b7f261930a6843f926183876a2ab71040b63c6dd`  
		Last Modified: Wed, 12 Apr 2023 05:08:23 GMT  
		Size: 12.1 MB (12141289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c6736f7382ead0267b27d16a5f707666c92d8a808590c95172291047b1c9be`  
		Last Modified: Wed, 12 Apr 2023 05:08:21 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be953d69007bced41ea3811e8f0ec4593f0a19fa20f03e948e70cc9ddeefb87f`  
		Last Modified: Wed, 12 Apr 2023 05:08:21 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56de3369c632f2e489198a1090dfdc1db235dde1a2deb239cc07eb0c9006ece1`  
		Last Modified: Wed, 12 Apr 2023 05:08:22 GMT  
		Size: 282.0 KB (282032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

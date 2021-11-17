## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:cd99cbbea095acf642255509e50391b0974600d8a6155038dfa96b6affd1a7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e6f8d676e0bae3414a4120256f1be5fc5028d50d9b50b7f469470c23ef002751
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52248784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfa181ee397979575677d60a300a60a0bb74bdb252558bfe33432975a596742`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:22:28 GMT
ADD file:d7365dd9cf34b10ca189f85c95c21a0c33e44092f85ffb5884d5e737fb0b9be1 in / 
# Wed, 17 Nov 2021 02:22:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:58:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:58:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 17 Nov 2021 02:58:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 17 Nov 2021 02:59:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:59:08 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:200cae5c9d88bb9cf1dd3fcfb831d671403f078d2310416fa3b304337d8279c0`  
		Last Modified: Wed, 17 Nov 2021 02:29:09 GMT  
		Size: 45.4 MB (45380444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be3c9de7783c5e87251f86ef4a7b2f3e9721c0b213a7d37b9cbb73c20e3b85`  
		Last Modified: Wed, 17 Nov 2021 03:01:09 GMT  
		Size: 6.6 MB (6572336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce80c836ab818f799fa9c6b5eb9843d537d08c826af1e602381bdcd5340453ca`  
		Last Modified: Wed, 17 Nov 2021 03:01:08 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3dbdcbb9197a76d62ff5bdf1f063a5895153eee08aa11cc4d4effb78499c41`  
		Last Modified: Wed, 17 Nov 2021 03:01:08 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b557efe41597d8f4398d841cc13e797dc3c43394d6e91eb5058fc778792bd9a5`  
		Last Modified: Wed, 17 Nov 2021 03:01:09 GMT  
		Size: 292.2 KB (292239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f0be000c2c81cd3282310d661167b40a8662efd09e975b459ba53001d3b97b`  
		Last Modified: Wed, 17 Nov 2021 03:01:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

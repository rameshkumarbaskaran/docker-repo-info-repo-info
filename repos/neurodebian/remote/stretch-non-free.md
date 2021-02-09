## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:518e331721c19f3257dc97e7227e85544d0ed9dd674369961c67514f9bc0be34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:cc312058ef168a41ac817dcad8c335b38ec1ccde5e5271c4a9fdcc7b5150151c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52245659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da854329d53d190558bc00e8a6e2bb6b6bad318bd679174dcc8d8a32cab2981`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:12:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:12:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 09 Feb 2021 06:12:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 09 Feb 2021 06:12:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:12:26 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b6da3e934df5b65abd1e1b5f2218611e6df8a36bfb3c2d8debef170a27b559`  
		Last Modified: Tue, 09 Feb 2021 06:14:57 GMT  
		Size: 6.6 MB (6569852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05adb6fcc5ce3f5eb84a602288ba47e5b6cba32e806d770cda5ed6d7f5a7154b`  
		Last Modified: Tue, 09 Feb 2021 06:14:55 GMT  
		Size: 3.1 KB (3150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70681e0b5142d7aad4c2484f08f24c48547d51335e6a96631fc88b8d53b717bd`  
		Last Modified: Tue, 09 Feb 2021 06:14:55 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83aa1ed202d16a63d544268991cc12a209dffcdca0aec55cc1ce2d34b083105`  
		Last Modified: Tue, 09 Feb 2021 06:14:55 GMT  
		Size: 292.2 KB (292161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c55573059b636bc2cbe927bf0e07659cbd07bdbed083dc9c26abaec35999f1`  
		Last Modified: Tue, 09 Feb 2021 06:15:03 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

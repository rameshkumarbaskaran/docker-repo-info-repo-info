## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:d51c06ea276f2eba5af3b265c17dc61411a4ff61f844e50823947294e6e85a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:94274aa5cedd7bca2aede53f12ff3f2e31bd96bb8bba13b2df27d6cce4c38b5c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66144778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10f81a9fb8b7d3af1c7792f83f44361688fb58bc0349ace2f59193b87588fb8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:09 GMT
ADD file:695398a9e249223d1e07b12d735ae1a0ce3d645d0fd4cf1478400a985311f1cc in / 
# Tue, 09 Feb 2021 02:20:09 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:13:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:13:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 09 Feb 2021 06:13:08 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 09 Feb 2021 06:13:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:13:20 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:e6f7b6573b5973ff98ec7b4368f16ac39a85fa4fa49a414c58d0a9a012d37354`  
		Last Modified: Tue, 09 Feb 2021 02:25:52 GMT  
		Size: 54.8 MB (54757786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856bad5bd5404e4bf6878a7dd210af3475d97d82759a6d9cafd44dc86d8e3cbc`  
		Last Modified: Tue, 09 Feb 2021 06:15:26 GMT  
		Size: 11.1 MB (11077537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8469be0f18af91fb31289e0ddc75d7ba8d84a0b7513033a3b0b3dc7b145100b0`  
		Last Modified: Tue, 09 Feb 2021 06:15:24 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e136da0e045bb42419cab4da5026e8fdd7fff1e6704db0e68395f5f3c8de862`  
		Last Modified: Tue, 09 Feb 2021 06:15:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e16df5b7cf50bc8a9e9c40b5d6ea8c66ae26e02445f371e17ed0ecf44b33878`  
		Last Modified: Tue, 09 Feb 2021 06:15:24 GMT  
		Size: 307.1 KB (307079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c319d00e027a9a9cdfb7333f7649474bef690c458ace78b5e4fbcd7c0c2d9f47`  
		Last Modified: Tue, 09 Feb 2021 06:15:31 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

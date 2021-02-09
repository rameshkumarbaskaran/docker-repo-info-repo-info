## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:f40f1dcea8c91dd6fb8120bc99d5484709148b566c5bbd94da7c6ec4ce1e7861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:b43b9cab3bc1faf75cf5301779b72f9cad0c083bc12d25a08f90db9da41143e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67066483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510dfbe774a213b18d59589b86cd1d833b3730de9a528a994547a9e720875a27`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:22:23 GMT
ADD file:66b4753e4d225919cb5470c007009d4dbea725cab1d3ad1cd3c0ac3b35192aa5 in / 
# Tue, 09 Feb 2021 02:22:23 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:13:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:13:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 09 Feb 2021 06:13:36 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 09 Feb 2021 06:13:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e9e6a013db8a50441790405f039006e736170b55104d06c80015cacba6d5b0f4`  
		Last Modified: Tue, 09 Feb 2021 02:28:28 GMT  
		Size: 54.8 MB (54793268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f821da22e0386f2caaa1cdad8f587ac2d65820a6d7dc5da124ab8499e31e81b1`  
		Last Modified: Tue, 09 Feb 2021 06:15:37 GMT  
		Size: 12.0 MB (11964030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb10df04cb9f9433226f82d6710d057f059ebeeaf31001f9e406ebf60493bc5`  
		Last Modified: Tue, 09 Feb 2021 06:15:35 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14daaf34dd088eacbbc412d61e68e3c2ac2eb23df59626607daf1a8de6be53c`  
		Last Modified: Tue, 09 Feb 2021 06:15:35 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093e7668aac5a623df8cda1b203bd5e15888a8073544ee3c7b7e7713fd856dc5`  
		Last Modified: Tue, 09 Feb 2021 06:15:35 GMT  
		Size: 307.2 KB (307186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

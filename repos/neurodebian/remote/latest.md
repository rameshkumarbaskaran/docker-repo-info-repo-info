## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:be75a622593d46b0c85c0dc55774436eb29a9b7b205c4228aaadfc7fdbe5fe89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:b0fb9b986cdbacd0afaab5e742974bd3ef153dd73840d547ed841c41b5c4a768
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61237937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14430ab3dcd893dccbf9811e9c3825c96cc4fe29ed53702417e21f7324e4f77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a89553ed3a7797659596b70fac74c996633d5f2cecd4360db1b6bc5aa81131d`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 10.5 MB (10499972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e2547b1380c9d77ce3ac458d0a28697a7064cda03c6239d421c365ab088738`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ba78ab5ae2bf7a1da1a747d895310235c2d28fa0a66c0eef0228e57d35e547`  
		Last Modified: Wed, 12 May 2021 08:17:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81703386770e4978fe71acaf5810bd4542e8e9fb5a7ed87bd780399f6885fddf`  
		Last Modified: Wed, 12 May 2021 08:17:32 GMT  
		Size: 302.7 KB (302715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

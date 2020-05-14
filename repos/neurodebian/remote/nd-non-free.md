## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:c947883f06698de3ac9896189a1beba94720e99a0d7b8dfdf9b9964fbc477ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:43fa7027acc7f1cd87147858fe6df0cf36840830ec7e60161a11c4b1adfb8d81
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62663812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c4ce75113d3b66d6eb701f972dcf48f220adafd9bed188c80632c5a98e6ce9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:22:30 GMT
ADD file:1b99a100214a4a86a413bf6a826c70d07fee06a8c4e6d1f3ed1550fb08f9818e in / 
# Wed, 13 May 2020 21:22:30 GMT
CMD ["bash"]
# Thu, 14 May 2020 21:33:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 21:33:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 14 May 2020 21:33:02 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 14 May 2020 21:33:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 21:33:12 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:268c82fb25093fc20c25872a9f96ca2bef121a19a81a91079b62afb96b725135`  
		Last Modified: Wed, 13 May 2020 21:28:35 GMT  
		Size: 51.4 MB (51390987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1d4fe7b88876748fd900c46eee6d4358391ceadde5c47ad5a21b832c15e052`  
		Last Modified: Thu, 14 May 2020 21:34:00 GMT  
		Size: 11.0 MB (10971121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd26f68b39fe65bcd00c98f25b23878f4fe589e4598e9dbf0f1e3e77c53826c`  
		Last Modified: Thu, 14 May 2020 21:33:58 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3048441fe43a960aa30be0137c61b477b483529b679de4ecfba8c4cc984e1b`  
		Last Modified: Thu, 14 May 2020 21:33:58 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc55548f46d469c43884bc70f054739741b066b117d60fa1ef03b85850e5ffb`  
		Last Modified: Thu, 14 May 2020 21:33:58 GMT  
		Size: 299.4 KB (299390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73daf7d0313e602fa6620d4dc6eb02707218c40c6c7630582e52fa50adf9bde3`  
		Last Modified: Thu, 14 May 2020 21:34:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

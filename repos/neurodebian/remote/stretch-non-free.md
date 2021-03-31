## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:6c2a041923ea5cd5381fca38eb32dd09dae8369d43bf20bfc04f7d25a7f05daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:739e4dd3162188dcb64401e9d3f7c7b6493620647363721e24627d133cd0d4bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c586463197e1e6a5285f7d3326b92bdc8864b88767d7fdd54b015f2e53e3f7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:55:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:55:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 31 Mar 2021 04:55:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 31 Mar 2021 04:55:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:55:34 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dd7be4644b74987b9b75a1a96446adc440c11635a2fdf0b0c5885ef1642e11`  
		Last Modified: Wed, 31 Mar 2021 04:58:07 GMT  
		Size: 6.6 MB (6571714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9b1951f2106b1141c96bfc8d902b8b6342014ccd715702d249cb3323a7bcb3`  
		Last Modified: Wed, 31 Mar 2021 04:58:06 GMT  
		Size: 3.1 KB (3150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e7b55e646949876c1d4b81d778b8b96284a8f179054be420726429e8d8baae`  
		Last Modified: Wed, 31 Mar 2021 04:58:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a56acbb7b1f003e366f7f2b3c1eaaf3dc48b91588ba226d2a535918e1da0d68`  
		Last Modified: Wed, 31 Mar 2021 04:58:06 GMT  
		Size: 292.3 KB (292290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9eeeda4183c6b82ff3153c9c65d24674672c661cfff8bf72cea4b6808d8120`  
		Last Modified: Wed, 31 Mar 2021 04:58:20 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:92327c201c61f5337a4119a8c56407a49a16e2a7436f0765245837bff8332ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:79ee45e0265c33f46941e318e035956cc9877442334cc0b91cdba9953e691787
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66555822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a980954ae109fc21c3e21808c86d81a4afbd01784d639544fd014a00ac1543c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:30 GMT
ADD file:5259fc086e8295ddbf02e48abef38e9bf93a183079d3631aa7a59306b7f2f9df in / 
# Wed, 17 Nov 2021 02:20:31 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:59:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:59:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 17 Nov 2021 02:59:49 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 17 Nov 2021 02:59:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:59:57 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:647acf3d48c2780e00cd27bb0984367415f270d78477ef9d5b238e6ebd5290da`  
		Last Modified: Wed, 17 Nov 2021 02:25:17 GMT  
		Size: 54.9 MB (54932774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bee1d7936c37070e49cf90c531a7b07d6c473f314c2a6eadb39cc71cfb04d99`  
		Last Modified: Wed, 17 Nov 2021 03:01:55 GMT  
		Size: 11.3 MB (11309460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb33e150f4293ff23d4b0fe0b02ba31eb24e61dacda449b262277da2d338fcbb`  
		Last Modified: Wed, 17 Nov 2021 03:01:53 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb4c7184066107fd7227e3db8748ec0ebc93f1a265a28da69438a9a8d1a87e`  
		Last Modified: Wed, 17 Nov 2021 03:01:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bc5105431211ba24f7a6555da03b87cb4b425b14718e44d9d95d9ce1b8087`  
		Last Modified: Wed, 17 Nov 2021 03:01:54 GMT  
		Size: 311.2 KB (311215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f3ad19f18eb9fad91a5472e0747a464c3feb29b59dd9857d190041c113677b`  
		Last Modified: Wed, 17 Nov 2021 03:02:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

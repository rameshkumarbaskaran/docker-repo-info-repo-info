## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:cf2a6d87f1a57ba2983ec811aabf49278aad8d4e6e100e7d307d2d7b7eeb9167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d9ccb959e33ae77543c0d8bac3ff81ab7f75ad514ee50922a669c1233b3f9ba4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61189625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a7fe58e75bd0702046f7745e084b32dd314d06c38a28bcb2bfeaf9c615fae0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:20:19 GMT
ADD file:a50affde4f5ccdfd6450a642199121ffc180bb8cace944a55fab7a78ea851199 in / 
# Wed, 13 May 2020 21:20:19 GMT
CMD ["bash"]
# Thu, 14 May 2020 21:31:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 21:31:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 14 May 2020 21:32:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 14 May 2020 21:32:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 21:32:12 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:be2ea06d55bb33c31098151d199a24029c4e0dd6bc5b3da9f617bb04e37d79d9`  
		Last Modified: Wed, 13 May 2020 21:26:07 GMT  
		Size: 50.4 MB (50387525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15594b9f8549e62435521c0fbaed0a90e844ad6ea5afedae86eed0d412060c49`  
		Last Modified: Thu, 14 May 2020 21:33:47 GMT  
		Size: 10.5 MB (10497223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa7e52b9296a5a6105180c1dceb0d296bbb4a26266215958dec9ac339168c62`  
		Last Modified: Thu, 14 May 2020 21:33:46 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b334e14a2d8631cc184e4b9a52b2909ae699ac1cf0044bf749d7d36472ed309`  
		Last Modified: Thu, 14 May 2020 21:33:46 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afd47a018f1b1af17f8f8be34cd299bd49709df326c97c6d5b0ad7b09d65c96`  
		Last Modified: Thu, 14 May 2020 21:33:46 GMT  
		Size: 302.5 KB (302504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f48a82383725e1676705efd460853c9b490b112f7e7678a9ddcc15846eef89`  
		Last Modified: Thu, 14 May 2020 21:33:46 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

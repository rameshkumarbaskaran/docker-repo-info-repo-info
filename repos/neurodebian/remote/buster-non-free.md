## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:daa2bc573ef6fb1eb99e0079c3aca45ed9b50f70aebc11dcafc60a0167bb2a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:94bbcedfe7025e88c5c55469de8bcd486781ef1bb4d0f780e7c87501d4c04baf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61238054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bff6c9d41f8e0d654c85be67a36d6223a16ebf9581a44dc4ff38c626a17452c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 07:27:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 07:28:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 10 Apr 2021 07:28:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 10 Apr 2021 07:28:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 07:28:19 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8f20230089518e24885579150cb0391a75fc9254206ee720dd881e2947b98e`  
		Last Modified: Sat, 10 Apr 2021 07:30:35 GMT  
		Size: 10.5 MB (10499951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbf19144b065a56695d8e40e10170c1d1066817a765981c2b1e3f94527c3b02`  
		Last Modified: Sat, 10 Apr 2021 07:30:33 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b50a6abc3882ffc350486db083ed73547cea58720ab65f8118989aefff1845`  
		Last Modified: Sat, 10 Apr 2021 07:30:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cb94eddbc8d59baaed80f384d7e9f5cccc93d94daa1d7b6b0df15add8fdde1`  
		Last Modified: Sat, 10 Apr 2021 07:30:33 GMT  
		Size: 302.8 KB (302756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2fcbe2ad9930d564b05b99584e034f19e574d38532b4f1365fee54baa364524`  
		Last Modified: Sat, 10 Apr 2021 07:30:48 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:b02dfa83d124e86d05a8aa5128b15ec91e377bd504bd2cae33a61ba473570336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:4dfecc6742c94c5c4b657a731fd1015e57020b2ab611439978075c584d57496b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61203176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf5ef55c644ad6fc40b8f0d452ee9fb0a6f90a7ca24bbe810cd221714da824a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:8f75f11b2bd2d50e5912359ae750de06a7b49506df3756c19baf4cc63d900c4f in / 
# Tue, 09 Feb 2021 02:20:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:12:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 06:12:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 09 Feb 2021 06:12:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 09 Feb 2021 06:12:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0ecb575e629cd60aa802266a3bc6847dcf4073aa2a6d7d43f717dd61e7b90e0b`  
		Last Modified: Tue, 09 Feb 2021 02:26:22 GMT  
		Size: 50.4 MB (50400198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbff3086d09b4748de4c8788908da586c4b41f28e37abe2b2dfb842d0541abd`  
		Last Modified: Tue, 09 Feb 2021 06:15:11 GMT  
		Size: 10.5 MB (10498496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62360ea9d7d0a0a3d4e224316e06ed9a31ca349870e827581089723679918b7`  
		Last Modified: Tue, 09 Feb 2021 06:15:08 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83855cf0bebd48bd93d8d4ddadb942f29d1f69e45d323881124d63f92c96c600`  
		Last Modified: Tue, 09 Feb 2021 06:15:08 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537805aaa01f0636ef918c066ccf5ea1e8d880eff9a3c038fd0de8750c70053b`  
		Last Modified: Tue, 09 Feb 2021 06:15:08 GMT  
		Size: 302.5 KB (302480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

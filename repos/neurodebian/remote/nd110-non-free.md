## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:2f62ad5bc04c1a030a43f2ebcd9d68b419968f7d13546f0f1f7ce0913959d859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:59f26fa2338256f6ef9cd9c98e0a2072af8c9cb79b2580965131f6785504212c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66440491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2613e01ef97c316981cce42185f519c8647010862e3040473553695f3e81385b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:04 GMT
ADD file:a858c472d72a55a1ed0b7b2fd2751bac78f77e3549a7533c508022aef7204233 in / 
# Fri, 12 Mar 2021 02:20:04 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 11:49:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 11:49:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 12 Mar 2021 11:49:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 12 Mar 2021 11:49:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 11:50:03 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:da21a291c553cde4f403910fa28fb69cad95f63ce1b378f341eb17738b45a6ac`  
		Last Modified: Fri, 12 Mar 2021 02:24:58 GMT  
		Size: 54.8 MB (54835833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff9b1a237e1a0b265f7881194e3c5176149ae4aac479b6e579c343f1edab1d7`  
		Last Modified: Fri, 12 Mar 2021 11:54:07 GMT  
		Size: 11.3 MB (11298426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b236272cc51b7e66738891009e64ee566231ce1f213706aa2523352a62c8b78b`  
		Last Modified: Fri, 12 Mar 2021 11:54:05 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae6e9341db3a29dc1de98f1ed37bc5a823e06d60173e0ea966b08143caeadd9`  
		Last Modified: Fri, 12 Mar 2021 11:54:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21551368594d7120f11938c377f52dcf91784c2aa4c1a8029972b21a7a7b4896`  
		Last Modified: Fri, 12 Mar 2021 11:54:05 GMT  
		Size: 303.9 KB (303857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25948413831539c2e383bd3533a1a4d503ae4986ba4273621ed382a845f7cae`  
		Last Modified: Fri, 12 Mar 2021 11:54:17 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

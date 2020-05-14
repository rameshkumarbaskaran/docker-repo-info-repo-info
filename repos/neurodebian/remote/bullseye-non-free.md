## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:e77655804e911607b83e832cf2a936e5b818ad0755c5b9a083b30530dc91ebfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:381eb9f23379502d7719b201c4d77a410eadc5c38071240b4aefda834a04b20d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62657733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3faaa2769298b7e7fee16a499f5620c537c746608f06d8649941f14c541fa5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:19:45 GMT
ADD file:19778292422b784c4eb17d79e7632fc1e3619b6bbbcf16a37bb6179a5c725b1b in / 
# Wed, 13 May 2020 21:19:45 GMT
CMD ["bash"]
# Thu, 14 May 2020 21:32:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 21:32:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 14 May 2020 21:32:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 14 May 2020 21:32:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 21:32:48 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:5ce4ab219a2f8bc551eb2502df5b719a1d8a32c4bbb00b3629001ebb6c5e0b94`  
		Last Modified: Wed, 13 May 2020 21:25:41 GMT  
		Size: 51.4 MB (51384672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173b56f08cc3c0d71f38101c19064df33289c98255f3c9eb96a85e1fb3300cbd`  
		Last Modified: Thu, 14 May 2020 21:33:54 GMT  
		Size: 11.0 MB (10971290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa3761e8ca467f2c0edf494c1b5906b21b550493ed9d5ba6856fba3beddad64`  
		Last Modified: Thu, 14 May 2020 21:33:52 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79443821d55836c0974012787d4adec1e8896795e432eea112ce4b82572cc1f7`  
		Last Modified: Thu, 14 May 2020 21:33:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cca23d33c50c37bc221a153aef0e011ab1417d0262f2bac51cd843e03c1e8d`  
		Last Modified: Thu, 14 May 2020 21:33:51 GMT  
		Size: 299.4 KB (299443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a604a53045f642ec2e0bd63845cff782a44333d68b8f61c1b10d868fe4cd6f`  
		Last Modified: Thu, 14 May 2020 21:33:51 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

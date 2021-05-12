## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:a7837f3e1fa8ddb0e990ff95f60ef492335b704dc329d7e12bd68854399eb1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:ddb092b2331787edfd0af3d4b4e528328da48691ae71b8b1baccbe8bbaebb0c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66518353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606f43da98b618c3f2d43c8187dccf688e86da2f44abe582bd1684592b4f9523`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:22:07 GMT
ADD file:b00402c4b2c5828b18b251f8a057510f9f7da733f833cd147ed1a8fcb8d574db in / 
# Wed, 12 May 2021 01:22:08 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:16:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:16:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:16:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:16:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2746b657344bbd3149c23794266413a61b32b44f53688f3619e485894c87b09`  
		Last Modified: Wed, 12 May 2021 01:28:33 GMT  
		Size: 54.9 MB (54896691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db24a845c6c5719feb645b6c40fc3b9ad68b478ee8f445438bb62ff239ce8c70`  
		Last Modified: Wed, 12 May 2021 08:18:23 GMT  
		Size: 11.3 MB (11309128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c809501e4bc2c38d8a90b9796e38b490408f53254f3d5fe0193dc1ec1e21711b`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bee38428ade9f57f57507e89a9f0528339d2c6272bf80b7731266137c46b5f0`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6df1b9768570a2168e04e6ace7e4a069e395c92065be4a06b0f2151f1d5332e`  
		Last Modified: Wed, 12 May 2021 08:18:20 GMT  
		Size: 310.5 KB (310531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

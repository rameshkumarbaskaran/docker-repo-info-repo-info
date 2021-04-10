## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:25dbdcb1deb71415adcf6458225e1ff04a3917d7fc8de27c0a3b3a92a67e8adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:0d2d7430ee2f7c290f87a3c68315d8d498a89933e193116b1782e11a5bb75fbe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278a73fe8185e6d57cc883c9f3dd0de1b1f17908a5a60bc0bcb2ed58ab624755`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:41 GMT
ADD file:e3d37689e896a83d39040f2c95091ff88f3899b5b410dbf76908dd6c938b8cb5 in / 
# Sat, 10 Apr 2021 01:21:41 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 07:27:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 07:27:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 10 Apr 2021 07:27:37 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 10 Apr 2021 07:27:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 07:27:49 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:76b8ef87096fa726adbe8f073ef69bb5664bac19474c5cce4dd69e08a234903b`  
		Last Modified: Sat, 10 Apr 2021 01:27:52 GMT  
		Size: 45.4 MB (45380037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c885f376a93641530dd47c95299862e91a0245cca5c31e458d06f20dbcf8fec3`  
		Last Modified: Sat, 10 Apr 2021 07:30:12 GMT  
		Size: 6.6 MB (6571641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4386dee5b36d62ee041bb887b0ea7120da4c7e45b58ae164200a778da7d1fe3`  
		Last Modified: Sat, 10 Apr 2021 07:30:11 GMT  
		Size: 3.1 KB (3150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c43b8ebd1287a8e4bd2b820eef33a43b9edb84d7165cc0959a1ed0d03d0a35f`  
		Last Modified: Sat, 10 Apr 2021 07:30:11 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0f390d96db241521fb7a058018bb6fc15db951da433120a4dcb74107659141`  
		Last Modified: Sat, 10 Apr 2021 07:30:11 GMT  
		Size: 292.3 KB (292264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b5e3df1b3584f47cff1ddeb78124eeb972f86af6aecaa4cd77c8d6ab84bcbf`  
		Last Modified: Sat, 10 Apr 2021 07:30:22 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

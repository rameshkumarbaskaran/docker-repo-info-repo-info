## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:8af13616e7007bbafa12f6999bd8e90fe8f5f6d40dccb2f8c5a26e07a3e5f1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:bab5b7ecd5e3ad978d94a2330603a351fffa6fcceecfc38afbd43d260d8e6c4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61240999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ccd6570c7bef854fe535e42d380e0d855c76ed0e70b8877ab66a96bce16ab5f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:22:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 08:22:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 28 Sep 2021 08:22:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 28 Sep 2021 08:22:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b9f2225f69d1643192a962703bdae5fa16cca2178732efdf6fd6cb39153a3f`  
		Last Modified: Tue, 28 Sep 2021 08:24:22 GMT  
		Size: 10.5 MB (10500018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9607a259996efd656dae0770ded1efa272f9739286165c16b61cc400f4229fb`  
		Last Modified: Tue, 28 Sep 2021 08:24:20 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281ea011312fcd4c34be33bb8fc0c1177bf8d00f709f3400f42b78f99a0e5c67`  
		Last Modified: Tue, 28 Sep 2021 08:24:20 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8e9646d746cf6602f0c62a4417f518c77f5ef5338a496802c70466a422a26c`  
		Last Modified: Tue, 28 Sep 2021 08:24:20 GMT  
		Size: 302.8 KB (302765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

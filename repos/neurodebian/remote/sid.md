## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:1fc1fe514fc70fa11cd9114cf9680a94502ecaafe292178829fd90e1ee31bdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:de39a5f9acdac1ce2abff14ce4602174a9fd578e8e4c5f924e0f1c6e981589d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67348581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c9e968105f18175cae419018b54405441fb9b3ea79c57b0fb7f613f253bd2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:24:18 GMT
ADD file:43a49c0ac74573bd560d191480bb30b2950f21ec76e9b3bdffdf73eb74628c50 in / 
# Tue, 28 Sep 2021 01:24:19 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:22:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 08:23:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 28 Sep 2021 08:23:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 28 Sep 2021 08:23:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e3fead4ded84f6449ee17b9deabf1e9144512edf86da02e0f93fbf81df3fd6fb`  
		Last Modified: Tue, 28 Sep 2021 01:31:21 GMT  
		Size: 55.7 MB (55702084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdd771dfb3f2ddd1fc330803615949ced8b77959f1721f6874210cc2ed89cd9`  
		Last Modified: Tue, 28 Sep 2021 08:25:08 GMT  
		Size: 11.3 MB (11337666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08695614570413bc4593392b287a7585ea91fadad04f32949e23085e60a10b34`  
		Last Modified: Tue, 28 Sep 2021 08:25:07 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47945ddc1dd71661ed0f1b3d83b2c82416ad50cf1f3ecb895f83dfe767d4a20d`  
		Last Modified: Tue, 28 Sep 2021 08:25:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cd386a1f133a2dea230d07b1005b946e2ee004ce7db68b6d8e03d760d9a17d`  
		Last Modified: Tue, 28 Sep 2021 08:25:07 GMT  
		Size: 306.8 KB (306829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

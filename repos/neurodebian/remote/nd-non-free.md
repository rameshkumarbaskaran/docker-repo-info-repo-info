## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:97a40ac21032c18cad0ce897c27cfc8f30fa934796e81fbde5bf776e89aa4e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e4c42ae18720a17725e81fd99326e25bfe6f45646e3193f10c680aff7dc6751d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67348896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bc68186084e260d9d00c3b08e2683a2801968dc0817272d3cf3561407b7a4e`
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
# Tue, 28 Sep 2021 08:23:11 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
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
	-	`sha256:59fc97b1d4080b62fe6a9e15e42294d9c8535f34a7373ce981df3cbeb25f203b`  
		Last Modified: Tue, 28 Sep 2021 08:25:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

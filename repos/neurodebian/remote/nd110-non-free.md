## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:764795d0f70ec491cfdcdb2f01198545567c5153a3263765d25a1e5a995de676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b4519e62ef49c1a98ff346ddf68cde5eb8a0bc57d7d146191087ccd885bbb600
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62278456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333b6d227f4495dfe589f9a14dd77d1372bd1ba1958f7fdec54f8369598d711e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:53:35 GMT
ADD file:f025f6ca1e77fe1656f616d970b982e054e3710b4b339f3348c89ebb8be98460 in / 
# Fri, 22 Nov 2019 14:53:35 GMT
CMD ["bash"]
# Fri, 13 Dec 2019 00:27:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Dec 2019 00:27:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Dec 2019 00:27:31 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Dec 2019 00:27:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Dec 2019 00:27:41 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:648fb216c0c2ed5d1c0dbbe64e65bcce21a5ded98ee34f3c7317dec5d5c1bef3`  
		Last Modified: Fri, 22 Nov 2019 15:02:04 GMT  
		Size: 51.3 MB (51290947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9915f1dc57190c059fef0be042aac59e53511b22e6df16fc40f0f7e761319021`  
		Last Modified: Fri, 13 Dec 2019 00:28:17 GMT  
		Size: 10.7 MB (10686960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4125a10e023e67a204056c0b0c858dfe08862905db57f538c65e9c7502087aa5`  
		Last Modified: Fri, 13 Dec 2019 00:28:15 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08e221032a5dd04f8b9cc3c1b7c54bbe185bf9c54b89f04164737d818653436`  
		Last Modified: Fri, 13 Dec 2019 00:28:15 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ca4320bdfa03e6f8fbd623c507e04b7c6d8061cbdd1f9e721cf465985d00a9`  
		Last Modified: Fri, 13 Dec 2019 00:28:17 GMT  
		Size: 298.2 KB (298225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270dd72106886febedc3caf7199823e9c90e7a130760d638e2066c0faa10e6ae`  
		Last Modified: Fri, 13 Dec 2019 00:28:20 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

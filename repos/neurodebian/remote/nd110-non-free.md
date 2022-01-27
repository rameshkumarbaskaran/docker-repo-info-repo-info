## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:b997a38867c8624aa4840d513642392a33be37cb44852f764b5050572df148c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b81ce4e458d986e48a4a396d7ff198364410c13186b58d61ee914806a9c28afe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66540284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5f759e20cd05754676c25be8f6e1391e7e3198732c37ab2ceae8b0e0f728ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 01:03:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 01:03:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 27 Jan 2022 01:03:58 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 27 Jan 2022 01:04:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 01:04:11 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6023f5479eeafc3746e341793cb77e27c713f1cacb5271cc6d1c2f4e988309f`  
		Last Modified: Thu, 27 Jan 2022 01:06:57 GMT  
		Size: 11.3 MB (11309489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d9b439931b738eec925c21b2dab16947ee9b77cc2d2500e34e001ebe361e62`  
		Last Modified: Thu, 27 Jan 2022 01:06:56 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b894fbc5167f636883931f934ead6cee9ab0b91e22134dc2163771f49316af1f`  
		Last Modified: Thu, 27 Jan 2022 01:06:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48c43b3e2401a0f240d5e10624ad87ad3f556ddf142466147b062784c0f6889`  
		Last Modified: Thu, 27 Jan 2022 01:06:56 GMT  
		Size: 311.3 KB (311257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72641613896dd4d8a17958c0ac32c10f518eddb278db1ff6a89737251024f77`  
		Last Modified: Thu, 27 Jan 2022 01:07:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

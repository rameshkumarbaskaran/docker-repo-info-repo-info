## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:9628a4cf8f7301a3b40248447315781604411fdd38b0e8a801d79b43c403be42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d91c6de7a25800034f9fefeee2997c0d3356621101646b1240e260c6658cb9b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66486225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b4ac3d8296a63bb50f6b162e48de7d42593a3ae9edd75aa2bd55312f8a4193`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:19:44 GMT
ADD file:09ffbc0a4ab7c70a3071740e19113a2f2d61593241bfb8455aeeea7877b8784c in / 
# Sat, 10 Apr 2021 01:19:45 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 07:28:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 07:28:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 10 Apr 2021 07:28:35 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 10 Apr 2021 07:28:41 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 07:28:46 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:cf7e31f852204930ef60bd4c12f9606812c0b9ba6235e2e46e1a5900f2db9d30`  
		Last Modified: Sat, 10 Apr 2021 01:23:56 GMT  
		Size: 54.9 MB (54868257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb09fa2add46c748c79de9bdc525ff35da97411c1609fe80e009d6fc4d8741d`  
		Last Modified: Sat, 10 Apr 2021 07:31:04 GMT  
		Size: 11.3 MB (11304944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b8202dc26af809ac9fbb769496b4cf7129a7efb9b9a52a268e0c2269be6591`  
		Last Modified: Sat, 10 Apr 2021 07:31:03 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf385b56cf3339720faa4725fff6ae60295c698750ca978900bf9860070f7e1`  
		Last Modified: Sat, 10 Apr 2021 07:31:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bbfba981e0ed35f307481b5a05470df58a6d2efae1c837a5ae10155611192d`  
		Last Modified: Sat, 10 Apr 2021 07:31:02 GMT  
		Size: 310.6 KB (310646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6d16cd5a08dac2b60a36224f751d16225574ef4b6b87a580f09c72f6dd5b9e`  
		Last Modified: Sat, 10 Apr 2021 07:31:14 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

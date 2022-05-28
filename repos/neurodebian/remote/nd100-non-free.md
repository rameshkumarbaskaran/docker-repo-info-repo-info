## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:34bd541da284138fed75724766e0d5e3cac218103ccab5d712db0e8002858d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b6f2c3e37f8532066293ccd087ca1f2511ae131f78439be9a9d3ab8dc26991f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61245865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d9e8dac7e90dcb98355f93be5c3ac21e3621c86c21152b1ecfdc8ea81e94a4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:32 GMT
ADD file:5c5cde050dbdbd5c7c0d9c723f436d37ab4a8b1a498647a719771eccce99d9cb in / 
# Sat, 28 May 2022 01:20:33 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:36:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:36:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 28 May 2022 05:37:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 28 May 2022 05:37:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:37:08 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:982cba7e471c6d3ce96014cf58b2e4e115a525e60da2e1e08716818f2c057a6b`  
		Last Modified: Sat, 28 May 2022 01:25:39 GMT  
		Size: 50.4 MB (50440422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b408b972c76f457b5928d48a45e6c6669ce35818a0c203b012c6966b8d654289`  
		Last Modified: Sat, 28 May 2022 05:39:10 GMT  
		Size: 10.5 MB (10500296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f476d1ba5bb41283ab8a2ef5d7968db4f7e10aab5242fbb3f8381dab67b636`  
		Last Modified: Sat, 28 May 2022 05:39:09 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a556d3bcd634466f553097ef3d03a9bd26dc13edafe9511d4254a1fc257c45e1`  
		Last Modified: Sat, 28 May 2022 05:39:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b5e5f807a99c180c7ceadd62cd0a13b22b4f9edae5661acf56bc40c9e9b169`  
		Last Modified: Sat, 28 May 2022 05:39:09 GMT  
		Size: 302.8 KB (302771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca022902e8dca86c10ed36509f07e5cb9ccafaacbf0687a47d858b5f7e344c66`  
		Last Modified: Sat, 28 May 2022 05:39:19 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:88d693ff34b70e5e6266e98fbe62bc88eeb1176ae3b92174bb0d337e682f593e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:7056363040e3b84ccb0d3250a44795ec572d358ecb7d6dc199794f095a226819
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34451516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b8679711853a140ad886941bedb94b5510767a807f499d7d57f97bf0bcb2c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:01:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:01:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 02 Nov 2022 20:01:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 02 Nov 2022 20:01:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9ee11ced6ce3628dd76da6f9b32365667037b587d0f1ae675cb2a4629389c5`  
		Last Modified: Wed, 02 Nov 2022 20:02:34 GMT  
		Size: 3.8 MB (3766036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155dd1cba560a39394f12b7bb11cbe55093fc07c73ee7ce2190b561eed81ec37`  
		Last Modified: Wed, 02 Nov 2022 20:02:33 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebe0153f555168992558fd867c5d94edafdeda493db3c7489cd9adf43560691`  
		Last Modified: Wed, 02 Nov 2022 20:02:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0661a238b2aa1511c003a9b095b2e3dc69dfc0ebf7be0a964e062603a33d34`  
		Last Modified: Wed, 02 Nov 2022 20:02:33 GMT  
		Size: 257.9 KB (257866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:606fc934cc10adf112459debf00d1cb31a8c8ccfa51623b3333934529507aaeb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32385565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bc81f27b938cb0b49110fc450d5ed000e223b6c5bebd80d5d2705d55548f75`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:57 GMT
ADD file:429a55a11d4bcd15647d1316d9debd9ead4b4ab5c0b9146894d07c39aa814290 in / 
# Fri, 09 Dec 2022 01:46:57 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:13:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:13:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 09 Dec 2022 02:13:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 09 Dec 2022 02:13:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:10175de2f0c4f7d306f660ee073bce12b824c8012dd19b3c140aae053fabd1cc`  
		Last Modified: Thu, 08 Dec 2022 18:50:01 GMT  
		Size: 28.4 MB (28384475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a38a0b51aceb83e26511a744d43dbe7004b12b9e67b6e047c1f2a2aee9c7b26`  
		Last Modified: Fri, 09 Dec 2022 02:15:38 GMT  
		Size: 3.7 MB (3739828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b6a0dc794a553e78321179be92acba4e99bad9323bb55f602adc86cac773de`  
		Last Modified: Fri, 09 Dec 2022 02:15:38 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17bdbba7a279b9cfc82132dd3a3d8619b85f435f48aa83168502847b78f3f2eb`  
		Last Modified: Fri, 09 Dec 2022 02:15:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695183e7f4f7a0c211cb93b2f4451ad69424ac3a00f6000b2ace8ff07bdd733f`  
		Last Modified: Fri, 09 Dec 2022 02:15:38 GMT  
		Size: 259.3 KB (259253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

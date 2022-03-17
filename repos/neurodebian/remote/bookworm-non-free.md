## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:b03ec450819ffe43f360eb27780fcb659b5b46a78e1ace688af5e90883ad716a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d57516234db238418490c7540bcb072084b919dfbe4d9194a756f121cb9c7fe4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67443752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb71088db9a7220d9275d6298c7f989f4f4f3c63ceabdd6ba3bc964e65a0884f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:12:48 GMT
ADD file:ba00d13bcd1098159b17d28658733d14360751081a0ff0ae5e599ea2b24d8bfb in / 
# Tue, 01 Mar 2022 02:12:49 GMT
CMD ["bash"]
# Wed, 16 Mar 2022 17:33:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Mar 2022 17:33:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Mar 2022 17:33:58 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Mar 2022 17:34:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Mar 2022 17:34:08 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4e0d8da139e3fe03100d4937bc5abe5a82000a26ba213987f21c101384e663b3`  
		Last Modified: Tue, 01 Mar 2022 02:18:16 GMT  
		Size: 55.8 MB (55764122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ba073f9c99fafb52d85f435728c19483f2ca415b229a7d06cf3b2a108ad37c`  
		Last Modified: Wed, 16 Mar 2022 17:38:01 GMT  
		Size: 11.4 MB (11366370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739d10dbf3eb576234d4f0096d5a2216df28a86820015543be0b81d47853690`  
		Last Modified: Wed, 16 Mar 2022 17:38:00 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4c2c7f7324d57728863c3b637814cfee8d3f10ff9aeb7ea5db512db518978f`  
		Last Modified: Wed, 16 Mar 2022 17:38:00 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99d21c0ee25999922d7fe8fd61945e9b3cfa2d352cd3351174b2d643fe2a035`  
		Last Modified: Wed, 16 Mar 2022 17:38:00 GMT  
		Size: 310.9 KB (310877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d3deae9143a11babd573d3cb9f1a65205f7aa6a5bd3a761546e9059562456d`  
		Last Modified: Wed, 16 Mar 2022 17:38:11 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:37a70a1d18f74cc00a14aefd2e6f2fff9afd2b8d7e26ea63252422b95e77286f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:d3f45dffd49a2b162a4e01edaa391cac11585ef1570f877d83cbc7c39c9d5c58
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66519150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9956cb29636d21fc4de6593382fe3a75f61eb7e8811d2145baab1c230630a2a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:20:32 GMT
ADD file:22ed184e421fcac775f322850c24589ef2e78ddd12900395d44b2ea74220a62e in / 
# Wed, 12 May 2021 01:20:33 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:15:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:15:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 12 May 2021 08:15:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 12 May 2021 08:15:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ad4592a9cb6deb788f794c7bc60f66d77280e79869f13e9eccbf34e1d381b95d`  
		Last Modified: Wed, 12 May 2021 01:26:05 GMT  
		Size: 54.9 MB (54897696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8542129608a42399bc292c1994a3f2340d165d1040e98a2bf563841e5a3eebb2`  
		Last Modified: Wed, 12 May 2021 08:18:00 GMT  
		Size: 11.3 MB (11308850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f358d6314ea033af895f5aebc4724359a9aa401aa672cc401d584a2465387aac`  
		Last Modified: Wed, 12 May 2021 08:17:58 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e876a28d30789565f8fb5724aa6186e85e0ec5d722e4e45ad3d6ea02b2cb4fc8`  
		Last Modified: Wed, 12 May 2021 08:17:58 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bab1c0263bda33d4f321fe0ed47941aa2373f4d0a6068478b03cf7f78d9820c`  
		Last Modified: Wed, 12 May 2021 08:17:59 GMT  
		Size: 310.6 KB (310594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

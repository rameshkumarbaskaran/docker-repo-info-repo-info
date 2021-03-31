## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:5747f903b3a421c43827f70d344d8c63286e030be4439bc452512c777b2e0f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:620416ac688bbef5b8056a4be5c71f76277aabd68e2e877f15c302d5007e1f9f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66485986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dc6c78c8d8afc283868d906e7ade907fdab152a3b76b8e8eecbf1b360a0655`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:48:53 GMT
ADD file:32519b03930d9f5db9010ae49e0987322ce19eab681ad5c841fe1cd6268ad2ee in / 
# Tue, 30 Mar 2021 21:48:53 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:56:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:56:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 31 Mar 2021 04:56:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 31 Mar 2021 04:56:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:56:32 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:6abc78d8e2422868f293b265b6c0ec3ba250fc4987f862ba05e86d7eb277f297`  
		Last Modified: Tue, 30 Mar 2021 21:52:53 GMT  
		Size: 54.9 MB (54868089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bafeca3921579692f476a4e086d485751b94a07e25f3f209209353d2e99ef18`  
		Last Modified: Wed, 31 Mar 2021 04:59:01 GMT  
		Size: 11.3 MB (11304891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09918939546c1b6de78816e9a788e82e4958f2679266d185fe465e221bd50213`  
		Last Modified: Wed, 31 Mar 2021 04:58:59 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fcdb9fee69fe1520dc3eec18074cb4f16217d364a51d15ac2d91cdca689d81`  
		Last Modified: Wed, 31 Mar 2021 04:58:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6c81d608fd57565446be253aa4c55a991be2ad9f4369b4cb71ba8a1a4f33d4`  
		Last Modified: Wed, 31 Mar 2021 04:59:00 GMT  
		Size: 310.6 KB (310628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a5802fa100dd40c896de02ce18c4e7e304d0f2f9df9d9c13a1c72afa17d2e5`  
		Last Modified: Wed, 31 Mar 2021 04:59:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

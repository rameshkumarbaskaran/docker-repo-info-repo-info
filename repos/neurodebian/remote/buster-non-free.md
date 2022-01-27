## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:4550deaf273b8e00b63335d8d0939778d91569322b1e14f208a75d4a3b1f5953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fe51e8cafbb753f08e1e12d092acbc47657c945da1ca50725f60624b07108349
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136af7a7029b209f1ad93eee7e43246c0f2f2e48e9c578682ab20a72e54af02f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:47 GMT
ADD file:a290acee3581e1e9c42c0a37b53086a8f070cb0730179be81a6ba24a620b6ee4 in / 
# Wed, 26 Jan 2022 01:40:47 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 01:02:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 01:02:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 27 Jan 2022 01:02:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 27 Jan 2022 01:03:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 01:03:10 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:a024302f8a017855dd20a107ace079dd543c4bdfa8e7c11472771babbe298d2b`  
		Last Modified: Wed, 26 Jan 2022 01:47:01 GMT  
		Size: 50.4 MB (50437057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1017dbf9d1760e937b19a30b78bfdf3d8449115e6d5fab4e66caa6208c979e`  
		Last Modified: Thu, 27 Jan 2022 01:06:28 GMT  
		Size: 10.5 MB (10500057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02035a90c3fd37530f987acbab2c1815baf5f072f04febac4a5fe14799976d`  
		Last Modified: Thu, 27 Jan 2022 01:06:27 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7928504ffaba82ff43ad02ed0eb4ee89905d0ecab1ffdcbdc4ef1c310c25539`  
		Last Modified: Thu, 27 Jan 2022 01:06:26 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b37d078c5fd37d48fea49816588678698649c49103aef01f40ccb95e7e307ec`  
		Last Modified: Thu, 27 Jan 2022 01:06:27 GMT  
		Size: 302.8 KB (302772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c63c97674ff88535950afcf7aafab912dd143459c2e004150c9f8e7f68db7f`  
		Last Modified: Thu, 27 Jan 2022 01:06:39 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

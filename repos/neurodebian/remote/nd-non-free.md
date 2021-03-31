## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:f9581f93227b085addcab000471c344dd792772c6b12363274ac16576e61382c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:0295f71354738d6536a158f9597bf70d850e51bf09a96831f0cad245213ed81f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66486761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d050362b1e3aa42afda754a7bad1bfc547987b8a88a5899fce9441e08cec3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:01 GMT
ADD file:3d2836abb42f177ad29a584ba02ccc6421b1613f73325823603fc98578f17445 in / 
# Tue, 30 Mar 2021 21:50:02 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:56:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:56:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 31 Mar 2021 04:56:49 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 31 Mar 2021 04:56:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 04:56:59 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:ff28f9110f9a07cc7303cdae0cac6dceebc733170af8336bff099af5e4b0eed1`  
		Last Modified: Tue, 30 Mar 2021 21:55:15 GMT  
		Size: 54.9 MB (54868057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34cb2ddb0fe0a74660e9f3fe6928d0575e77545d99ce6d3238e8742880af26a`  
		Last Modified: Wed, 31 Mar 2021 04:59:27 GMT  
		Size: 11.3 MB (11305744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f08a806c354456b560105ebf5abbf074d99958301365df7c784b97d14dfe9f9`  
		Last Modified: Wed, 31 Mar 2021 04:59:24 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcff0a43a8c33c1dfbd25a118b0f63bd2d6cf7538ec5970b83ecdb5a3a9ddaa`  
		Last Modified: Wed, 31 Mar 2021 04:59:24 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af6e1c6fb7a3c7b9ddf80c2c2009f855ffecd611960f2c8d4734c57ecd05d56`  
		Last Modified: Wed, 31 Mar 2021 04:59:24 GMT  
		Size: 310.6 KB (310637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51ab9e59fa440ca65d18f0f9a2015467b9c99e6da2e1774a8a5672ce44ccb56`  
		Last Modified: Wed, 31 Mar 2021 04:59:37 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

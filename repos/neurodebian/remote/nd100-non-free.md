## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:7c92555e3452f649b78879166b3176586b024ee9112b7f9465fa9bab34293e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:12d754d053efb01a8f3821efcda5ef87ab2817c2ab0a414bbf43b78b2bd0f506
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61247420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24ad930a1901bf048da14116fb442008e84998baa424b3732af254f69197e77`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:12:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:12:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 02 Aug 2022 05:12:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 02 Aug 2022 05:12:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:12:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2428f3c65b4a0857e83e44b4676bf3e39ec809c668bd704bddce68ec61b52e10`  
		Last Modified: Tue, 02 Aug 2022 05:15:29 GMT  
		Size: 10.5 MB (10501149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f82e6ddb6850cb6466874c09e979636970a533963f80ef795d0e0e06c51301`  
		Last Modified: Tue, 02 Aug 2022 05:15:28 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2431945ab713dc20f6853944c00b260f4ad6b9ae568724f05db0320f91733e`  
		Last Modified: Tue, 02 Aug 2022 05:15:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692a76fa08425884628d0ccb74ee04e9121c6ce4d56fed24e23401b8b14d2bf4`  
		Last Modified: Tue, 02 Aug 2022 05:15:28 GMT  
		Size: 302.9 KB (302925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415a97bfa3b450d3e71dcd53435b13957596b4e21c70ec3edcbb6e3de5f7c11c`  
		Last Modified: Tue, 02 Aug 2022 05:15:38 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:601556c364c99a36c4755e12e45e1e77d13275fb99424f4cb21639d46736836a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59637122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45145cc49520afbfcf3356ce44e38853bd46c74239c501e67dc3348ac7238c5b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:07:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:07:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 02 Aug 2022 04:07:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 02 Aug 2022 04:07:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:08:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ad9175bab50a203372a0e5e18519ece155815088752e2900f451f9dd7792de`  
		Last Modified: Tue, 02 Aug 2022 04:12:21 GMT  
		Size: 10.3 MB (10297208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d527a3912e4982e1d06db4d8b2f3d684833010e1d4cfc16801787b9fed69d31a`  
		Last Modified: Tue, 02 Aug 2022 04:12:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4199933e5d6634a8d460a6099aa3dbadee5483211ddc926a0da379fb5e417c26`  
		Last Modified: Tue, 02 Aug 2022 04:12:18 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9418e61ef8a7313b3cf88c397a2fb0a35dfc117517fa2d0ab5366dd3e54aa80`  
		Last Modified: Tue, 02 Aug 2022 04:12:18 GMT  
		Size: 108.5 KB (108521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6fc2a8b0d927cb6e31155575514ce5721bdb9a7b223b2345c89c414520514a`  
		Last Modified: Tue, 02 Aug 2022 04:12:39 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a3faa589c0f7d2376bd5144f638008ea6554c79dc1fe9d838d0490d5174a5a79
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61984278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6c7186a299849c2aedce736ddefd6128bd7a701454c2782e842de93ef2a5f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:31 GMT
ADD file:a25646092eaa55ba1e77da8bf292a71c17f8f54e6fa7a3cc057a8bd7d2febd63 in / 
# Tue, 02 Aug 2022 00:39:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:18:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:18:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 02 Aug 2022 16:18:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 02 Aug 2022 16:19:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:19:07 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:87423d7294b9d02dc4a6174f8947a28436937897c107e94249f27f8c987b91b5`  
		Last Modified: Tue, 02 Aug 2022 00:45:43 GMT  
		Size: 51.2 MB (51204266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bde8b75add39bff8346a40cf19a696d90f83fc7b4d1e3c035b478656d7034b7`  
		Last Modified: Tue, 02 Aug 2022 16:21:22 GMT  
		Size: 10.7 MB (10669192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8bc885a3a4c2e7820a9531f2e81d8567cae93afa593b55a5463ca3a7ad84eb1`  
		Last Modified: Tue, 02 Aug 2022 16:21:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5107873d404a90d6b95e3407b818195c97a7437da9b1681d920e70b2e94752fc`  
		Last Modified: Tue, 02 Aug 2022 16:21:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b27a5bfa9663386e2233f61f36aafa47682e7e3a82789f89f624d252b95f3db`  
		Last Modified: Tue, 02 Aug 2022 16:21:19 GMT  
		Size: 108.5 KB (108479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3eaeb1d1d2ad5ef4049a1c039e03903213e67bc473c3462ee551e87c96e9587`  
		Last Modified: Tue, 02 Aug 2022 16:21:33 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

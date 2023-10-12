## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:8aab30bb3a6b069354c4b0064001ce687c87fb0cb87f96dd96d4b62533d4c61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:4133b5b6d77a540ca2de79f0a7bca7b0c68c219193164bb435305820858cc2e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64076847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe80a908421046f1e39e1c01017388339535db844e8a0f5195bae8f72ebde7e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:36:29 GMT
ADD file:0301a32b2b2f0af81dd4277b61ab0069818663e8ad39e59dec42f2a74e027eda in / 
# Wed, 11 Oct 2023 18:36:29 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:04:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:04:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 12 Oct 2023 00:04:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 12 Oct 2023 00:04:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3997a52aa0dcbfc5a01686dece23fdbb32f74ea998359451f16034544761414c`  
		Last Modified: Wed, 11 Oct 2023 18:42:29 GMT  
		Size: 49.5 MB (49503645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc64fa2e37f8989a74e99ffb107aad254e7976873443f8a4bd5c99735c327a87`  
		Last Modified: Thu, 12 Oct 2023 00:06:36 GMT  
		Size: 14.3 MB (14287000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11c551cc6c41f9b4547f1e21c0a2dd4e7ab58e7eb543916c529698ec68c2115`  
		Last Modified: Thu, 12 Oct 2023 00:06:34 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1870f67e592e0be20d08c2bf9b688a27ae99d26899b2b7122dcd50d11cfd7b09`  
		Last Modified: Thu, 12 Oct 2023 00:06:34 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2285a1d3c3065086a0887974ed20b67a06b7d10ecbe3c5a53d6a353f776645`  
		Last Modified: Thu, 12 Oct 2023 00:06:34 GMT  
		Size: 284.2 KB (284194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:173008b551278ce730b2a5fb927628155315bcad2903e1933b35a1924e60b311
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63895553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64895a65ed15e20fe3cb3670bdb7458b07b9c880134e662ce3ae1f4b8cb6a23`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:56 GMT
ADD file:c18e09bd64c99d045a504c333efaa05322c76b488039b206edcf75aa2a1a3812 in / 
# Wed, 11 Oct 2023 18:25:57 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:45:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:45:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 11 Oct 2023 22:45:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 11 Oct 2023 22:45:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9d2c869ca968be69328dfec29874eb48a467a69cd422adc8efeb8becda0764bd`  
		Last Modified: Wed, 11 Oct 2023 18:31:12 GMT  
		Size: 49.5 MB (49505948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e844bb225a5a348ff23686694fbf59eaf37068ed24819e02d30c61bec857c081`  
		Last Modified: Wed, 11 Oct 2023 22:47:18 GMT  
		Size: 14.1 MB (14102923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8044ce3ea04c5947d141f918d281ac9008eeacac3f25ad93c15a863417945d9`  
		Last Modified: Wed, 11 Oct 2023 22:47:16 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64155e7810b4ad02035c50e244dc6333dbe0d31f00bfd84e224b6be053441b5b`  
		Last Modified: Wed, 11 Oct 2023 22:47:16 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ede91c5e4d86e0c7fa3ba7728a20d98e6f941def37db7cdd07f5740a5156cf`  
		Last Modified: Wed, 11 Oct 2023 22:47:17 GMT  
		Size: 284.7 KB (284674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:491b9c8b3d7cd2efa9f041674dd484f6be2f69df48e454947df8afab99b97a4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65459826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22815772247b79196b081fdc3b1ea9f78efae6682beaaa918fc8ebd86ba4fea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:43:36 GMT
ADD file:89a1cfdf26e23095cc168a8c054aaa8afe0cb7f1b748f0dbca755e9aad935ce8 in / 
# Wed, 20 Sep 2023 00:43:37 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:51:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:51:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 20 Sep 2023 15:51:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 20 Sep 2023 15:51:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a77a25e288eca9c35f0aeada81ba65e2f4beb3d0b739a139eb41bdd87309a97b`  
		Last Modified: Wed, 20 Sep 2023 00:50:06 GMT  
		Size: 50.5 MB (50483129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00716f16669fbde1a6927877c8b01a86fadde4dba1fa729c70c2201e14dead39`  
		Last Modified: Wed, 20 Sep 2023 15:52:53 GMT  
		Size: 14.7 MB (14690576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142260c4269f1833147ea7d89316ff0d7fe446bca322be1c938c8f427b7ecc74`  
		Last Modified: Wed, 20 Sep 2023 15:52:51 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53f904f97cb7220a02a08fa85614a17ea76ee3034d7d80d3128bb31e257435d`  
		Last Modified: Wed, 20 Sep 2023 15:52:51 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba20fbcbd3f269dc55fa471a0d8557fe1660422530efd90bac3726276d870505`  
		Last Modified: Wed, 20 Sep 2023 15:52:51 GMT  
		Size: 284.1 KB (284112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

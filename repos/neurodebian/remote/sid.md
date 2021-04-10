## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:cc851982ad29a1af341581b01babd3b5dbc666b90af572da7afb395812c04d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:19d7040b3f6049f1fa0b490441d4199550b114724add523a0adba54d6f3a72e1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66499982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8db74bed5bde1e7e070231d6d2de8d04be3b24cc10a9afebcd715ebe7dff0c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:57 GMT
ADD file:97b8c276224b2b9407a1635d61780b968f86726642a00f3d49298ab19e9ea714 in / 
# Sat, 10 Apr 2021 01:20:57 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 07:28:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 07:29:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 10 Apr 2021 07:29:02 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 10 Apr 2021 07:29:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9097f35530b77dcae85a27364a3301e3362adb2860367422ed06b99fabe94b8b`  
		Last Modified: Sat, 10 Apr 2021 01:26:23 GMT  
		Size: 54.9 MB (54881626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77d6d8bae74a2d56fa2afde8851164aa68790f5f6a92b8810aa3c09c9ac54e0`  
		Last Modified: Sat, 10 Apr 2021 07:31:26 GMT  
		Size: 11.3 MB (11305700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d9f2062d074519832100c0ce852d4d058c1015b60bc71bd985c5a747743fb6`  
		Last Modified: Sat, 10 Apr 2021 07:31:24 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001d4a1a39739a4e6fe084af81425ba8771de70deb90b919b65c95f1b0ff5632`  
		Last Modified: Sat, 10 Apr 2021 07:31:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19357c6012634f1d029a8f836a779d413b7b750bebfd21201734f19ab27abe9`  
		Last Modified: Sat, 10 Apr 2021 07:31:25 GMT  
		Size: 310.6 KB (310648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

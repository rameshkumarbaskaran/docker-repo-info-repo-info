## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:582f5b7042446f9c97fb26a49a82c0fce2f70c14876717a0a9a7e968d7b4d491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:05e914bd6986b257c0073f50ccd6145e1c36289fd7b040f5bcfe75d975ee429a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67491040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272053735c628a3791522f2d09ee0a3d5f0aab0b9cfcbd2db2343a958a67d7f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:41:58 GMT
ADD file:69369feb027cb9fcd22f8a4b51431458f4e51eca8bb0c398edde4cc47c3d74e0 in / 
# Wed, 26 Jan 2022 01:41:58 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 01:04:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 01:05:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 27 Jan 2022 01:05:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 27 Jan 2022 01:05:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48c02bc8c594d3500557aad8d76d43fb3cd9632de373f64648f0523fd33f3197`  
		Last Modified: Wed, 26 Jan 2022 01:49:14 GMT  
		Size: 55.8 MB (55811672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3940685bf052c45b1d0982dcf21afb435ae0055ab618b4a6486641ca52f9d9df`  
		Last Modified: Thu, 27 Jan 2022 01:07:26 GMT  
		Size: 11.4 MB (11366367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e955b7208a98413d21625dd1215479fa729c36c9adce35fd047d33bd0e4b05af`  
		Last Modified: Thu, 27 Jan 2022 01:07:22 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f70668e9c2f6f63b81590f738cbe0cad34243a51a9d3fe4f40ccf52503bd51c`  
		Last Modified: Thu, 27 Jan 2022 01:07:22 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529a7204f66ddfea4f14473d78eb3c493793ddb370127c8ec970ed80ab52f39b`  
		Last Modified: Thu, 27 Jan 2022 01:07:22 GMT  
		Size: 311.0 KB (310996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

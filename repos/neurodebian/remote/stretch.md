## `neurodebian:stretch`

```console
$ docker pull neurodebian@sha256:98335033d97d4431ce117669670fd5324e4033ab8d0d93be2a004fd5a6c3a8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:stretch` - linux; amd64

```console
$ docker pull neurodebian@sha256:268df378de3d5c7460bc4fef4a2217f9b6a0625baa15aa90123b2f5265ad549c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52249429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4836ff15fe2646febe8de2c3abe217b3865ca832287d22fc8ab1148080f594a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:44 GMT
ADD file:8486e54cd9c7f48cd93b4dc399b71f2053aa61655dcc37e06a9274d4878408a1 in / 
# Wed, 26 Jan 2022 01:42:44 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 01:01:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 01:01:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 27 Jan 2022 01:01:58 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 27 Jan 2022 01:02:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a834d7c95167a3e129adb00a5ddbaf5d3c035ad748ff7ee1273373d150457820`  
		Last Modified: Wed, 26 Jan 2022 01:50:37 GMT  
		Size: 45.4 MB (45381397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2018cc0a54fd2233f26650c8d5702280498b060c573d39e736e77008d9b99281`  
		Last Modified: Thu, 27 Jan 2022 01:06:06 GMT  
		Size: 6.6 MB (6572362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bb5a8587932858fd444c32745a22fbfab4dee9de843d9ed42a3d02bfda1df6`  
		Last Modified: Thu, 27 Jan 2022 01:06:05 GMT  
		Size: 3.2 KB (3158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6b3777b48f3fca8c8aad09ba83b0cfab642827b896195e72039e10ebfc8ba2`  
		Last Modified: Thu, 27 Jan 2022 01:06:05 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb87d7121c48c180132946b41e7bdd0cb82af9ac624df4f55dad29adf4e7efd`  
		Last Modified: Thu, 27 Jan 2022 01:06:05 GMT  
		Size: 292.3 KB (292268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

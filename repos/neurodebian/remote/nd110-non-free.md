## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:e8438a5f58872cddcf8cdf796a51d85a2922b2b4bd91fbf05083c1d923ec92a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:35228b70c9e01b6a1bcbbf4cdba9c284425691bed446e5a297f516c65b9f69c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66550675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa33da3a1d4edbf8142248649fbc317ff995739ebaaa95e7d8d5176a354418a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:25 GMT
ADD file:d05a14b1e57f9cc8eeb316a843403bbb35176d6222d60d6ddbb34faba977e316 in / 
# Tue, 28 Sep 2021 01:22:25 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:22:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 08:22:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 28 Sep 2021 08:22:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 28 Sep 2021 08:22:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 08:22:42 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:df5590a8898bedd76f02205dc8caa5cc9863267dbcd8aac038bcd212688c1cc7`  
		Last Modified: Tue, 28 Sep 2021 01:28:33 GMT  
		Size: 54.9 MB (54927682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aeb24bb1a1628ca7195bcc91c3d61aa9dd181d30373e3a92ff9a7d37315185`  
		Last Modified: Tue, 28 Sep 2021 08:24:47 GMT  
		Size: 11.3 MB (11309442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d325387ff7db9a3948a649aab5bfee497b4ee576f0adcbb896c09d61d8bded`  
		Last Modified: Tue, 28 Sep 2021 08:24:45 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e7c539cddc81a0171b282b15156376ff6d388bef237aae96e9d9108e779f21`  
		Last Modified: Tue, 28 Sep 2021 08:24:45 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a3c441961e9c90ec2498d3f3ed870f5b04db1d32862600b6ef2d2192e01c04`  
		Last Modified: Tue, 28 Sep 2021 08:24:46 GMT  
		Size: 311.2 KB (311178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b5510d862c0626ab068236e6c8fe82d8e188b0be177be9e40fe2db08d24d61`  
		Last Modified: Tue, 28 Sep 2021 08:24:57 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

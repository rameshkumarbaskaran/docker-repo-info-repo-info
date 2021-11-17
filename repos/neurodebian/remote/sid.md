## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:56384ebc94c4a679aa71c13265a9a900153ecda7a5d5a62375f9f0b3e963e961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:e9d0647c0d74120d34a915ad2fab21477180df9ff2ebdb7097dde32acb631fd2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68261104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35bc89d76c8f818dedb4a2a9c8e8383f25f5e62a000c0a89e71b81ebc270eb1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:50 GMT
ADD file:1f62518cec36eb3320e38344c0d36779557214cfce8bc32eda000183a34a0ffa in / 
# Wed, 17 Nov 2021 02:21:51 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:00:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:00:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 17 Nov 2021 03:00:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 17 Nov 2021 03:00:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fef5443775fe054990b02e8f72c4c5bc7792c6a5bf6ef8df110873a81676a87`  
		Last Modified: Wed, 17 Nov 2021 02:28:03 GMT  
		Size: 55.8 MB (55758091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a0228be49855eeddf655d951f1cfe1acefde58feceda49bd546bb45fa8dbd5`  
		Last Modified: Wed, 17 Nov 2021 03:02:15 GMT  
		Size: 12.2 MB (12189635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0597392ceafcb42863396563085b2080c1c35197432577e982787af3005efab7`  
		Last Modified: Wed, 17 Nov 2021 03:02:14 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaf2bd56c7824d0a3e28a2d375375835d7a0274d8bf8dca7e46fc87242207ac`  
		Last Modified: Wed, 17 Nov 2021 03:02:14 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb86a759b386c2385ea488451b9b84246a5392fe931d481bb48758f3ca6df9e5`  
		Last Modified: Wed, 17 Nov 2021 03:02:14 GMT  
		Size: 311.4 KB (311369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:caafdcc9bdbca569653b1df0100877ee6707c59e2d02fd4fc597d3dfe2f2a21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:75f04d8f02c6ab709c98c0e255f5fe8487cf91e00869f68220df1001c09f27af
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68261423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca82665ccbfe47c0ec7b82f6678bb7912a99b041cf720d54c0bc2bf37365c75`
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
# Wed, 17 Nov 2021 03:00:24 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
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
	-	`sha256:1d6a608a57c4fecf88d9ba0bceb84abd24f71eecb2f96f5f5f13284ce1a426fd`  
		Last Modified: Wed, 17 Nov 2021 03:02:25 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

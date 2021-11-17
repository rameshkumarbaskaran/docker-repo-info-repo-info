## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:d62466a413cfed8c3b780dc30a1ea92716521883c8ee105464c213f511aa302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:42a1770c2b3c05dbeb3c289c53893108ec31057882e8abacdccc6af19f092345
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eac918587d491697192bdce80b9be5bea8b26d02115dc32049791cbc8c86d06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:51 GMT
ADD file:cb5ed7070880d4c0177fbe6dd278adb7926e38cd73e6abd582fd8d67e4bbf06c in / 
# Wed, 17 Nov 2021 02:20:51 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:59:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:59:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 17 Nov 2021 02:59:23 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 17 Nov 2021 02:59:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:59:34 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:1230f17f526cb07307d41462355b10488b994e8bdafe0d8f275a405fa3b33831`  
		Last Modified: Wed, 17 Nov 2021 02:26:06 GMT  
		Size: 50.4 MB (50437098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538c3b9fbc8447be794689def3e35170b0f30c917d7b05d6cd83f57c0b0cf1cc`  
		Last Modified: Wed, 17 Nov 2021 03:01:29 GMT  
		Size: 10.5 MB (10499937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c97a8f77cdee3e02c42692c952126646c70fa1e5ad00f5a258b7dd532d63cf`  
		Last Modified: Wed, 17 Nov 2021 03:01:28 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589b7378494749d16a0da792ed131c8fba6c9f9d0f8d22f29a3e51dff93c3f42`  
		Last Modified: Wed, 17 Nov 2021 03:01:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21ae30c3a25c03324da4ec74478a5c67aa268e0f3a2c3133094cbd65fa456d0`  
		Last Modified: Wed, 17 Nov 2021 03:01:28 GMT  
		Size: 302.7 KB (302745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae18462b5714b5c456aafbb28d5e3cc6ea95079a1b3fcf2938afb03cae5ccab`  
		Last Modified: Wed, 17 Nov 2021 03:01:41 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

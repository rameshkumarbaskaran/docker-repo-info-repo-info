## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:b4d49e7360eb0c2b42ffa98f7d39d5a10678aa8150eda796a5a7f1ab4dd39307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:e2aa73f9f09af2566980b8e495f0b8b62a814d92a8f8ca16eb0aaf20d9067c05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34460051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0452d17a83582c40d2cafd271986a859967fed1c986a0c26f566ea5e2767fb51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:30:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:30:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 08:30:21 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 08:30:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906e0384b0751c689672d93e3a583d0f82f563ac76ed169e1b8c3698e7c1b9ae`  
		Last Modified: Fri, 13 Oct 2023 08:31:33 GMT  
		Size: 3.8 MB (3766206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1965fb1bd982ac95de3cd97df09921e2b37180acca64f9c5e1caeda6fd12d5`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1950979dba938d002077c91ca72ca18a4664cfd04d00f60b1eab5492177c7292`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dbe240e1948f0756efdec7579645345b9d490ccec6616989ab5b75cc57f237`  
		Last Modified: Fri, 13 Oct 2023 08:31:32 GMT  
		Size: 252.7 KB (252718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a79d1953fe207f196ad06744c4c494d2f1626e2ec4433fc5dc3731c13596955d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32387822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13669db7a906a6d32ec74e7122de0dd2db8ba365dcc760349c70dd67919c2955`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:55:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:55:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Oct 2023 02:55:59 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Oct 2023 02:56:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477c9d9fd32f7ed46ec165bfc72630fe971f719e63fdf4324845082dbd1caa79`  
		Last Modified: Fri, 13 Oct 2023 02:57:07 GMT  
		Size: 3.7 MB (3739822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c61a34bfc1eb01fd98e89934398ac55d28f86554556cef06331a761cc6d70e`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d61c0ded99806942b23025d926d8999759a391a63a30c5222665142865bc9b`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17795fbc1348d7ec52019935cb1ffef48e3a4bfb7de209dcba5705b765e8d374`  
		Last Modified: Fri, 13 Oct 2023 02:57:06 GMT  
		Size: 254.0 KB (254049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

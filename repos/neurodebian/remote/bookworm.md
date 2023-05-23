## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:394f8b790cc1481de38ef914b1235da9e0ae71b226f351d3259e2aebb3983c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:baabb08f7f35eece8fe86b5cca134eb909f7605d48b5070fc38ff2584518df2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61307789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47799e2bf3d6bb22f8204885da1e8a33389ad6326faf0f6abdb17224ff07f3e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:19:36 GMT
ADD file:aea4560c39a3a877086fc63afdf218ba3600a05abef7c44563f788e8b60c04ef in / 
# Tue, 23 May 2023 01:19:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:23:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:23:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 23 May 2023 04:23:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 23 May 2023 04:23:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c98dda1b0e97e7fa61fa33cea43f85bb1a36a4f6f65c7b8430cae442b76ece09`  
		Last Modified: Tue, 23 May 2023 01:23:14 GMT  
		Size: 49.3 MB (49301275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33627279e466d7f7d1e2299fc1f1ef0aba016364269114db58eefb5bc4f174fe`  
		Last Modified: Tue, 23 May 2023 04:24:30 GMT  
		Size: 11.7 MB (11719838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc38d23881ba02c585bb2b72b06f955689ebf8e30cce25285d5c6ded4b79550`  
		Last Modified: Tue, 23 May 2023 04:24:29 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179908f928b0af97bceaffff9a265d97bffd58aa45ff6ec4b2b6595b33b7bb3d`  
		Last Modified: Tue, 23 May 2023 04:24:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b52941f1978acefe1f1b3a5493124b6927d21693f82780f76726caab179a1b9`  
		Last Modified: Tue, 23 May 2023 04:24:29 GMT  
		Size: 284.7 KB (284664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:648d84e2d1b843835b3fa399b85eeaf865c48c3be470f229543f63a4c1f56a04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61320411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a9c9e342134ca145b25d98ab14e66f984bda18bcc60e0a0f0141083df122e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:42:54 GMT
ADD file:91184714f613e1768e87fad722350f471376a88cb595664e8e23864ce5d79071 in / 
# Tue, 23 May 2023 00:42:55 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:30:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:30:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 23 May 2023 02:30:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 23 May 2023 02:30:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3485dc61c38c6db2e8092e9f4326fe6c51e867a1841f55346f74ec25847d7401`  
		Last Modified: Tue, 23 May 2023 00:45:14 GMT  
		Size: 49.3 MB (49347785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27205be5ff69de2ea80daf475b7d6782f5bd2c4eff02242061f43eaf6012d24`  
		Last Modified: Tue, 23 May 2023 02:31:39 GMT  
		Size: 11.7 MB (11685619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a91d72189acf1f099b7b4f36d85c03907fb5bacd266f36caa6b04ef2e3fd7fb`  
		Last Modified: Tue, 23 May 2023 02:31:38 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3bb66bd12fcefd327ecdad94e32054fc3501ea2c5f23a797f919ad31b9bc9`  
		Last Modified: Tue, 23 May 2023 02:31:38 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e899ae9f9f58a47c33891e8ef8311f802cbff074ff152ecd2f6fa34be22900d1`  
		Last Modified: Tue, 23 May 2023 02:31:38 GMT  
		Size: 285.0 KB (284995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:a8950e781f0d7e413cb43a35939504243936f723a3362cbfb4579ada1646af1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62752170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0397aab4130cfdd8b1bc6e0c4a66596c8d00e10ba6805e93f72fbdd0f7ea47b7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:00:17 GMT
ADD file:cd02b45138959c7ec7d466eff66efaa68d03b2e72f294b468f08c576643ac084 in / 
# Wed, 03 May 2023 00:00:18 GMT
CMD ["bash"]
# Wed, 03 May 2023 23:17:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:17:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 03 May 2023 23:17:04 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 03 May 2023 23:17:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:028db28caf3d2a0b3bc8b8281c9f370a6ca8a97954f596e2b27e20ebf7f3b578`  
		Last Modified: Wed, 03 May 2023 00:04:07 GMT  
		Size: 50.3 MB (50321827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa3f2ae1595f6575bfc69faed0d539bf88a71f81033a72dd7cd6a6b16533a26`  
		Last Modified: Wed, 03 May 2023 23:18:26 GMT  
		Size: 12.1 MB (12143607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030d5cafe5a4885634636dec550fa431c5d4332902b7fa1e592504eb10cb4698`  
		Last Modified: Wed, 03 May 2023 23:18:24 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc4a181c2202a0f49007cfb365321e0dc3352e79f05f6028e41b534da7b6018`  
		Last Modified: Wed, 03 May 2023 23:18:24 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b687257037f8146aecaffcb99f883d553e938ba2d1635186ff1fde12e64952d8`  
		Last Modified: Wed, 03 May 2023 23:18:24 GMT  
		Size: 284.7 KB (284726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

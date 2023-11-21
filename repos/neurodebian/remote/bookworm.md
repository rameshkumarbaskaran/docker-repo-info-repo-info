## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:e35e1ebda0157d635121200ce782aef2aaf789aa070c229ddba2a563e1188f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:0acf4ccd7979f181031416378268c9d195dcd26fcac771e9c385e8ba18b2e905
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61339049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc12c40eeddd04e825a714126de916daac07b5608eb8c1efd509e1381a6d923d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:02:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa63293c58d7f4eb78806fbcdaa17b9c11e011a9808f35f8829dca9a3db4acbf`  
		Last Modified: Tue, 21 Nov 2023 09:04:21 GMT  
		Size: 11.5 MB (11465318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554e43a2b83503b547ab65b0ba7ae317f4ed53706435f3c741b606251fd24d8e`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2824a0cc551e8a570695ede50032f451cd8096058f66d8ff101a0a5aa3326cd3`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e9b428aeb24a379d8cf654d1d67515d70a9de02494ca42e5aaa9ad715df5d1`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 289.5 KB (289495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fd67eface08324388119bee4f10bb75e9a6619d8217046470a8846f7b65fd55b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61334042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adcc21bc3b5d17a6427aa32b7aa7c2b96fa6a07d76bea9ccf7c7b09a8b7743de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:28:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:28:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 11:28:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 11:28:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35a05b8e97c67453a0a55a42f69b0e567db2d0752c265c7a5c5f219e1855cd0`  
		Last Modified: Wed, 01 Nov 2023 11:30:19 GMT  
		Size: 11.4 MB (11429427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ed9bd84f33819020b7286ee3228a6129c3742dfaaa3bc6fefc6f18622bb024`  
		Last Modified: Wed, 01 Nov 2023 11:30:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9780640c8ae3cecbbd1a655dd9311877765283fbb03b209664e4dbf8117b6e83`  
		Last Modified: Wed, 01 Nov 2023 11:30:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec84b69a62a84a36c9bdb39cb2b2d7586f0912ec40efe2801100ab801f5896f`  
		Last Modified: Wed, 01 Nov 2023 11:30:18 GMT  
		Size: 289.9 KB (289948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:369e44778bbd257e64b5d2bb9debe0e889697c1e5bab81215b1feba527c8487c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62777327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11eebfddc39f59d3ea468a60b211da66a5c1ea8522beeffbc621dcb832e1dae4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:38:46 GMT
ADD file:4043d711d8d7d1a995aed0a6998c96230765f55d4449167107955fe4af2a31db in / 
# Wed, 01 Nov 2023 00:38:47 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 14:11:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Nov 2023 14:11:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Nov 2023 14:11:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:be8d77e28ff21732ba73253b6226e47e4e07ec2cedc803ffd62148df5d7a165b`  
		Last Modified: Wed, 01 Nov 2023 00:43:00 GMT  
		Size: 50.6 MB (50600049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54672849c6fbb653b54ed8563dd39c70f075d13deabdd15a3c0d8b34cf1c5d0f`  
		Last Modified: Wed, 01 Nov 2023 14:13:04 GMT  
		Size: 11.9 MB (11885540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589be2903537d6c97210103968fcff93892f8f70224543c01714513f7262ab60`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e905684323f5f1d0f41fb0502c3f005ba7f99f845da0326c6478eee4b1ef1f`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2d83607efb9119cc84d9c28730d2c4c2028e131ec0a40f7721f13f89351a0a`  
		Last Modified: Wed, 01 Nov 2023 14:13:02 GMT  
		Size: 289.7 KB (289720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

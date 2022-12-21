## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:cfe27c6e4097f96eba82539d13a315a418a5389cd9926c08857693fed090ca4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:a798192f540b21efd22eaf5fb156bbca690ebefe6b916e542390342f504f6445
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62269842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8f7e06a13bc62ec135a888db4e42165c315feb75aefe85fa0ab9a8833c7a93`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:01 GMT
ADD file:5498bb69da6f2fdd15556904d80120042d5bb48f73fc9f20a2d1bd5a908e0017 in / 
# Wed, 21 Dec 2022 01:20:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:46:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:46:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 21 Dec 2022 12:46:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 21 Dec 2022 12:46:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2eed4289b3de645a7af9bc81fe7c50d50a1c7aae044a61e100a676b9e6224267`  
		Last Modified: Wed, 21 Dec 2022 01:23:37 GMT  
		Size: 50.3 MB (50324468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d684c700c928a924acfb8e63cc2f1f221b22a91af904bc43abd82f60759fcd`  
		Last Modified: Wed, 21 Dec 2022 12:48:08 GMT  
		Size: 11.7 MB (11663206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e67ad9a9557d3c9db03000c4d0fd620a4746ed5c3265b654aaaf7ac226e0c`  
		Last Modified: Wed, 21 Dec 2022 12:48:07 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205a85f36b86b874baffa44201da50ee2e552a01cfe699c079f8bf13043b9348`  
		Last Modified: Wed, 21 Dec 2022 12:48:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da8f02c09c3892562652ee798806a76a6863675d50ca287e3df840931fe0707`  
		Last Modified: Wed, 21 Dec 2022 12:48:07 GMT  
		Size: 280.2 KB (280152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c5be881a55403b97f256ef46c296ccd21e5394e6018179811bd35801cf6bd061
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62210602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6fb541bc53492c7bfd98a43ed638bccd8e8bda02308a552d56e7c0c463555d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:39:50 GMT
ADD file:de3ed89259c63b45a553c11db2206a6ca4201bfd264f04890af2c672736c15b4 in / 
# Tue, 06 Dec 2022 01:39:50 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:06:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:06:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 04:06:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 04:07:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d78ccc24e38e1c539440b7f90d65e136bba8366864c2b4a45e3956272709049`  
		Last Modified: Tue, 06 Dec 2022 01:43:02 GMT  
		Size: 50.3 MB (50307715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da1d2c5c78abbf06d9010fd7c00be00e933cf8bb9a9a6ca3ea75916a4d7c7f`  
		Last Modified: Tue, 06 Dec 2022 04:08:51 GMT  
		Size: 11.6 MB (11620429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620697d3a391fff2ec179cf047b34d9c3c017d1179d5e34f93cf09bea4a839b6`  
		Last Modified: Tue, 06 Dec 2022 04:08:49 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255eb1b1c1cb6d5420f4f5b269c5013e04880ae731ce777e2c7867d2a36e9cd3`  
		Last Modified: Tue, 06 Dec 2022 04:08:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b272eb0ad91c8281832a02e75285913e08469432d7053bbb8aadffb8f9940ee1`  
		Last Modified: Tue, 06 Dec 2022 04:08:50 GMT  
		Size: 280.4 KB (280447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:bd84b36a72f321740dd6b562372c3e831331eb7240f592d882facb9e836d0150
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63349687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a7c19c67d0206471aa45df42b71d0428ec74365e57b0c9ea59b6b44dd1c33f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:38:43 GMT
ADD file:f11f9a6e73a1ba42c97eb037cc53f119df6d6b050eaeb10df2ae716f4eabd8bf in / 
# Wed, 21 Dec 2022 01:38:44 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:35:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:35:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 21 Dec 2022 02:35:31 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 21 Dec 2022 02:35:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bce8ae6c08a69b30b85b1e939b782fc4dee31791e21ed3abbf56d1ec1dde0381`  
		Last Modified: Wed, 21 Dec 2022 01:43:40 GMT  
		Size: 51.4 MB (51363529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731a3936d5c3e3fabf78ed8dcd67354c86b32b5d07ecffb1b5b7fa096e8498be`  
		Last Modified: Wed, 21 Dec 2022 02:37:42 GMT  
		Size: 11.9 MB (11892514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3a0ab91c86ade96a325852c7e36e65aa3ba3e48bdeaa11f860435d179da130`  
		Last Modified: Wed, 21 Dec 2022 02:37:41 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff654b887ee0a812a6e1f448a6c38ee3cec9ba594df8c2df7f5111ac56e1aaca`  
		Last Modified: Wed, 21 Dec 2022 02:37:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1a95849452ddc55f1e591df86d4f1248a78afe557bc4440a0649fe5f711bfa`  
		Last Modified: Wed, 21 Dec 2022 02:37:41 GMT  
		Size: 91.7 KB (91652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

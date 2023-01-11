## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:17eea4385ffe5b7a0d79381c4d47a2376423e2f573878e95f9eb4afdf606857d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:befb8919c13b7ec3de363cec0dcc7cb03daa68ca34203dc0b9e5d133b6dca707
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62270203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf47ff996a38db1fa2f78e0f2f824090741a185518697cceb919b708f9d8eecf`
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
# Wed, 21 Dec 2022 12:46:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
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
	-	`sha256:09762e7fecfe7a19979ce2d944009784f86b4dec81a409aad54781f0f197a7fb`  
		Last Modified: Wed, 21 Dec 2022 12:48:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:71bd70132c583e3c9d69be5cc19b4336ad65af67bb2a9534ea2ee0caf4601b0d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62054375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7fb41b1bc09092046ca09527570297037c7483a843a45874d4e1f05b1223f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:06 GMT
ADD file:c43d870f9cc5c78ae2b5929a9b3ff0e3b1f78609ed1778045e9ce2cf6c85b0c9 in / 
# Wed, 11 Jan 2023 02:57:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 05:50:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 05:50:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 11 Jan 2023 05:50:31 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 11 Jan 2023 05:50:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 05:50:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:464937bea8f251db8aac33b1f72ddb6cd41283ccba5ec3cce468797a236e3411`  
		Last Modified: Wed, 11 Jan 2023 03:00:25 GMT  
		Size: 50.2 MB (50161611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8e665498128e42bf7359421cb63c35383524e03f11c853a0f5780f35039514`  
		Last Modified: Wed, 11 Jan 2023 05:52:17 GMT  
		Size: 11.6 MB (11610245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510903cec25c309e574bfa2e2e053e84608f325b7e9a93805c32cf7c918b35d1`  
		Last Modified: Wed, 11 Jan 2023 05:52:16 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dd6e69d2772ecf35b3d9733fa901d0af76e798a9ba96ffc1803519eda65f73`  
		Last Modified: Wed, 11 Jan 2023 05:52:16 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8777944b477dad3ce51e27e1ad6b1e421fc811b7e0fc9d4904e0eac51e87a4`  
		Last Modified: Wed, 11 Jan 2023 05:52:16 GMT  
		Size: 280.1 KB (280149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875cede3e22f237807487765aa19efd5ba23f6a693b78505aecdd18c04794ae4`  
		Last Modified: Wed, 11 Jan 2023 05:52:24 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:5f0cfd75b4080bbccb71fd62cbdda8e0786e7ed675e70b73aca36df2873f5634
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63120734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba48064f8138f9f9b40809c840ca5feeb7e90cdc8364db66b7a8d0db5034b7e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 03:15:25 GMT
ADD file:06e348f9dbb5c60f5fd91cd10d8ee7ea08880c456ebafe9abda4790022b4df0b in / 
# Wed, 11 Jan 2023 03:15:26 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 06:00:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:00:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 11 Jan 2023 06:00:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 11 Jan 2023 06:00:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:01:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:a47c0f7cbd17d33fb9f2b6cf8675588aebc0fec7ed1b046061cdf73f126e59e5`  
		Last Modified: Wed, 11 Jan 2023 03:20:53 GMT  
		Size: 51.1 MB (51145053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f7adf71c7d12beadb4f73118d1a9154e4a626abe28d7e0a86965f8cd4df054`  
		Last Modified: Wed, 11 Jan 2023 06:02:58 GMT  
		Size: 11.9 MB (11881718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6428899d9968ba999c70ae0a40bb4287a97552759f4fefddb39cb68321543652`  
		Last Modified: Wed, 11 Jan 2023 06:02:57 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d212f2c587af8cab0abbcee7079d9ca1ffd6b963e7beb091ffa3c298fb3b83`  
		Last Modified: Wed, 11 Jan 2023 06:02:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a070ade3356d1acb869157e4801b344e1da37e24a42b5fb422354663c2e9cd85`  
		Last Modified: Wed, 11 Jan 2023 06:02:56 GMT  
		Size: 91.6 KB (91616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab08dfe2ded6b45f8f13267a691cf58c91b16b9fa6c46d64686750f72acbe30`  
		Last Modified: Wed, 11 Jan 2023 06:03:07 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

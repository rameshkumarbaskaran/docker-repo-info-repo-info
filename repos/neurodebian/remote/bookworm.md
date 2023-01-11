## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:562407e6d62232f1204337234c00a1e215b3bfe125ef6a339848b2dd3f0b905c
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
$ docker pull neurodebian@sha256:901665068d74e9ca8f79d178b920f1eaba5d169748a915e233d658c2ac52d831
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62054016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebab6c933ea5fd939bfcf0140308fb33911ee51a4f0f398ec424b36e0b4ab353`
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

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:2fb67d1da78891eb8055232478711bf209cf4a3e0a4d80a8bf5163082d50d1d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63120374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3b928e4d79a1317735be6c8ef98ac623cbce145d3dd488301788eda273bd8b`
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

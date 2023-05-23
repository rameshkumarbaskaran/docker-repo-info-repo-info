## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:26a60912afb8054dd8f7c7fe44937a0bdaec3c707cdb598b2f1999e97df37ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:44806c8d2020d66ae467d0812cde42ad45fddb5e0a8ff7b427793a23d6a447b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7823c1a9101821c016ca63cf774e6a8ccd0cc61aa8d9a1099d7a61f8b7e71f0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:22:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:22:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 23 May 2023 04:22:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 23 May 2023 04:22:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:22:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af5580aa8b086cc8c6dc3c839df2b54e92d4785fc4e9b824c0da7819479aa00`  
		Last Modified: Tue, 23 May 2023 04:23:53 GMT  
		Size: 10.5 MB (10504489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fae9d7e648f7f5be8b0df37a4284949621932cbe6f4f3ad8a51c76867b82d1`  
		Last Modified: Tue, 23 May 2023 04:23:52 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09094d5b9484661a6878ceaf9f02e2d901afebadcdb601e0deb31411ce74c26`  
		Last Modified: Tue, 23 May 2023 04:23:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee599431be61d0a5ed744c9cb86ef6b4d02c23e602e36f5a2ac021111dca7ca`  
		Last Modified: Tue, 23 May 2023 04:23:53 GMT  
		Size: 304.5 KB (304451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dd539f4479d039165c3dd5ad7548b8840bfb1e87810c63a90fd25f2c4cc371`  
		Last Modified: Tue, 23 May 2023 04:24:01 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d1d384571538549ef9e73096923d7672000b32b10260d4d105c910338942bcbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60055480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826fc2babca4e62a146037fa97738c0993582f625ae3657fc35c11f46f10fd4d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:21 GMT
ADD file:a5100e7ed3c2665c1b4dfbb32eb2b47b85783f2a6800e0ae9004db0ce021dfa5 in / 
# Tue, 23 May 2023 00:43:22 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:29:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:29:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 23 May 2023 02:29:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 23 May 2023 02:29:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:29:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:5ea482247e9a0d1ae4ed218fb0828063b9cce53822e64fd4621f587ab85a7e6d`  
		Last Modified: Tue, 23 May 2023 00:46:24 GMT  
		Size: 49.2 MB (49238292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3669f12602d08f0dbf725c5e531299324f34d80aa1333c05e17213b09f9b4f82`  
		Last Modified: Tue, 23 May 2023 02:31:02 GMT  
		Size: 10.5 MB (10510471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35875484f4c75482356db7b88ff96956756ca2ddf9fcf0db615fa7fac9e6795`  
		Last Modified: Tue, 23 May 2023 02:31:01 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dad3d877033dd23fd3219c87d8586351dbe14d7ab3c9fe9c25296df7bbb2901`  
		Last Modified: Tue, 23 May 2023 02:31:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1424958f76e02c936033580d62bee2972bde5e1f1a8b6d5c0a8781046a3b37`  
		Last Modified: Tue, 23 May 2023 02:31:01 GMT  
		Size: 304.4 KB (304350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5600a1971a0e2142139cffffa014177321f94569310c622a4f530cc99eee5a72`  
		Last Modified: Tue, 23 May 2023 02:31:10 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b565467f94285936ab3a8d8d852cccba66345b8f508d33946bc4e40011ee2e8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62380998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c27bc0c72ef518da8e561f830d119f105da8970c80685b386314fc6d01a045`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:01:10 GMT
ADD file:d427d53c0d42e21426b53d60a17dd7014d2504084ae758c35f088cee043ff9ed in / 
# Wed, 03 May 2023 00:01:11 GMT
CMD ["bash"]
# Wed, 03 May 2023 23:16:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:16:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 03 May 2023 23:16:28 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 03 May 2023 23:16:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:16:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:cc3c764404274f8a6e2edf459bc863892205283aa5069a204e16cce54455cb83`  
		Last Modified: Wed, 03 May 2023 00:05:33 GMT  
		Size: 51.2 MB (51206158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43844ba53e304f4440b1717d17b7f4739ebd73aaea1b850a3697ccb354ca152b`  
		Last Modified: Wed, 03 May 2023 23:17:48 GMT  
		Size: 10.9 MB (10868216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2599c7f3672a192bf65ce0684c0be96a9a476901c4f5a1f5fdad43d3f14250`  
		Last Modified: Wed, 03 May 2023 23:17:47 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e99eacf5db7dc7bf3ebc61365890bf33ee0892276ba2c0681514f7e6e457792`  
		Last Modified: Wed, 03 May 2023 23:17:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ca39efb9f207d4de5ab6495531fa5fbc3cfe9d73d19ccc4ca83e73a7d29e6f`  
		Last Modified: Wed, 03 May 2023 23:17:47 GMT  
		Size: 304.3 KB (304255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eca7e12a39acbba25b91d9cdab41e4c34f117c2ab0c4843b97340a0ddb97e1e`  
		Last Modified: Wed, 03 May 2023 23:17:56 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

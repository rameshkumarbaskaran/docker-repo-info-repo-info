## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:ea2b90a2cbf040d8663822788ba4b22fd6451f7e0d1246e83d74c1318be278b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e466f7dbd3de62a843682246318539d8d8cc23653a253008887805e8cc76d3c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64687104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81848706649fb2dbee852abdf0bb3057a7a91e27e1a07658c87cf4fa3cf53e79`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:57:16 GMT
ADD file:7b7161ef988532de9a1ae3caee50f4337a445cd5d88bfe1da455ad45111e2a4f in / 
# Tue, 13 Sep 2022 00:57:17 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:43:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:43:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 13 Sep 2022 13:43:28 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 13 Sep 2022 13:43:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:43:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:fbb5199f866b772d7999f8d0fead2c513b95972d6d32ec2c8e29311458f0855f`  
		Last Modified: Tue, 13 Sep 2022 01:02:12 GMT  
		Size: 52.6 MB (52643556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fdfaa6048bb74e484185c6a2954a2edc5c86707c9e5ec0ee4a78c9fee115d3`  
		Last Modified: Tue, 13 Sep 2022 13:46:01 GMT  
		Size: 11.8 MB (11756683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f92f815ffb1fd449d2870306889921b418cf343bec3f203c29bbb28e4b117c`  
		Last Modified: Tue, 13 Sep 2022 13:46:00 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6369fb38d66c84bf934264cf2fcfd92ffaee5934d4ac2465e27163e3faa1eaa2`  
		Last Modified: Tue, 13 Sep 2022 13:45:59 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb375eef344b1f9e5aa7f70e064e12273ee09fd30619de99b643554fa27a606a`  
		Last Modified: Tue, 13 Sep 2022 13:46:00 GMT  
		Size: 284.5 KB (284457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499a48c8db15a545445a4000ae198f80bbb6f557316d43fe2e7bee4b154257a`  
		Last Modified: Tue, 13 Sep 2022 13:46:12 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:47635762f344317598dce2e4bb4b293c55808ffcf013957b1e17246722503bd8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64332274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60878ab35485605801fe9972a19002148644695e6ace672c1675fc53331a90da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:45:47 GMT
ADD file:28797d8b43689eae5ccab5b01e88b732a5fca655590a0c9f066d6f0a4d880a95 in / 
# Tue, 04 Oct 2022 23:45:48 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:59:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:59:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 05 Oct 2022 03:59:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 05 Oct 2022 03:59:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:59:55 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:6499ab100dbfb0305e0d96b62f7ad515906275ab30864ac686f0af8ff2fdd114`  
		Last Modified: Tue, 04 Oct 2022 23:52:17 GMT  
		Size: 52.7 MB (52699991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df1adfecab1461b8bd99768350d329ebd6e7b7f5e62880f44688fa052d81ee5`  
		Last Modified: Wed, 05 Oct 2022 04:03:49 GMT  
		Size: 11.5 MB (11532459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211df1c3633aa1661947564b9ed3696aa1124f6f50b0f8f3b5955b1375b7edc9`  
		Last Modified: Wed, 05 Oct 2022 04:03:47 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae2e7a8e83e699919e6d0b01c2018d0aa2bab3c68163dd11674788e3045521d`  
		Last Modified: Wed, 05 Oct 2022 04:03:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c48121c4388703126d8476e2c0db10a4f0e3fe3b6cf4b0c6c837990718ec487`  
		Last Modified: Wed, 05 Oct 2022 04:03:47 GMT  
		Size: 97.4 KB (97449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a122987277c618f99d8e9797c12f5554f3e292599645081a8d40ceb2a5e6f6`  
		Last Modified: Wed, 05 Oct 2022 04:04:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a425770283cda772573807278c0b8b6f038f76ca2dd620354fe49d4ae381080e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65739361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0b187a067e370c9357a6f1f6a7eefc3e0ed25daf17f316e3b9b537ba736c3e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:40:48 GMT
ADD file:ea6d247c762f6294c87144d1a4308c30669e9e732bd8ff9ef892c71d14563165 in / 
# Tue, 04 Oct 2022 23:40:49 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:16:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:16:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 05 Oct 2022 02:16:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 05 Oct 2022 02:16:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:16:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8a0d07a7940ebb4ded014cd2eaedc6b9aa8767ff5afeee7b1b09fce7cbd7a31e`  
		Last Modified: Tue, 04 Oct 2022 23:47:29 GMT  
		Size: 53.6 MB (53647464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155ef37d1ca044b99973bac8a03dd842b017b7e1459194239fd83e9dd188597c`  
		Last Modified: Wed, 05 Oct 2022 02:18:16 GMT  
		Size: 12.0 MB (11992190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a7bb9a78d2d85b84ec9ffbfb13e408d286021108c33addfecf65bcc2993839`  
		Last Modified: Wed, 05 Oct 2022 02:18:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994eb0042ba9c275a2f107edab9fd532d71c9a01c5addf5d4966600e9bac59b3`  
		Last Modified: Wed, 05 Oct 2022 02:18:14 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d19a641e13b51478bf8e07a69c870d20f5b6988a813cb8082a4e0636567fa19`  
		Last Modified: Wed, 05 Oct 2022 02:18:15 GMT  
		Size: 97.3 KB (97327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28db70b4bbb814cec277b2bbd389ec555efbbf4fb63b356046e21eca8518708d`  
		Last Modified: Wed, 05 Oct 2022 02:18:26 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

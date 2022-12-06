## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:c6adaf2435cdaa73a68b8d2f96699875c4263fdea350be8402cdbc0e79cd8e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bdfe03cdeeda71223eef013f01330d44befb726694c7f0d4d7bb7bc825b9ce29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62255344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cadd3e12dbc5149955cc6f800cbe73583dd2f1215c04bf204269a3ae5afda05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:52 GMT
ADD file:643fde45a6d11f36b1178a022667e74288e58a263ac7999c7cb023cb3fcde3a8 in / 
# Tue, 06 Dec 2022 01:21:53 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 09:00:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:00:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 09:00:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 09:00:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:00:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:f8db6e5cd5802a750fd04af4eb64a857f779b9c2333d2d830a50d7b2983365c1`  
		Last Modified: Tue, 06 Dec 2022 01:26:42 GMT  
		Size: 50.3 MB (50309617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda33a9cd6f398243ba530ed6334bda146848aa4316787c0930b2daeeb2686ba`  
		Last Modified: Tue, 06 Dec 2022 09:02:03 GMT  
		Size: 11.7 MB (11663180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd69bce09da306b47bc798ee98afd88bb7558f4434f4f88e2b7162560cd89cb1`  
		Last Modified: Tue, 06 Dec 2022 09:02:01 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58013dd6eaf6025ae24d48982e89d252e94782372b25f11f3f9f5f7214893cd0`  
		Last Modified: Tue, 06 Dec 2022 09:02:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65caecbc3d9520528bc570d293912e66cb36948f64d5f480705849e1c514aaa5`  
		Last Modified: Tue, 06 Dec 2022 09:02:02 GMT  
		Size: 280.1 KB (280149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb2fba46a2e68ce1009e054dd8a08c2e4f7e959f356e936fd549200f0db7edd`  
		Last Modified: Tue, 06 Dec 2022 09:02:10 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:612bdf7104a40798afc189b952035aba92177708e85381708e1ad1c218c000bc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62260370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd937e813eae9709bb76589395ffa8b6beb628b88bebc8eccdcb6c3e8cd90619`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:58 GMT
ADD file:465db2e68facfda9a8a0c90d74ca46eaa4c6678539ba23e8b95ed5245b4c014b in / 
# Tue, 06 Dec 2022 01:40:59 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:07:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:07:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 04:07:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 04:07:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:07:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4eadaf994967069fdc4c6fb0c34ba7ff8466eb883bc166d386d6891cfde0d540`  
		Last Modified: Tue, 06 Dec 2022 01:45:23 GMT  
		Size: 50.4 MB (50356726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed6f64ec4652b7c3171c2645831997ab69b35317be6c56a1bb3b4caa4a36bd9`  
		Last Modified: Tue, 06 Dec 2022 04:09:07 GMT  
		Size: 11.6 MB (11620570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e67b31c0d7e5a83a1d975eed64de87d955972ce25a958e31324818cfe53169`  
		Last Modified: Tue, 06 Dec 2022 04:09:06 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd7ec5c16dfa5fc993395782ab3628879ad831177eae3e603b74d413cc749f`  
		Last Modified: Tue, 06 Dec 2022 04:09:06 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7017d11de64ba4289abd26711c68c33abb56ac774ec33a00329020e01d368ed3`  
		Last Modified: Tue, 06 Dec 2022 04:09:06 GMT  
		Size: 280.7 KB (280671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca967002033c47687cbaa4bfe1f29c1e321d17ec211b3134b43bc4a6559774c`  
		Last Modified: Tue, 06 Dec 2022 04:09:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:c519129b55fe548b0549049c680f500011ad1c3a5bf4af55b9082260460e3ef2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63345448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e3d0a005b6aa9dbfd5fd26c3ca8fd132fc8dce8f40db0431c23cd052661711`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:41:02 GMT
ADD file:0909d182d8916b1b37783d0c3582c9d3f3edddf6cd27e90100343ed0462c9c75 in / 
# Tue, 06 Dec 2022 01:41:03 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:37:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:37:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 02:37:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 02:37:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:37:49 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:1cd5a2a4c5902ff854cd1178702a69271f9bf768ae5b99124c16b51e5c2d42a1`  
		Last Modified: Tue, 06 Dec 2022 01:47:24 GMT  
		Size: 51.4 MB (51358972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17be3d1436cd579bc8d98f3ffb1ef3f9cc4be510d995ed78bd2da0a30a663074`  
		Last Modified: Tue, 06 Dec 2022 02:39:41 GMT  
		Size: 11.9 MB (11892469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac792060cfa2b70d317c0d7f7b98db4fa37dc750f3305e1113697b77038ff1be`  
		Last Modified: Tue, 06 Dec 2022 02:39:39 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e1f476e348d11b3764ba14d711514789e329e70dd90031e0dab63582a9bfee`  
		Last Modified: Tue, 06 Dec 2022 02:39:39 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258c3265a6bd1a5b1f37b8643e486a04ec9e684278f6c30cf2abb9d512e464a`  
		Last Modified: Tue, 06 Dec 2022 02:39:39 GMT  
		Size: 91.6 KB (91634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b39f109c62fe38002ec9110ecc9f42c0c096123c0ec98947103e05dc2fe870`  
		Last Modified: Tue, 06 Dec 2022 02:39:50 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

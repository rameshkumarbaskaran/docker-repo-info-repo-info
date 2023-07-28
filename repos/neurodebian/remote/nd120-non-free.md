## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:033ee2b1f314b115b253db652cc3786f3bf294c57f0eb51c816bb8e37d74bbd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:843a4f50a7d3defaa8e25a7d17aadf588f032159488d51c29c9dfe59d70a90dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61309288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5f0fc4fc7c53f26ffebf3e73e6c64e686790e8495ca47337da09342595b927`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:29 GMT
ADD file:cc1376ecb3d9e93e4160573c110da753ffeb2efe2223351f1fbf483d89f1a756 in / 
# Thu, 27 Jul 2023 23:24:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:27:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:27:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 02:27:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 02:27:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:27:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:785ef8b9b236a5f027f33cae77513051704c0538bff455ff5548105c954c3b1c`  
		Last Modified: Thu, 27 Jul 2023 23:29:02 GMT  
		Size: 49.6 MB (49557354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d905e76705ba2d491b7492aeac8117cfc126602ffdd894beef10d25670f950`  
		Last Modified: Fri, 28 Jul 2023 02:29:01 GMT  
		Size: 11.5 MB (11463200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ca86729e5380b14dc0a70aaa4f595b9855028f2e2f47fd27bbc097f34b549d`  
		Last Modified: Fri, 28 Jul 2023 02:29:00 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384259591a12377cbc15f68010e5cf735f5abdef08fbe2dc65b4078d05b8d622`  
		Last Modified: Fri, 28 Jul 2023 02:29:00 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5881885a9820e9520a9da6130dd40d853fb34723d1586cdb81065df36a0152`  
		Last Modified: Fri, 28 Jul 2023 02:29:00 GMT  
		Size: 286.3 KB (286285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5333acc3813ff85d6ad77bd88b32b6ce2a450ee8e75149048528ff91740d3c8`  
		Last Modified: Fri, 28 Jul 2023 02:29:09 GMT  
		Size: 432.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b5d53aa07e1854d196984b33006557c99a1eb4ad853e5a4760d3c3278062f76e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61307364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7539f220e7474b8977399a7149cf4e669652f5452238bb2ce9c2be1467ab01a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:42:51 GMT
ADD file:fa545fc37115e874135945921d2cc72df8dc5b16d4354b2052717c7a57043e0d in / 
# Thu, 27 Jul 2023 23:42:51 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:07:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:07:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 14:07:50 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 14:07:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 14:07:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:fc9ce7290e7e014f69623715ba619a0d3488a7b6ecbf09e55e11160365691192`  
		Last Modified: Thu, 27 Jul 2023 23:45:54 GMT  
		Size: 49.6 MB (49591268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498ddbca5e8ed40f5e0fe438e3c2cb29937ee19d9ec40e1481ea918f21452b7f`  
		Last Modified: Fri, 28 Jul 2023 14:09:16 GMT  
		Size: 11.4 MB (11427029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6677de8b7fc321e9a344c460cac09e7cead96c86f97a9df2900570fbd09e99`  
		Last Modified: Fri, 28 Jul 2023 14:09:15 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15527b837be28e52d6dbf1a2e838e2cbd5e672257fbf9cce2127a51f5778b083`  
		Last Modified: Fri, 28 Jul 2023 14:09:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8febbe9dc7b21296e8963044ea6a2ad1b695da89d7d870917960f961c014c67`  
		Last Modified: Fri, 28 Jul 2023 14:09:15 GMT  
		Size: 286.6 KB (286619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc144652d2a1cb19a47e7f13cd8c3ee5e1154f2b9fe1503d80ea9f789ed9108`  
		Last Modified: Fri, 28 Jul 2023 14:09:24 GMT  
		Size: 432.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e93626359a36a48bcc52dafc8f06c0314f34e2363d5222491aca6992aec03a08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62740074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfc1e630f7cf429a188bd3ae4877ca5fe4084dec8cbdfb63969279c8e6a03e5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:44 GMT
ADD file:bfd1a38bf0df9f79f82223093a7cc153dd7b622ab08d82845c29e6c6a2b63344 in / 
# Thu, 27 Jul 2023 23:38:46 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:7edd5f0eb761ecec3cc6497cb7ea8914684087583488efe885ab62bb56ddb33b`  
		Last Modified: Thu, 27 Jul 2023 23:42:57 GMT  
		Size: 50.6 MB (50567875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d955a37bc16f78384964e9fe3eaea19c7ce73126226143d91ad06904f88f6c`  
		Last Modified: Fri, 28 Jul 2023 00:28:21 GMT  
		Size: 11.9 MB (11883326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bffc2e83e61fafba4c775d5e49f245f6c41fec6fb974344eba3e8413a9efe79`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28982312586fa3fb6b226464fdb7d7012bd3b791fd5861afdf90710edd6eadce`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77d2ebb426ec21ab46e2606841ee798e7cb0ac271b2c9496e806d0796628983`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 286.4 KB (286430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7712c30fa50f50f5023f34c834fc38657c999b4b7016a15b5456d677e8b50d3d`  
		Last Modified: Fri, 28 Jul 2023 00:28:29 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

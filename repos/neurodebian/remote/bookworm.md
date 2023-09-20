## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:d517d492707d6897b36a4a1d05190623768e13a897a905854ffe0002a76eabfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:6c679c6ffa223bae75c084833cbecfc1708fadf4c3d858b61c58259646010eca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61309982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee7b72d12a4a7951cebb2b5cee1c1e173a0045a4ec10ccde32f484ea1b85624`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:26 GMT
ADD file:ce04d6a354feaef93795269c859f36667fce9efda23c61b37d7060263b66ed4e in / 
# Wed, 20 Sep 2023 04:55:26 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 05:57:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 05:57:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 20 Sep 2023 05:57:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 20 Sep 2023 05:57:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:167b8a53ca4504bc6aa3182e336fa96f4ef76875d158c1933d3e2fa19c57e0c3`  
		Last Modified: Wed, 20 Sep 2023 04:59:55 GMT  
		Size: 49.6 MB (49557601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c419a0a1c8188a62c978c93260a8f9485b838e24cdd4b2f909204fe27ab0536`  
		Last Modified: Wed, 20 Sep 2023 05:59:05 GMT  
		Size: 11.5 MB (11463248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a442d8d1d593aebb6ee13cbd20afa90c396ea27d0716a638b5542d5179896ef`  
		Last Modified: Wed, 20 Sep 2023 05:59:03 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e887b385fcf90d26836d084c5116c780426caf59160025b4a549897404dba8`  
		Last Modified: Wed, 20 Sep 2023 05:59:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fdda28a81436332727d65db51a0d0e60eeb821587da5445180971d48b2af1f`  
		Last Modified: Wed, 20 Sep 2023 05:59:04 GMT  
		Size: 287.1 KB (287121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:77d757fba0b24492f0c9201f3a668bb3b33611a79f25bf886ffc101a6ca591e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61306312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb3f6710e3ac277e0bbf52d5277cb3c9e49b91a0e28e5e3b326dd6665d4b39a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:31 GMT
ADD file:f9dd2b1cc0ba261acd8a3e500c54f6b6e0a46131a32988bfd71cf3c6fc5a7d13 in / 
# Thu, 07 Sep 2023 00:39:32 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:34:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:34:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 07 Sep 2023 09:34:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 07 Sep 2023 09:34:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fa34261389f3dee2ecffe9bfe38ae7fd05a1908e98a7486354905aee0f648a6e`  
		Last Modified: Thu, 07 Sep 2023 00:42:39 GMT  
		Size: 49.6 MB (49590783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1416c874d38e794a477cae25f253730bbcbdc5173decc6018f67b0f10b07028b`  
		Last Modified: Thu, 07 Sep 2023 09:35:49 GMT  
		Size: 11.4 MB (11426925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cff783984c16c1d2c63bb7a880692867213838e5db34a585a3d4a74463067e`  
		Last Modified: Thu, 07 Sep 2023 09:35:47 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6517bd8408f9f2a2f6a4a782b8acc937a0a751873d9ed96f60bbd261688d73d7`  
		Last Modified: Thu, 07 Sep 2023 09:35:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40dc72df4937212f4c5bf4361e27182ead34548335baa997db0f5d05e78f2541`  
		Last Modified: Thu, 07 Sep 2023 09:35:47 GMT  
		Size: 286.6 KB (286590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:87f3e7424c54e6550701544e4e9045e831f764229b08c8f792d0873cfe64e635
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62738990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3c8d1c4439200d18a88c1b55d61890c32b2c37d336ad386cf0caa533001824`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:38:49 GMT
ADD file:8f184a190a3b39f8a44c9c20af46dd27ea11f07138459893b113592302f90a40 in / 
# Thu, 07 Sep 2023 00:38:50 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:06:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:06:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 07 Sep 2023 01:06:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 07 Sep 2023 01:06:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:28e9e767fc740145a9fd9e593c7ed9b1ab1ed746324049bf58752d28fa197e5d`  
		Last Modified: Thu, 07 Sep 2023 00:43:21 GMT  
		Size: 50.6 MB (50567259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126f8178f039dcde5b94c5baf1f416aed99bd468dddfef648d7076666f7cbb4f`  
		Last Modified: Thu, 07 Sep 2023 01:08:06 GMT  
		Size: 11.9 MB (11883296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1356286a96b0846f065e50ae2b83533053e39cea782cfec01197c95320634581`  
		Last Modified: Thu, 07 Sep 2023 01:08:04 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a9b23cb2c8f0fbdae7c23049e3870d5aaf7ae1f8a9693ec423335f0649d926`  
		Last Modified: Thu, 07 Sep 2023 01:08:04 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdb8aed3103dc8c360d23a2a95b6a20a7ff20bcbf4fac20b81e7ca8e397ba89`  
		Last Modified: Thu, 07 Sep 2023 01:08:04 GMT  
		Size: 286.4 KB (286420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

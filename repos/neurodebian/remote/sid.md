## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:7c67644bb4903dffbf879fb84b52d4291480730d40f5ad360b2232aaa2f6ecfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:5fe7da4512a60b0d04da2d0b934e3144b590651ef535f1f137a7aae63521eabe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61218765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3d8df3b4f832d39637ae30c01c22c727ef4adef9f5cb69891c3e416104e81e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:21:29 GMT
ADD file:b3a4ee0f0fbf2d8fbbab0aefd91aa4d658c41b09c8a2beea1024bfce5e7d3fca in / 
# Thu, 09 Feb 2023 03:21:30 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:33:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:33:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 09 Feb 2023 10:33:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 09 Feb 2023 10:33:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca2c7deeb5af7aa8a0aa3358218901c07b10bb98573151782e5e7af0ab03009c`  
		Last Modified: Thu, 09 Feb 2023 03:26:46 GMT  
		Size: 49.2 MB (49234515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e8364caf5a58b2deb6126067cb35d010bad611576893cd5016c15f73077ed6`  
		Last Modified: Thu, 09 Feb 2023 10:35:29 GMT  
		Size: 11.7 MB (11700970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d427fbbb2b26c4a76ad11c5aca1a15a6e3a3ce0ebed9bb368ac16aa4b0a201c4`  
		Last Modified: Thu, 09 Feb 2023 10:35:27 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaccf87aac953e023363d8b331021aa3544b998ea3b8a32099f54494bf17268`  
		Last Modified: Thu, 09 Feb 2023 10:35:27 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d98dcb68c6cd5f7564faf602448779dafa9193a157852d3d9b0cb9194ff14a`  
		Last Modified: Thu, 09 Feb 2023 10:35:28 GMT  
		Size: 281.3 KB (281270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f0db5e6bd8da69923738601192e7f57f8d67b6efd7791f02323c4de45c1c7086
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61217072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6946d33497cad621519c391be40182270951049a24ea5e5ab8add41bd72bf91`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:59:27 GMT
ADD file:e092144c3667bd346dc4cb05da5a70ca9f7303d7160f9d5763af88fe51e02f66 in / 
# Thu, 09 Feb 2023 03:59:28 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:52:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:52:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 09 Feb 2023 13:52:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 09 Feb 2023 13:52:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:00f9d2ac5ed56c16a45852afb781f7257c58125a3b154fa75d18141566291f9f`  
		Last Modified: Thu, 09 Feb 2023 04:04:03 GMT  
		Size: 49.3 MB (49272262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9f20c3fcac000f01854d69d6081d6e3f5ff92091ca51aa45a004754e94c9ec`  
		Last Modified: Thu, 09 Feb 2023 13:53:46 GMT  
		Size: 11.7 MB (11661109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa6bd92ad22b90905e44fb6b7585d3e4a847136df396199b48b91e839cb7391`  
		Last Modified: Thu, 09 Feb 2023 13:53:45 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8ff463f96b6c8abe4cf66b07161b9878b2fc9f2fafb0e84e5c42672d372b4b`  
		Last Modified: Thu, 09 Feb 2023 13:53:45 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3233f90943714a3768cdab13885ed0fd8432c1218ec6d4486c430bfffb381a2a`  
		Last Modified: Thu, 09 Feb 2023 13:53:45 GMT  
		Size: 281.7 KB (281698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:455b44b7e0c1d17689080417db8ac9f52f60cd492c355412ffe920270cfddaa2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62312627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedf8b33e399cc416b854b13b947b342c26e5a35866973353a64f6ccc306a737`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 05:14:01 GMT
ADD file:9ac1978405b6f0a95e33d1c34f01be82bbc11fcce2878747e4f688335279964c in / 
# Thu, 09 Feb 2023 05:14:02 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:44:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:44:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 09 Feb 2023 12:44:20 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 09 Feb 2023 12:44:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e58ae2871ac91256d220f3da2b9736b2afb1a06906579876546cfae103647f95`  
		Last Modified: Thu, 09 Feb 2023 05:20:31 GMT  
		Size: 50.3 MB (50285434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2a120090af691fd4e5ade938037157e5d29f3d11e3c3fd540b83e8f5a65011`  
		Last Modified: Thu, 09 Feb 2023 12:46:22 GMT  
		Size: 11.9 MB (11933559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a93706304552ccb0d7cebc8928c9d0832dbd0daca00da28c190209bade85501`  
		Last Modified: Thu, 09 Feb 2023 12:46:21 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7065c687c96091f2284561bb5a43d98da272ed8a551560f9d647cf28c84137b8`  
		Last Modified: Thu, 09 Feb 2023 12:46:21 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe14b41a09e2614c0ecf5a7a46afa8824cb42dd8a5503453498ba712306cc7b8`  
		Last Modified: Thu, 09 Feb 2023 12:46:21 GMT  
		Size: 91.6 KB (91647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bionic`

```console
$ docker pull neurodebian@sha256:96eae7ef2ac965c0998afc444f1df540d2a500df03f057ac103e9c3d7ce2f25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic` - linux; amd64

```console
$ docker pull neurodebian@sha256:11ea2de93ebd8027f28e2398182569570db6a7a982230d5ef8ebd94c61361e32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31774384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6016f10a2a6f59a265ad12cb1b64c73048ae73d05c3912aa093bf021f64dae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:11:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:11:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 25 Oct 2022 04:11:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 25 Oct 2022 04:11:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15baece08727e3929e15ca302a047b8b0f107c3a90360448d8126afaf34243`  
		Last Modified: Tue, 25 Oct 2022 04:15:02 GMT  
		Size: 4.8 MB (4819633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f5148e0a5a4cc92de00f4cc8e1fd27790e7324f700323b517526970b5a720a`  
		Last Modified: Tue, 25 Oct 2022 04:15:01 GMT  
		Size: 1.7 KB (1659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187e93f4ce23bffd0ba0ed9ad07de02f475eab02d245901dbae227d68a95a96`  
		Last Modified: Tue, 25 Oct 2022 04:15:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0515cead5f90c4db393f8c80e0a03f4aee07139b1a740e4993cf32219e784f7`  
		Last Modified: Tue, 25 Oct 2022 04:15:01 GMT  
		Size: 240.3 KB (240345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:19dfbd8c661df6d6618a1dd4937f823cd9d252693c7b09905e24a6bc4f978435
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28377890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31de054b48c4e1ce7aeb954d852b83759468920a286a9fbd1aabf8c442b39bbb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:43 GMT
ADD file:eb8b2914800b2ed866666fbff73c8234f4ac2a5ef01743d6fea0984230c2f464 in / 
# Fri, 09 Dec 2022 01:46:44 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:12:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:12:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 09 Dec 2022 02:12:25 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 09 Dec 2022 02:12:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:87acad9590b042ceb59687d498c396e9344cf2e381923fecd299555966b14975`  
		Last Modified: Fri, 09 Dec 2022 01:47:46 GMT  
		Size: 23.7 MB (23734135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f61184f3a9b790e0a607c824da66bbd248053b5af93a4b06a1af387f90b43b`  
		Last Modified: Fri, 09 Dec 2022 02:15:03 GMT  
		Size: 4.4 MB (4401770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65ede042e70b3755336665612d24bfaa821174317013287abb7d1c5c3ff1acd`  
		Last Modified: Fri, 09 Dec 2022 02:15:02 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82fef820b26b0185647ffd846d0b173c04bfa8fce4607b2dd97572477fcaa45`  
		Last Modified: Fri, 09 Dec 2022 02:15:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa768f88ebd974ae18e34bebba9d6b31fe8de438bd83201bf02787af231ec179`  
		Last Modified: Fri, 09 Dec 2022 02:15:02 GMT  
		Size: 240.1 KB (240077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

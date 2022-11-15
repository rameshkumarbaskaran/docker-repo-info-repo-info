## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:e88c51a64613cb524e372c808f20eef9c7b73a0025c4627c01af1d35ddbdeb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:a1771f97021ae7fd30e809bca80170f8c1d3589102e6ffd6868567f9728c6c9d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63801457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f93735c80b42f80dd22e4e527e4d1355b53458d3aee97532f3a1d996556f035`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:22 GMT
ADD file:3b158c11a921c91aa3cebf5651e59c21fe59da295d3edc56147fefaa760329ff in / 
# Tue, 25 Oct 2022 01:43:23 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:13:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:13:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 25 Oct 2022 04:13:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 25 Oct 2022 04:13:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3721e3e259583b8b78cfdeb51a553c189938925b902bceaa1f4f92e837fb9a23`  
		Last Modified: Tue, 25 Oct 2022 01:46:52 GMT  
		Size: 51.3 MB (51261783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2cb44d0dc9a113af7098ec95ef9e9faffc8fc355c63109604e1fe5b96064ac`  
		Last Modified: Tue, 25 Oct 2022 04:16:44 GMT  
		Size: 12.3 MB (12257021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1b16ed4e1eba9d2fb4083a3ff9284fb6004263f633ee30c00bfa72ec1416ec`  
		Last Modified: Tue, 25 Oct 2022 04:16:43 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03ec2c2e4e4e032f3a29e2f05ba8c64da2eea1461540296f4c44922fd9017ee`  
		Last Modified: Tue, 25 Oct 2022 04:16:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaf90501140d89e5e153eb6670efd67efd132a467cdcba46bf41c9c083e8fb0`  
		Last Modified: Tue, 25 Oct 2022 04:16:43 GMT  
		Size: 280.6 KB (280649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b43dfa6f4ac9a59a4d92336c97608455a30854fb6ee6a8ad7d3cda429d0ddafb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63764681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758cc537d07c9bd0a4529509ea7f13c514e5b7f839e48f3d7ac4936ce81dbe2d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:44 GMT
ADD file:83253dd857c3f1ea456b2b77494a2d865a467a36c188ecaeaf493faa5afb4c1c in / 
# Tue, 25 Oct 2022 05:45:44 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 00:34:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:34:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 26 Oct 2022 00:34:04 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 26 Oct 2022 00:34:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bec7a4c1eec818efa32bedb19eba072edfb65db7384f73efc2a6ee7b13a3ca49`  
		Last Modified: Tue, 25 Oct 2022 05:48:08 GMT  
		Size: 51.3 MB (51263048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1723568161154c8a1c5890e3ce59627ef36108ab8f1b4d99c9b2a2593c7ce12a`  
		Last Modified: Wed, 26 Oct 2022 00:37:23 GMT  
		Size: 12.2 MB (12218453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb9e6308b2c7aa6f129f2c580eea76efca3428e3cca3a11accaff5c5211f3e5`  
		Last Modified: Wed, 26 Oct 2022 00:37:22 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df3151237adde53d2e6f8acf2b356fa4d7efd659cab945b1984170665c6b2ed`  
		Last Modified: Wed, 26 Oct 2022 00:37:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f848c50fe0958198467bb825dd4a463c873a4490fb65ae5270d3e4a0e4c2f6c`  
		Last Modified: Wed, 26 Oct 2022 00:37:22 GMT  
		Size: 281.2 KB (281170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:c1954c157ed8ce9ad6c1f66aef8ba93574a21f27f2d9a00b6cb21014f366f476
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63337600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27d2a2bc2d8a79e213efe337feb9120a9a2535111905344f02e30bb32f9bc45`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:40:45 GMT
ADD file:dc52b19235f576e4601a85df40bbca1bd78982afc56d272746728294ee8a335a in / 
# Tue, 15 Nov 2022 01:40:46 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 09:04:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 09:04:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 15 Nov 2022 09:05:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 15 Nov 2022 09:05:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eed5d6b8bc9dedab6a360f9b58991756d109919cc4cac0c030d7c94377a3a13d`  
		Last Modified: Tue, 15 Nov 2022 01:46:00 GMT  
		Size: 51.3 MB (51344908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542a38d6a9bab854052cfac8c5fcb465ca7ae3de8ab10e26fd147bfc1e2b93a0`  
		Last Modified: Tue, 15 Nov 2022 09:07:10 GMT  
		Size: 11.9 MB (11898839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95807e1b9d5c358fc3f85963894880744f6b8787c9ecf00bf134ea2040bdd7e5`  
		Last Modified: Tue, 15 Nov 2022 09:07:08 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be487eafdc2c6df346301faa3e75d4775e88fc641c4148bad1ee2ac7b479b7f`  
		Last Modified: Tue, 15 Nov 2022 09:07:08 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec29db2cbd680319ebcce0ec7ab7a8c578dda2ee1f609aff5ea375dfc991fc74`  
		Last Modified: Tue, 15 Nov 2022 09:07:09 GMT  
		Size: 91.9 KB (91864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

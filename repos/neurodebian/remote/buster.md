## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:67f47f5e946eb4e0d89a5b01fc42ae526b2823df93e00eae519bb36ae795de90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:7d4db3b4e802eb8f0b2bed6338f08ea4518fb1d277603616295a9e89e0a8e165
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61205110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717626b64d94ea824645c906720e650a46d8afa52376661f315e1ec675fea377`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 11:49:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 11:49:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 12 Mar 2021 11:49:04 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 12 Mar 2021 11:49:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a2d0d3500c57adb6c17eb6ff993e0d61f795521c3d587ce0313463486263f8`  
		Last Modified: Fri, 12 Mar 2021 11:53:37 GMT  
		Size: 10.5 MB (10499980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef3b59d3ded9ca7d96f3be474ab5d0ad4af78136e2fdfba13766b436512a078`  
		Last Modified: Fri, 12 Mar 2021 11:53:35 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6b63a7e6641631b8b997890d9cd9a3df2212821b0390774e229731c962b1a2`  
		Last Modified: Fri, 12 Mar 2021 11:53:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb9063d8cc1b8bed3ca27a47f6c41f3d7f7294a32b4dc4234b0885485d99347`  
		Last Modified: Fri, 12 Mar 2021 11:53:36 GMT  
		Size: 302.8 KB (302768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:impish`

```console
$ docker pull neurodebian@sha256:fb9d70b242241a7f28c19fb125129d670200adc31af1272c281c0e4c7f989ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:impish` - linux; amd64

```console
$ docker pull neurodebian@sha256:9da9c8a48c4bbcf25c9798ef2728cf737fce0bd91f192b87d31a8a7ad8983e6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34388953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac60fa6c4cdb0f5cde114b6544ab89585e5427532ddfd0bd5cee8f148e0564db`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:40 GMT
ADD file:0255a38a25ff74df5705cfa360847fd81f98cc513707203d1e54a75263f54a76 in / 
# Thu, 03 Mar 2022 20:19:41 GMT
CMD ["bash"]
# Wed, 16 Mar 2022 17:29:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Mar 2022 17:30:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Mar 2022 17:30:31 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian impish main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel impish main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Mar 2022 17:30:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec78bc49f256d7c26847ea612014b0bfd18cefe448e2b8e327512c6839fdba84`  
		Last Modified: Thu, 03 Mar 2022 20:21:02 GMT  
		Size: 30.4 MB (30385738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03ce6dd58207a5f8397252e03c3ebff09e5e023bbc80fd9d09c50c1a48090a0`  
		Last Modified: Wed, 16 Mar 2022 17:36:33 GMT  
		Size: 3.8 MB (3751767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db3bd723b7a1a05661566e4c3dd27126a929c99ce80921f802a1e8e1120d98b`  
		Last Modified: Wed, 16 Mar 2022 17:36:32 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f872629267f238b50b06db08163de9acef52bbc0870dd8d79d3f5d386c88fed9`  
		Last Modified: Wed, 16 Mar 2022 17:36:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873ae9b5b82b92a2e036b2ee3b923869fb85591c9dbcc56fe594b6496d52476e`  
		Last Modified: Wed, 16 Mar 2022 17:36:32 GMT  
		Size: 249.4 KB (249434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

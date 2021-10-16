## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:da0b3c83388dac096c680b497d60f4e7c82c94b754b526dadd9619b5c26cc331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:6020576c77de8eb4e2432365b189ec759793239bf9d737f6285b1baa40aae750
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34297016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c976f318d8686d7ddad6e8a7b2084aaefe84ec9495672f1e882831a720daa3d2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:07:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:07:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 16 Oct 2021 02:07:13 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 16 Oct 2021 02:07:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b2e1802902d4b686ded748236cc036979fdfd82e82e607e0badc756b24bb5`  
		Last Modified: Sat, 16 Oct 2021 02:08:21 GMT  
		Size: 5.5 MB (5489313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bf40aebf82d3ac28fb7d4ccda8ef313ecf6f2c58e35129c4b98152a8eff82d`  
		Last Modified: Sat, 16 Oct 2021 02:08:20 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096dc2a182b25047a0a0dfce1c7c098ca57a1496d681c1562a50f6c9a2b370db`  
		Last Modified: Sat, 16 Oct 2021 02:08:20 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fefdae26d52ebe499572d7769aee0f9c56db1fcba2dbbec69d0d71afb1baff2`  
		Last Modified: Sat, 16 Oct 2021 02:08:20 GMT  
		Size: 238.6 KB (238589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

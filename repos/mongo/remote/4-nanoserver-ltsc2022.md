## `mongo:4-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:ca7836f8c6363f67ea3bc91e8a96b4fc56488bd83191c82e6406addf29e065bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `mongo:4-nanoserver-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull mongo@sha256:35ecc80b2d195c3f35f005955b63aa9c0010fb30691ed3ccf917f2dda0d0261c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.4 MB (367420168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03d0317d7756ad8da827b16e966004f41a5954ccd0194e2f95ff1b0eadbcc2b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:16 GMT
RUN Apply image 10.0.20348.1668
# Wed, 12 Apr 2023 00:22:09 GMT
SHELL [cmd /S /C]
# Wed, 12 Apr 2023 00:22:09 GMT
USER ContainerAdministrator
# Wed, 12 Apr 2023 00:22:24 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Apr 2023 00:22:25 GMT
USER ContainerUser
# Wed, 12 Apr 2023 00:30:22 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 12 Apr 2023 00:36:58 GMT
ENV MONGO_VERSION=4.4.20
# Wed, 12 Apr 2023 00:37:21 GMT
COPY dir:35e2e0355933205dfcc9db0dd9dd7966fc920bed4837190cdb61a25f657355ad in C:\mongodb 
# Wed, 12 Apr 2023 00:37:40 GMT
RUN mongo --version && mongod --version
# Wed, 12 Apr 2023 00:37:41 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Apr 2023 00:37:41 GMT
EXPOSE 27017
# Wed, 12 Apr 2023 00:37:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:e06b772d586b58466a653b72002aee7c59496110e9ae402ff58f026e44452506`  
		Last Modified: Wed, 12 Apr 2023 02:34:14 GMT  
		Size: 122.3 MB (122328782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329579f5fc95fa89293545a20f4e45221db45261002e7012b86c4d3233edd1f8`  
		Last Modified: Wed, 12 Apr 2023 02:33:39 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ffee768115c8d7d69b2fd027383a36010ef0fdee82af33f03b9d4cd96300e0`  
		Last Modified: Wed, 12 Apr 2023 07:24:29 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b01eaee96d583c766fda2075c2b3f0d0ecbaae5f80349e49fd0231ded90b88c`  
		Last Modified: Wed, 12 Apr 2023 07:24:27 GMT  
		Size: 87.9 KB (87861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8632bd61e3a0f1116d090e2b6cafc76d6bb3c3b5cf14ac1fc393c94e4a1bc6`  
		Last Modified: Wed, 12 Apr 2023 07:24:27 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec487c1ab7e5a979f4fbd7e80f7bb8436646e0494b27aceb9005ca7e57dbba4`  
		Last Modified: Wed, 12 Apr 2023 07:29:50 GMT  
		Size: 263.5 KB (263515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01e3ce8e264056d9c4a240e734178ca5a3209d138d940dc396999287ca19de4`  
		Last Modified: Wed, 12 Apr 2023 07:34:14 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0066b0507c05812db880d0cb90ae93697aee92470bfbcd4ec6fde7d66d67ff7`  
		Last Modified: Wed, 12 Apr 2023 07:34:56 GMT  
		Size: 244.7 MB (244682856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e114fbc63e946dcf2687fc37e7c939436b3975b55f1dbde1ed0bc1d0c9cad7c3`  
		Last Modified: Wed, 12 Apr 2023 07:34:12 GMT  
		Size: 49.5 KB (49487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9837de55c7d812b041a13d73f299cdd15fb9a902ebe2abcf3c474be0e7cf11c8`  
		Last Modified: Wed, 12 Apr 2023 07:34:12 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6621f203f3fdde5dac0f4bc9a05f0e6a728b6ff0e4ed1c53b4820c06c3727c25`  
		Last Modified: Wed, 12 Apr 2023 07:34:12 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c59d1ea2b05cc17c3ad50c945e35820cbe4c3ed9f87193a5c10249ac20e30d4`  
		Last Modified: Wed, 12 Apr 2023 07:34:12 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

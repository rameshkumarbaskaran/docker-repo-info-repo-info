## `traefik:maroilles`

```console
$ docker pull traefik@sha256:9a53d5dff2c5b474a8560a4af129cc7863fb8932f8bd0e6896f4292445a2bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:78a0311203a68b2a9173d8e19b42fc39e5f02f17f1db03c1a06e3fa1c66f4dd7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21563612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b804da420476b5cbcc59bdd26e354e8fa44e4dfe20caf3ac84768dd143b5f2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:48:11 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:48:11 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Thu, 17 Dec 2020 00:48:12 GMT
COPY file:8e3cf7c133ac957e81d3eb831160ad827bfde058f356d7ac234b8c5ae307e37a in / 
# Thu, 17 Dec 2020 00:48:12 GMT
EXPOSE 80
# Thu, 17 Dec 2020 00:48:13 GMT
VOLUME [/tmp]
# Thu, 17 Dec 2020 00:48:13 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Dec 2020 00:48:13 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:79de75e85675fa9abbac17b57205d3e0dfcf2bd2fc4cbc194f2aaf917435425e`  
		Last Modified: Thu, 17 Dec 2020 00:49:17 GMT  
		Size: 130.9 KB (130872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0e925284bb6370a549da51637ed98a8e574317473e082cc4be745d87327c7f`  
		Last Modified: Thu, 17 Dec 2020 00:49:18 GMT  
		Size: 306.4 KB (306411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca797b3e2d2ac9c3925e07a34654011a4314302362ca0dfe8320d4425bf01f5`  
		Last Modified: Thu, 17 Dec 2020 00:49:22 GMT  
		Size: 21.1 MB (21126329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bb041f9232284130c3646cd4f0d83e032b078ae88a9ab88ea46580df2ee0b991
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20210272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c618c098e7b6182b45a63ffa8f49bb1656407fb6b666da85775efb87264cf12`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:26:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:26:48 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Thu, 17 Dec 2020 00:26:52 GMT
COPY file:a02ffe991352ee1f8abb077135ea9d27557e8b364fb712a42ccb2865e08df3cc in / 
# Thu, 17 Dec 2020 00:26:53 GMT
EXPOSE 80
# Thu, 17 Dec 2020 00:26:54 GMT
VOLUME [/tmp]
# Thu, 17 Dec 2020 00:26:56 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Dec 2020 00:26:57 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:26c529e82b09c489524aa4f787754320793a95eb7aa7eaf306c517b76818ec25`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adc6fb65827756c9d95005162623d443b2bd3e445269bcb1a7006e080726d3c`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 306.5 KB (306458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decc75cc844d668e21a715048cd9c78f2804e625a910fe5568e174c89bd5d8ab`  
		Last Modified: Thu, 17 Dec 2020 00:28:49 GMT  
		Size: 19.8 MB (19772941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2dc4a89841d24667bf689a0386eed1525cfe92afd4847039d73204d17e8d77f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19930321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5993443e6d894e7f4a83e79f4ede7636a3c8b57e7dca57a2dac980bed5a48274`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:27:56 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:27:58 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Thu, 17 Dec 2020 00:27:59 GMT
COPY file:f592954af2951d1a2538b1945366cb995f49638c7ef8b561b6961e0f8023197a in / 
# Thu, 17 Dec 2020 00:28:00 GMT
EXPOSE 80
# Thu, 17 Dec 2020 00:28:01 GMT
VOLUME [/tmp]
# Thu, 17 Dec 2020 00:28:02 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Dec 2020 00:28:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.26 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7dccf22d113d483cac839141f2028cbf6ac2e0c6aa4a1716c5e7b575b162028c`  
		Last Modified: Thu, 17 Dec 2020 00:29:55 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c32c03119dbb32c844511340cb40a21ba5a56b90862cf603dec2e49cf5ab20d`  
		Last Modified: Thu, 17 Dec 2020 00:29:57 GMT  
		Size: 306.5 KB (306466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda38820bf6e08ea342d37563cf7e4c258c772d4a0576588e8a451209a4534b2`  
		Last Modified: Thu, 17 Dec 2020 00:30:01 GMT  
		Size: 19.5 MB (19492982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

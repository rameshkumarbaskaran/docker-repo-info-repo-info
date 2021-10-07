## `traefik:maroilles`

```console
$ docker pull traefik@sha256:583a57788a093d3c42fe5e720f907e96bed0f7454bc456bf51ffc270e91740e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:ff05a8c2cb3098ea50561c5b861920c03648084a3f8cdcd67cfb241ffb36282e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22591630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd7bea620ba43343ba1af68fb1fecf463acf0014ba9a0d3f0c3a4e7b4dc18a9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 17:58:25 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Tue, 05 Oct 2021 17:58:26 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Wed, 06 Oct 2021 20:33:57 GMT
COPY file:7ad9801effe89697f09f236baf36b97aaf109e85d87c88062d54d4e989ecadb5 in / 
# Wed, 06 Oct 2021 20:33:58 GMT
EXPOSE 80
# Wed, 06 Oct 2021 20:33:58 GMT
VOLUME [/tmp]
# Wed, 06 Oct 2021 20:33:58 GMT
ENTRYPOINT ["/traefik"]
# Wed, 06 Oct 2021 20:33:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13e52be55f8d958b3ebb4e73685de5dd10ff4b4af613c4d23424519693aa01e0`  
		Last Modified: Tue, 05 Oct 2021 17:59:12 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f116118f8a36a09eba9c55ae29c9925e0ae854aa36d9dc1fc271a7be43b820c`  
		Last Modified: Tue, 05 Oct 2021 17:59:11 GMT  
		Size: 308.8 KB (308839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e461fe6ac72b68d38942ee7bd52b351bd04e3c840551d3907349c729386b45e5`  
		Last Modified: Wed, 06 Oct 2021 20:34:46 GMT  
		Size: 22.2 MB (22160384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a9115bd64291c28569b4da6603043fe5c5f77b67ac16c9573a639842d19f55f6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 MB (21049536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa32dfeccdefca2de2d0b79a80eed77609a1a3e53683324ce24ccb1eec093cb0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Tue, 05 Oct 2021 00:02:40 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Thu, 07 Oct 2021 19:31:28 GMT
COPY file:37d0f8b70c5da3bdf158098e422d0bfc00d82405c51ca41ee81a5e564433a943 in / 
# Thu, 07 Oct 2021 19:31:29 GMT
EXPOSE 80
# Thu, 07 Oct 2021 19:31:29 GMT
VOLUME [/tmp]
# Thu, 07 Oct 2021 19:31:30 GMT
ENTRYPOINT ["/traefik"]
# Thu, 07 Oct 2021 19:31:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07230710ce3c527700e0de335b44592e9a29b741a0fd3b5c78768beb4d5378e`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 308.9 KB (308869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58879bf3ff90c00bf7b32d71c06d81a17679e973ce7bf8c2e6cdaac88ab37518`  
		Last Modified: Thu, 07 Oct 2021 19:33:51 GMT  
		Size: 20.6 MB (20618260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ceb4d0b580f99ba7186eb68ebb5da861036a65b7dd3a3a8be6086408806806c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20555485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41d64d7db7d81bed5981d3228e6abde55f5219b00d9eff6fa0d48e489109a36`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 04 Oct 2021 23:44:22 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 04 Oct 2021 23:44:23 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Wed, 06 Oct 2021 21:52:27 GMT
COPY file:7172e6e5ffb5f02ce32799c6a7b8f10cd07c43e34b1505195e8781415e14dd8b in / 
# Wed, 06 Oct 2021 21:52:27 GMT
EXPOSE 80
# Wed, 06 Oct 2021 21:52:27 GMT
VOLUME [/tmp]
# Wed, 06 Oct 2021 21:52:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 06 Oct 2021 21:52:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.32 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3c562953a5524a25157fc08c1e7009693f341518b2dcfdcab8ae04d990438254`  
		Last Modified: Mon, 04 Oct 2021 23:45:36 GMT  
		Size: 122.4 KB (122408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086b385acba426fecb8a1f24e7e5b29c5b3dfdf54524653104e29d181dcbcd5b`  
		Last Modified: Mon, 04 Oct 2021 23:45:36 GMT  
		Size: 308.9 KB (308866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47ebd5bd859bc4a1d464bf0fb37139222c96add606e8d090061f441ec23e3d1`  
		Last Modified: Wed, 06 Oct 2021 21:53:44 GMT  
		Size: 20.1 MB (20124211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

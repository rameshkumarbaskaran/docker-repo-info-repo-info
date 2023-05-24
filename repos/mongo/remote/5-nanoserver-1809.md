## `mongo:5-nanoserver-1809`

```console
$ docker pull mongo@sha256:a6d616eed722d52d3952f43cf08bea9cb82dbb4a80025bc7a50aeec5ee6fa554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `mongo:5-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull mongo@sha256:2c03faf4124e56330f71cd3c14a554909b3974bb687730643292ad692599ce38
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.3 MB (417334917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c08f7c9287e32f551039a63f148550f3a2c7124756d11d6e7432b761e5b768`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 01:31:05 GMT
SHELL [cmd /S /C]
# Wed, 10 May 2023 02:01:10 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 02:01:23 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 May 2023 02:01:23 GMT
USER ContainerUser
# Wed, 10 May 2023 02:08:12 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 24 May 2023 01:28:43 GMT
ENV MONGO_VERSION=5.0.18
# Wed, 24 May 2023 01:29:08 GMT
COPY dir:ab74dbf9ad27d2154a3f270894c5c95f10fe56a2d5ec4c1875a57c2afdba8cff in C:\mongodb 
# Wed, 24 May 2023 01:29:23 GMT
RUN mongo --version && mongod --version
# Wed, 24 May 2023 01:29:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 May 2023 01:29:24 GMT
EXPOSE 27017
# Wed, 24 May 2023 01:29:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ddac9d33b62fa0bb37c6743a1992a622e53b5bb070758474e92416b5f031ba`  
		Last Modified: Wed, 10 May 2023 01:48:38 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca1a117e5be28c4247978f3dfd437fff6feffb4a11ea43d4338f5d2b068ac76`  
		Last Modified: Wed, 10 May 2023 02:26:28 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba404708f5c409a4327ef9a8ea3e3601dd2db287f5d90c7794dada10f4ae9e69`  
		Last Modified: Wed, 10 May 2023 02:26:26 GMT  
		Size: 62.9 KB (62943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc7f80cef905cfe3aae8cf8ef021d8f598871b9df0222b4cc3f5b66899cac64`  
		Last Modified: Wed, 10 May 2023 02:26:26 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd95f6c90520d7fe9349ffc114d55efdfc3d2a4675433070a2dd42eb6d76948`  
		Last Modified: Wed, 10 May 2023 02:31:00 GMT  
		Size: 263.4 KB (263441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f126b2674157993a9251a77346bbf0f4853a0956341a769942985b98ff291ad1`  
		Last Modified: Wed, 24 May 2023 01:45:54 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b35e49e114fb028e4eac711546aa4986295babb8960da5c8ea7526d5f90eb9`  
		Last Modified: Wed, 24 May 2023 01:46:46 GMT  
		Size: 312.5 MB (312540301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf11fe0a5fd800d967962cffaa0cfeb5a2fce818da6960e3de98009a45a89724`  
		Last Modified: Wed, 24 May 2023 01:45:53 GMT  
		Size: 76.4 KB (76351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac07e47ebc417b62bcfd88a23969e8e3d37e61a30749858d2b2410a45b4501d9`  
		Last Modified: Wed, 24 May 2023 01:45:53 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3db67ab465ef7e2c73a5ebc2ebbd503c709399a13a21110353da11bb731898`  
		Last Modified: Wed, 24 May 2023 01:45:53 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b84b4edd4bcde054d061c19fec8681db047c6ba51bd0a43f7cfb763d855546f`  
		Last Modified: Wed, 24 May 2023 01:45:53 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

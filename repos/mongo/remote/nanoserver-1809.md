## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:8454f743c006d432a9caab5471416f1fc239cb55e1aee9c35510ca4e943dcbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull mongo@sha256:4065aa35739518e4399eb92ee5c1403de2dc00cd31493cf07f8b14fe84a54c07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.8 MB (333764344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc498716715d748f4ec4cc9bc19cedd6165d3c088048e68ba4d01f950ccc648`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 12:49:37 GMT
SHELL [cmd /S /C]
# Wed, 09 Jun 2021 20:36:09 GMT
USER ContainerAdministrator
# Wed, 09 Jun 2021 20:36:31 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 09 Jun 2021 20:36:33 GMT
USER ContainerUser
# Wed, 09 Jun 2021 20:36:36 GMT
COPY multi:0196f9e96f60ad3e2b92fd0773f8d0fe3a8235e1eefbb9ef1a1f0d672e6a711c in C:\Windows\System32\ 
# Wed, 09 Jun 2021 20:44:03 GMT
ENV MONGO_VERSION=4.4.6
# Wed, 09 Jun 2021 20:44:27 GMT
COPY dir:e5731845368f7299600736cac7a9579787821dfbdc9d4f89336700f23196d727 in C:\mongodb 
# Wed, 09 Jun 2021 20:44:56 GMT
RUN mongo --version && mongod --version
# Wed, 09 Jun 2021 20:44:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Jun 2021 20:45:01 GMT
EXPOSE 27017
# Wed, 09 Jun 2021 20:45:03 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2646c4431bb01c2667bc3bd1353d18b2632d04cc58ad53a79480ecdde4fd710d`  
		Last Modified: Wed, 09 Jun 2021 13:05:18 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11e7e37417b2fb90324deddea0736ad85cd4ba5ffdaefcb26fb1178aebc7a91`  
		Last Modified: Wed, 09 Jun 2021 21:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce0c822d8bf8e33e253a361caa9d023f96983c6cd09d552e4d7839f76f55512`  
		Last Modified: Wed, 09 Jun 2021 21:04:03 GMT  
		Size: 70.0 KB (69960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e153c857d2b7eb18535188b5d573c2ee3556ebf5d69f9dba2ed4a2d3c48c7f38`  
		Last Modified: Wed, 09 Jun 2021 21:04:02 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f414141758172a32421c56dd39ef2f6d31aee7994bf34d50441654fb7d34a33e`  
		Last Modified: Wed, 09 Jun 2021 21:04:02 GMT  
		Size: 274.1 KB (274087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6253490832fa2f53b487b83e4db4c35f05559794da99cdab4fcf212ec7a51145`  
		Last Modified: Wed, 09 Jun 2021 21:11:13 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ca5d32d6fe1a681f17e6aa9ea8e7837a2de8161168a565b37ba670b122fc41`  
		Last Modified: Wed, 09 Jun 2021 21:11:57 GMT  
		Size: 230.7 MB (230658828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eeddc751d16258e3a11b475296ba22ff551ae6005e765c11e3d37907df7628`  
		Last Modified: Wed, 09 Jun 2021 21:11:11 GMT  
		Size: 81.9 KB (81948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9007900f6a0b53f087a0cc0afec67dd5ba8456e89cab7bd73e9bf43a18604c`  
		Last Modified: Wed, 09 Jun 2021 21:11:11 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcb4bfba81c163055fbd4b28803011bfb450c7de1e2d274d5957d9aff7a5470`  
		Last Modified: Wed, 09 Jun 2021 21:11:11 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ad3893b78575fe2852bc15b5c20837e0eeaa9c507a690c96632d3102261728`  
		Last Modified: Wed, 09 Jun 2021 21:11:11 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

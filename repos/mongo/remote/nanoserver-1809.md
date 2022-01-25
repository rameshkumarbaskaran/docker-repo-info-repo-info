## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:5ca679bc81975382df48ddcc4cfea8023ef69b0f009e705fc96bc980bb927f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull mongo@sha256:210fc74494c3d2a9271bf3c48a099d3c790b79ca1ae1260224fa6bd436db1974
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 MB (397388721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edc7f611dc47617132b24220187f687677b188a3c77e76c39e1d2f512825faf`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Mon, 24 Jan 2022 23:24:23 GMT
SHELL [cmd /S /C]
# Mon, 24 Jan 2022 23:24:23 GMT
USER ContainerAdministrator
# Mon, 24 Jan 2022 23:24:38 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Mon, 24 Jan 2022 23:24:39 GMT
USER ContainerUser
# Mon, 24 Jan 2022 23:24:40 GMT
COPY multi:0196f9e96f60ad3e2b92fd0773f8d0fe3a8235e1eefbb9ef1a1f0d672e6a711c in C:\Windows\System32\ 
# Mon, 24 Jan 2022 23:24:41 GMT
ENV MONGO_VERSION=5.0.5
# Mon, 24 Jan 2022 23:26:11 GMT
COPY dir:97e0851993a8443e809dbfb982fa612becf2ad4c3b07d76c242613492af3987d in C:\mongodb 
# Mon, 24 Jan 2022 23:26:23 GMT
RUN mongo --version && mongod --version
# Mon, 24 Jan 2022 23:26:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Jan 2022 23:26:25 GMT
EXPOSE 27017
# Mon, 24 Jan 2022 23:26:26 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fdb052c4016b3238a417abae6ce3a3c81e145118a4325ab2c01bba6cc9eedc3f`  
		Last Modified: Tue, 25 Jan 2022 00:19:35 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239067809343d5f4e095b39624dfb9ca941d8dded1963d405cf946c066fc3988`  
		Last Modified: Tue, 25 Jan 2022 00:19:34 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e4524972be3a240be3eceb5d9e1b0ba086c38be42fbd75d9a9eda4bbd6d716`  
		Last Modified: Tue, 25 Jan 2022 00:19:33 GMT  
		Size: 75.2 KB (75231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d41aa32bc9bad3c1aaf1a0eeddb9f7aa652e2114e669ad049b3935d95e7bd92`  
		Last Modified: Tue, 25 Jan 2022 00:19:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dc023480baef892891b405c690a00f168e34e86f058bd67cd52edbfaf5704e`  
		Last Modified: Tue, 25 Jan 2022 00:19:33 GMT  
		Size: 274.1 KB (274091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5758f3a928dbde5c5de309941ae49cda6ca242a12d038906bf8d76efcca83a4`  
		Last Modified: Tue, 25 Jan 2022 00:19:32 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08cdb6f97175d04c8e9faa8cb1f17b50f894f8f8f93eee9a8bdcf9d40f9c7c8`  
		Last Modified: Tue, 25 Jan 2022 00:25:17 GMT  
		Size: 293.9 MB (293936068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fa5190cd5e47aadbe405307872b849f612403804ec5e709673c611ef1d94df`  
		Last Modified: Tue, 25 Jan 2022 00:19:30 GMT  
		Size: 48.6 KB (48605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98414ea99737dd5d5c5b028cdaa536c346303a6ce4540b54479eb07094202cd`  
		Last Modified: Tue, 25 Jan 2022 00:19:30 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04eb1b717fdc0e0d37d991c69bcf773fe5e57487d1bbd2a4ae500230c6cdea2a`  
		Last Modified: Tue, 25 Jan 2022 00:19:30 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f447323df43cc81274227837ff2dc58726412388919cdd4788436928c4ea83`  
		Last Modified: Tue, 25 Jan 2022 00:19:30 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

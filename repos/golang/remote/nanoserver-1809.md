## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:f06cd31f17e0af1f86b07d34ecd4c85c8b568ebaf1013dbc5328cba4b28ed9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull golang@sha256:103210f1c9b851c70d51e30fcc94a4530002ef01b384a7a87abb505e0572ac77
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240466282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4310b0a9a59ca0dbcc79d2ace91e5e2ecd8ee080b62dfde583a7195686d3bc45`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 12:43:35 GMT
SHELL [cmd /S /C]
# Wed, 14 Apr 2021 12:43:36 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:43:37 GMT
USER ContainerAdministrator
# Wed, 14 Apr 2021 12:44:20 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 14 Apr 2021 12:44:21 GMT
USER ContainerUser
# Wed, 14 Apr 2021 12:44:22 GMT
ENV GOLANG_VERSION=1.16.3
# Wed, 14 Apr 2021 12:46:23 GMT
COPY dir:b88401ff3780d42fbfa834639653cb0f9afc98bbd3e0bff92e1ba020b4435072 in C:\go 
# Wed, 14 Apr 2021 12:46:47 GMT
RUN go version
# Wed, 14 Apr 2021 12:46:48 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:be6876a5c8fd442b68d04a6a7e144db66f22e7c7aba22b514442a31e0f83c50e`  
		Last Modified: Wed, 14 Apr 2021 13:02:13 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2077d5bc588bdc2938e30cfb02f3928dd2ccd386a44bcf2b6531d858fe1dd2`  
		Last Modified: Wed, 14 Apr 2021 13:02:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c020c23ff9ec520045bfa017d66096a8a5358a99779da558caf7e7f070a7de`  
		Last Modified: Wed, 14 Apr 2021 13:02:12 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7d9a60f17fee47fbd5aa1e0b8f6d9e96f2bf0b1eb3bd2742a7b73f0fb88a75`  
		Last Modified: Wed, 14 Apr 2021 13:02:12 GMT  
		Size: 66.6 KB (66580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68b9bedd117801b679f126ab1a3f4c6e345b067246680ca5e36b693e5c14ba7`  
		Last Modified: Wed, 14 Apr 2021 13:02:10 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8326103279c9f82135534e8a576529b63bd24eb51704114001604c5dc583b73c`  
		Last Modified: Wed, 14 Apr 2021 13:02:09 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a89ef84bda1e55b76e1afb56e1f2c8a572d07f5c811e23d3773b504afa8ed5`  
		Last Modified: Wed, 14 Apr 2021 13:04:41 GMT  
		Size: 139.0 MB (138982338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de041e4e8abdd6b971c81cf03a6fe9078b0733a2bc9b94ca733e388937d1b07d`  
		Last Modified: Wed, 14 Apr 2021 13:02:09 GMT  
		Size: 70.1 KB (70056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933892e418ebf92f2437e18b5374add6d9f51025e2698bb63fa0ec0f5b1fbbb8`  
		Last Modified: Wed, 14 Apr 2021 13:02:09 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

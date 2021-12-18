## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:347a25c99eb0eea6253abf9ee1026a1b7cccf82bdfe33da4e4d426ac967f7082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull golang@sha256:2423a4cad673ebe84611ee15823b5e8a36a836aae634b82001f8f7009aa26941
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248126537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2097c83dcab0d1c8f1011ba7ab040a3558e3c5e2c6de70fd54d062a73dbf2560`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 00:33:50 GMT
SHELL [cmd /S /C]
# Sat, 18 Dec 2021 00:33:50 GMT
ENV GOPATH=C:\go
# Sat, 18 Dec 2021 00:33:51 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 00:34:18 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Sat, 18 Dec 2021 00:34:18 GMT
USER ContainerUser
# Sat, 18 Dec 2021 00:52:41 GMT
ENV GOLANG_VERSION=1.17.5
# Sat, 18 Dec 2021 00:54:52 GMT
COPY dir:4c99dbbc4d53a915cdc29ae9417d812da5b5217c7296fe04ef7fdf708c4a960d in C:\Program Files\Go 
# Sat, 18 Dec 2021 00:55:38 GMT
RUN go version
# Sat, 18 Dec 2021 00:55:38 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dac80fcd8aee90ad8a9145e0685b7c90d701307507ff32ffed6c86abc09c0f7a`  
		Last Modified: Sat, 18 Dec 2021 01:24:07 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c14910fae13be585e698e80c191a6ca8b4d4ca7c1cfa7ba6e5839c0ff9d37cc`  
		Last Modified: Sat, 18 Dec 2021 01:24:07 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c585c62725044581c397691e0cc42f23784332757eae6be3ebbb4f8ebf83a9c9`  
		Last Modified: Sat, 18 Dec 2021 01:24:07 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a4b06c80653b74f6d18b1845aaa0bab0a8234513e2beb5a97a655d96152ff7`  
		Last Modified: Sat, 18 Dec 2021 01:24:07 GMT  
		Size: 67.7 KB (67683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb2867122ac52d3617c048f83a93cca87925a6e5530e20d89648feadbcb23b7`  
		Last Modified: Sat, 18 Dec 2021 01:24:05 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4b439d91f68c93d58ecbba76e17c848518f670c7c0847a4f80d7f22eba5706`  
		Last Modified: Sat, 18 Dec 2021 01:34:48 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c9d275a4376b69f2a56d1055043fec305f987155570d4745b91e75c664e8d`  
		Last Modified: Sat, 18 Dec 2021 01:35:23 GMT  
		Size: 145.1 MB (145076108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f5228beb9357c77b17f33ce270a0578233c5157e27aabfd11473459979a56e`  
		Last Modified: Sat, 18 Dec 2021 01:34:48 GMT  
		Size: 72.0 KB (72020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664662bb130239d39eaba6a6963a5da11018a06101e9375acf289e837d44e2b5`  
		Last Modified: Sat, 18 Dec 2021 01:34:48 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

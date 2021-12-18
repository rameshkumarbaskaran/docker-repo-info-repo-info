## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:d59bab5d20df3a5db338a730768c034d39b734409acb55d9acd2fd4e0a344fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.405; amd64
	-	windows version 10.0.17763.2366; amd64

### `golang:1-nanoserver` - windows version 10.0.20348.405; amd64

```console
$ docker pull golang@sha256:c2fae6015e319e75712f5118b1427f7d2e8023f83c72fb401406f58c32479843
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262432685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d86f570f0964e14e46beae171af4ee2ed1b6ce3b355274b957e3d937081fa5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 08 Dec 2021 01:24:33 GMT
RUN Apply image ltsc2022-amd64
# Sat, 18 Dec 2021 00:29:51 GMT
SHELL [cmd /S /C]
# Sat, 18 Dec 2021 00:29:52 GMT
ENV GOPATH=C:\go
# Sat, 18 Dec 2021 00:29:52 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 00:30:22 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Sat, 18 Dec 2021 00:30:23 GMT
USER ContainerUser
# Sat, 18 Dec 2021 00:49:13 GMT
ENV GOLANG_VERSION=1.17.5
# Sat, 18 Dec 2021 00:51:32 GMT
COPY dir:4c99dbbc4d53a915cdc29ae9417d812da5b5217c7296fe04ef7fdf708c4a960d in C:\Program Files\Go 
# Sat, 18 Dec 2021 00:52:23 GMT
RUN go version
# Sat, 18 Dec 2021 00:52:24 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:11961e4f2e13a442b572d4bc37edfe94ad6d8c2ed378f0dcae8b880959c4b538`  
		Size: 117.2 MB (117225770 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5f7005dc509dad3c53e79bd72ff76e4dda4a38b2eee2264ceb864eaa233dab99`  
		Last Modified: Sat, 18 Dec 2021 01:23:16 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4e9f3e38224e5b84c429855780b0ef7e6b0a577e925894bf426a73252fe4dd`  
		Last Modified: Sat, 18 Dec 2021 01:23:18 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f2acbfdb66c79b7e8a0b1a4194db1d7d6513ea6cc53dfb4221b786c7c74a8e`  
		Last Modified: Sat, 18 Dec 2021 01:23:15 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40585525152eca561c21db4a5bd8b39d73bf0e6db9a501c19e1aa7c08c6b4014`  
		Last Modified: Sat, 18 Dec 2021 01:23:15 GMT  
		Size: 78.6 KB (78567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f03c4a986705577537ed4bcc508d6c305c7b567c6838dd124f535f59759c36b`  
		Last Modified: Sat, 18 Dec 2021 01:23:13 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a938e6f2658df3154bc9e901ccb8b1e61ed29f5a0a8bd656dd6b550bc0e1e6`  
		Last Modified: Sat, 18 Dec 2021 01:33:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3990eeb569528947ecdc8e1b95ef324cba453111c0432be72a9d471e02a808da`  
		Last Modified: Sat, 18 Dec 2021 01:34:34 GMT  
		Size: 145.1 MB (145070598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cd9a35df659c1dd114aff0dcd2dae3ec48f79ff61f327a3c9f7d5655a2a286`  
		Last Modified: Sat, 18 Dec 2021 01:33:59 GMT  
		Size: 50.6 KB (50582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8043972cbae6f05382e3c4aee086cfb764fa2fbe40d3951c2ac58c5195aeff3a`  
		Last Modified: Sat, 18 Dec 2021 01:33:59 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.17763.2366; amd64

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

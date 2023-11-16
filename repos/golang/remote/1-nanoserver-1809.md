## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:ce0137f7ae80583b1244d7b01f340598aadd387d6ea5228872806a203d24f933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull golang@sha256:78e67a37069c83f0c26f94eb8d4c5f136289565a61e5f06807b5ff551844fc1d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.6 MB (173649973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed6bdc5ab9882a73480c99c94b56ec20f3c3ba7b27573efcabc3ac7a5cf17f0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 02:55:52 GMT
SHELL [cmd /S /C]
# Thu, 16 Nov 2023 02:55:52 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:55:53 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 02:56:03 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 16 Nov 2023 02:56:04 GMT
USER ContainerUser
# Thu, 16 Nov 2023 02:56:04 GMT
ENV GOLANG_VERSION=1.21.4
# Thu, 16 Nov 2023 02:58:04 GMT
COPY dir:7827edb83457064cd80294b50515e727b7fbe2b5f8a90735cc2b12437bf56ebb in C:\Program Files\Go 
# Thu, 16 Nov 2023 02:58:23 GMT
RUN go version
# Thu, 16 Nov 2023 02:58:25 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26eb16ff47ed3c1f3ff64a9920a3407afa035ee398f803b948326dc0e5e4e79e`  
		Last Modified: Thu, 16 Nov 2023 03:13:07 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f758d4db50553e4dba17ca30d3cefa3a18af457915c26e8d11bc54fef1070b6`  
		Last Modified: Thu, 16 Nov 2023 03:13:07 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b835dcd535b713623a8859c2cfa90a2d2ae7a964b1031fddfa3f432c961d19`  
		Last Modified: Thu, 16 Nov 2023 03:13:07 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0616eabfec61b5839eed830a30e25005beb525fb9faaf41ea40b6f258fe9a391`  
		Last Modified: Thu, 16 Nov 2023 03:13:07 GMT  
		Size: 71.7 KB (71710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0ef9230d8f093c04263f87734f7963bbaa3f479c8676b3b8fa54569897f6e6`  
		Last Modified: Thu, 16 Nov 2023 03:13:05 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6a276fe5fab852cced43e331371859b8c9f6044a59fe1a1780f9c3e0b9e739`  
		Last Modified: Thu, 16 Nov 2023 03:13:05 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e537d6aa81396fb0870c0b410dc41d0a8172db45be84ba6c219d5086b2ba2c8`  
		Last Modified: Thu, 16 Nov 2023 03:13:27 GMT  
		Size: 69.0 MB (69024011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543cf9acc0624c865f1166e9883024b92249b9a91dd2c43eb7ed2528671d97aa`  
		Last Modified: Thu, 16 Nov 2023 03:13:05 GMT  
		Size: 50.3 KB (50279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3594dd8843bff37ebf0b8c26941971fd2386ef78e9f3642819dc879244100685`  
		Last Modified: Thu, 16 Nov 2023 03:13:05 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

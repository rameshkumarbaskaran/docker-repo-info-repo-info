## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:4bd37bd7a2a37b97d33f78d9f1faee2025a715cb7d29102d6cdcd31b01f6dac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull golang@sha256:d07ab30472f8bac7ef8676aa70d315de324225dd819be2219fb689e4278036db
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213147043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd5c2b597bc48e176445b2663b6cf40e79e53798ddd95e486c405187a4787b1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 01:31:05 GMT
SHELL [cmd /S /C]
# Wed, 10 May 2023 01:31:06 GMT
ENV GOPATH=C:\go
# Wed, 10 May 2023 01:31:06 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 01:31:15 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 May 2023 01:31:15 GMT
USER ContainerUser
# Wed, 10 May 2023 01:31:16 GMT
ENV GOLANG_VERSION=1.20.4
# Wed, 10 May 2023 01:32:59 GMT
COPY dir:522e0da3d6c3a6cfa6b16530131c440cc60a26151f29e0cb9d21de10dd15cbac in C:\Program Files\Go 
# Wed, 10 May 2023 01:33:16 GMT
RUN go version
# Wed, 10 May 2023 01:33:16 GMT
WORKDIR C:\go
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
	-	`sha256:85a155cedba06fb5098abf51cdebd14a436bafaa6b6331cdf23c15a1b88aa9a6`  
		Last Modified: Wed, 10 May 2023 01:48:38 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd8f19817a4336375d9d4706a35ee835a3391a94309471d2d0465cc38b3f181`  
		Last Modified: Wed, 10 May 2023 01:48:38 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67b17eb34d866264b66ab9e30b51834fef645f02261a5382f9d80bf1e377340`  
		Last Modified: Wed, 10 May 2023 01:48:38 GMT  
		Size: 65.5 KB (65474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7b0290c09d5f21a749be38c92ce5c06bd83dde4983d6e7c543189c6611324b`  
		Last Modified: Wed, 10 May 2023 01:48:36 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486b69967a87e750d2600f38c81e55e8dd1bbb9fe0593f06f6502edb349fd7ec`  
		Last Modified: Wed, 10 May 2023 01:48:36 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4795822cbdef1ebda9571a3e5301b09e2376c706741ab7c7ccbd870a4e83b6dc`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 108.6 MB (108610864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4691a6bbbb1df772952aafab87f3c522e4638e18b12762820074f780b3fdfece`  
		Last Modified: Wed, 10 May 2023 01:48:36 GMT  
		Size: 79.5 KB (79546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be1ffcd7e61caf49121c54e4c63dbfb0428f87b863fba9bc1594b742885d19b`  
		Last Modified: Wed, 10 May 2023 01:48:36 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

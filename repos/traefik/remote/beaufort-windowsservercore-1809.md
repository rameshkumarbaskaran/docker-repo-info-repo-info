## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:95274097834b137a81339fc12c2d08fa49275d50f6c8ef35643b1635a16ed6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull traefik@sha256:b9676abc64517cec8a5ab93086f18d2ef4d18e0e71b56e6c2a2ff6125d310ab7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2070508847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83603ed5bad2e6db5685103817ac65b1e63673ed89b5dff5fcd5187568e0341`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 06:55:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Oct 2023 06:55:40 GMT
EXPOSE 80
# Wed, 11 Oct 2023 06:55:41 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Oct 2023 06:55:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b65c4e56fd1d876d2a965e000a7aa240a57bfddee6c3ebaea6c7b34436d1653`  
		Last Modified: Wed, 11 Oct 2023 06:57:43 GMT  
		Size: 38.9 MB (38912828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ebc3acc69abc564461c51da48f015e2eb23222157526964b1a6d411573f00c`  
		Last Modified: Wed, 11 Oct 2023 06:57:35 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f6c5b726630e7b6666c48dd0c04c8800e293754acfe5c1cbb8e8813a71d81a`  
		Last Modified: Wed, 11 Oct 2023 06:57:35 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07fa1c30f0c8c8049acffb4756128c3060a6cd0334970dac14b87b944d6112a`  
		Last Modified: Wed, 11 Oct 2023 06:57:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

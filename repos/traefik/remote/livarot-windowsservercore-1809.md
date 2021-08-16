## `traefik:livarot-windowsservercore-1809`

```console
$ docker pull traefik@sha256:981f64ad8bc2eb274826d977925c52c4929f28067bda9206ac9fe74a116bee33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:livarot-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:c4d57df45f54ecd6b31b92099182a2d8ffc8cf5ab3cf3976d782caae119cedd5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711252092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b861721a173d361f9a0e7279d9b4e50819e6aea1e47838a6a93101549cf655`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Aug 2021 19:16:15 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.14/traefik_v2.4.14_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 16 Aug 2021 19:16:18 GMT
EXPOSE 80
# Mon, 16 Aug 2021 19:16:20 GMT
ENTRYPOINT ["/traefik"]
# Mon, 16 Aug 2021 19:16:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.14 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd3eec1f322c635dd3f8d133b5891c8280d05da5106e3d94b77a9d7f663be8a`  
		Last Modified: Mon, 16 Aug 2021 19:17:11 GMT  
		Size: 25.2 MB (25248436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc950fc6284ab40137ee825b561d7916430ada073dced7907ec943150151374`  
		Last Modified: Mon, 16 Aug 2021 19:17:04 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324e3c2a4e5b9741ea03ca8043b363a1c4a352ffb6858c0c8240a2c85677ee0d`  
		Last Modified: Mon, 16 Aug 2021 19:17:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798d0a148fd886ebbf5f8221a9c84f3fdf7dc337ea2b9d6a2aea7391cdd4d93c`  
		Last Modified: Mon, 16 Aug 2021 19:17:04 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

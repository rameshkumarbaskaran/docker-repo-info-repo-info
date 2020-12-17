## `traefik:picodon-windowsservercore-1809`

```console
$ docker pull traefik@sha256:ab1ca488ee5f68844454eaf632e76e34e72a029d648990f9b07002cbedc68760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `traefik:picodon-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull traefik@sha256:dfd14d68b36b35c281b7503828f020c632913f2ae3bd86b071f7261dade83398
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2425402277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e589c8d114b27b8f3abf3651f62921ca7a75062e16a78db38e3eb95877397136`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 13:30:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Dec 2020 23:16:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.6/traefik_v2.3.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 17 Dec 2020 23:16:08 GMT
EXPOSE 80
# Thu, 17 Dec 2020 23:16:09 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Dec 2020 23:16:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a4372d14958dc8a7eaaace9e4774e7f1db524da5eb4474b5e46738848a3a61a5`  
		Last Modified: Wed, 09 Dec 2020 13:54:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48993525e065f237390d2f2cdc926adbb0bcabb6019e76e75eaeb003e25a05e1`  
		Last Modified: Thu, 17 Dec 2020 23:17:02 GMT  
		Size: 34.5 MB (34523301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fee1df3533145b694b76b96d20f376d442a73307cbed2fcfc3f311afa9f5f8`  
		Last Modified: Thu, 17 Dec 2020 23:16:54 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091731933ce3fce78a20ad394caaab4a9936e53a58f72dee2a8b446d27cf99bb`  
		Last Modified: Thu, 17 Dec 2020 23:16:54 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e499764964d282381dc1dc8f4dc1a119c1da4e22fc41849797994613876e6b`  
		Last Modified: Thu, 17 Dec 2020 23:16:54 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

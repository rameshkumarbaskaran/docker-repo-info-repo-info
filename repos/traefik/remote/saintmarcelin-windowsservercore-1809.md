## `traefik:saintmarcelin-windowsservercore-1809`

```console
$ docker pull traefik@sha256:d924ca92f14584ed4c2cd33915cecca5e800f281c067f9b3571a22212bc2cb15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `traefik:saintmarcelin-windowsservercore-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull traefik@sha256:a241df861208d3751f9b706f43d04eed4853b887a602b08c58b55a8dc1fc9f7a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2108926385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836dd9646a08b1025557765736f0bd90e24bad69eee5cc38f12bb3734e7e966e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Tue, 11 Apr 2023 23:40:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Apr 2023 19:17:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.1/traefik_v2.10.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 27 Apr 2023 19:17:30 GMT
EXPOSE 80
# Thu, 27 Apr 2023 19:17:31 GMT
ENTRYPOINT ["/traefik"]
# Thu, 27 Apr 2023 19:17:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9103f1e2cdefe8f16dae9619b88e38aa659abb17276d2362d435ad0721d3bf41`  
		Last Modified: Wed, 12 Apr 2023 00:50:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99660c4e30b34d279e40936ebe3f9fdd95137be529710706f2c00d6edbf657d3`  
		Last Modified: Thu, 27 Apr 2023 19:18:23 GMT  
		Size: 37.6 MB (37629562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57958f4cab27a88f94b8acf7680c45be8d457ad9e0a37ca751db415631e65d71`  
		Last Modified: Thu, 27 Apr 2023 19:18:15 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db08e01671cab696252f7d36ac309a2ef9a7886a3c698a8143ffc469e3b0884`  
		Last Modified: Thu, 27 Apr 2023 19:18:15 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f8a3a75daf984dd99429b7ee07348ec362a5c787505882dee20b1da3eaf917`  
		Last Modified: Thu, 27 Apr 2023 19:18:15 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

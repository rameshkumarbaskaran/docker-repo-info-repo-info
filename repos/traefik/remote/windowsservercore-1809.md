## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:0171555d49032d3e9a8143f92d75bb773bd1d02d0c6ab5c1ce038e1b9d8a97fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull traefik@sha256:7d9e986b167fd6a6e8caf0d270cff4848f68e67d615789d5072359dfaae4658c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098008476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef5097a6081d1124f5e62b4a0cb1e6f2798c0be3bf4b2ac534172dac2e4aa73`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 08:34:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.5/traefik_v2.10.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 16 Nov 2023 08:34:26 GMT
EXPOSE 80
# Thu, 16 Nov 2023 08:34:27 GMT
ENTRYPOINT ["/traefik"]
# Thu, 16 Nov 2023 08:34:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5364859be3494bde67293ec5e752ce6710eb84de075e56586e9dc1a05b9a4953`  
		Last Modified: Thu, 16 Nov 2023 08:35:34 GMT  
		Size: 40.6 MB (40571250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8773eae2563ee25a1f20ece298456e74f874c3ae705b5516b5f0c51fb4df1a`  
		Last Modified: Thu, 16 Nov 2023 08:35:24 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676bd9e03c6916f67ddb80177e5dbcb9ba48e2a02aa73990f4a3ca84e314b1e1`  
		Last Modified: Thu, 16 Nov 2023 08:35:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d97aade365ce6ad0e88dbeacf46d6d4848438afe9098c42f9d45cb56c3d5889`  
		Last Modified: Thu, 16 Nov 2023 08:35:24 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

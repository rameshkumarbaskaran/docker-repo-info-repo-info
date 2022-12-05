## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5eeae50f78f79dd84fee1bb77fe7fe7384a13dbd32ebaa5c80bc9b15d83d1d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull traefik@sha256:1caf484b3364fc839149585ff9e9df0e2f9b82a4d63d4298d0e1340ed97d82bb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2816185547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adffb6e0e4ab0c0696bc04fd7838772060eef2bdc50aeb814ef49773e334801`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 05 Dec 2022 21:19:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta1/traefik_v3.0.0-beta1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 05 Dec 2022 21:19:03 GMT
EXPOSE 80
# Mon, 05 Dec 2022 21:19:04 GMT
ENTRYPOINT ["/traefik"]
# Mon, 05 Dec 2022 21:19:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf10c072ea1decad27162e33014b87a4a0d893a08f6259c83615886f7689580`  
		Last Modified: Mon, 05 Dec 2022 21:20:11 GMT  
		Size: 37.6 MB (37593045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b816ab54a1f9bf5eb43e0aea31c4b44fdec25fa6db44d02f58eb46cf021eb730`  
		Last Modified: Mon, 05 Dec 2022 21:19:57 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff05f49a360e835df322dccf350bd6ff8d907a67ce3ff32dad883a3e9ac66d61`  
		Last Modified: Mon, 05 Dec 2022 21:19:56 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9019e3961bc041a48bf292b9992be18498cc417cd524c779548b66686b7586c1`  
		Last Modified: Mon, 05 Dec 2022 21:19:57 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

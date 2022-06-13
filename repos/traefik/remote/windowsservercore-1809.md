## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:b813d64a5c1eb3498986d5a316fa433df682acfa3038a9467f72232655fe3d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull traefik@sha256:7d454bf6f16177192750790acdbde2230a4d390a06b36683e92e5fc276a7f7b2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2532336814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef3d6aed360b6013f3eac849ed76ff75eeaca4fd73dfec990b913776e8a164e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 13 Jun 2022 18:17:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.7.1/traefik_v2.7.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 13 Jun 2022 18:17:17 GMT
EXPOSE 80
# Mon, 13 Jun 2022 18:17:18 GMT
ENTRYPOINT ["/traefik"]
# Mon, 13 Jun 2022 18:17:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc81fc68b4bd26ace09cac1f9e156a7f10c4a01fb84c1bd61156bf85efeac85`  
		Last Modified: Mon, 13 Jun 2022 18:18:58 GMT  
		Size: 28.3 MB (28275302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2b74c1667e6fd86372a21e937c532e1aa5a02c0c5590cdf2990e82bb1e6caa`  
		Last Modified: Mon, 13 Jun 2022 18:18:27 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5ec0fd7a47d0f100d28be14844121e6ef46f7d279f9365d6f4c5ae34833395`  
		Last Modified: Mon, 13 Jun 2022 18:18:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613e0863856475e19f15fbdf6bcf5516e0962a80fa16605d3ae57f8c2d4e2334`  
		Last Modified: Mon, 13 Jun 2022 18:18:27 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

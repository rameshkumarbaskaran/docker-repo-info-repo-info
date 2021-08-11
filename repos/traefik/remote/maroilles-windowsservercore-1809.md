## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7d1d137d268e564085e5c05f918bf4346a8290ab611c57d1ccf1e08e79b0006e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:ec1da595d84f5b3257698735564626a30c0560d9e68aa759d32cf96ed1625015
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2704291103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e6922cc13d4e220d195b7a6d7aac00de05dfb4bb78eb345efe16dd2a6ebd88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 22:23:45 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 11 Aug 2021 22:23:48 GMT
EXPOSE 80
# Wed, 11 Aug 2021 22:23:50 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Aug 2021 22:23:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:8e191a5bf292d7a12c5f917dde336d2439d4d22f34b3ccc93ba2ec56eb429a5e`  
		Last Modified: Wed, 11 Aug 2021 22:25:11 GMT  
		Size: 18.3 MB (18287524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e368da9720874eda4c481f2fbfbc13d345ce8b07efd443a946a7f0a002163a9e`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a826777ecee2f4cb9fcf66ed49eff2226c0e7d5efcd438e572f89c791bfaaa`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac5b0da240f2ab9425ecd3484d6a900c5563251d11a6c4f9872fdc3f02f1635`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
